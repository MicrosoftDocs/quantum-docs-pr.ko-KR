---
title: Microsoft QDK에 코드 기여
description: Microsoft Quantum Development Kit (QDK)에 샘플 및 라이브러리 코드를 제공 하는 방법에 대해 알아봅니다.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.code
ms.openlocfilehash: 1882e640dacf3987745ed225fef18636726f70a8
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907480"
---
# <a name="contributing-code"></a>코드 기여 #

문제를 보고 하 고 설명서를 개선 하는 것 외에도 퀀텀 개발 키트에 대 한 코드는 퀀텀 프로그래밍 커뮤니티의 동료에 게 도움이 되는 매우 직접적인 방법일 수 있습니다.
코드를 사용 하면 문제를 해결 하거나, 새 예제를 제공 하거나, 기존 라이브러리를 더 쉽게 사용할 수 있도록 하거나 완전히 새로운 기능을 추가할 수 있습니다.

이 가이드에서는 기여를 가장 잘 하는 데 도움이 되도록 끌어오기 요청을 검토할 때 표시 되는 내용을 자세히 설명 합니다.

## <a name="what-we-look-for"></a>찾는 내용 ##

이상적인 코드 기여는 퀀텀 Development Kit 리포지토리의 기존 작업을 기반으로 하 여 문제를 해결 하거나 기존 기능을 확장 하거나 리포지토리의 범위 내에 있는 새 기능을 추가 합니다.
코드 기여를 수락 하는 경우이는 퀀텀 개발 키트 자체의 일부가 되며, 나머지 퀀텀 개발 키트와 동일한 방식으로 새로운 기능이 출시, 유지 관리 및 개발 됩니다.
따라서 기여에 의해 추가 된 기능이 잘 테스트 되 고 문서화 되는 경우 유용 합니다.

### <a name="unit-tests"></a>단위 테스트 ###

라고과 같은 라이브러리를 구성 하는 Q # 함수, 작업 및 사용자 정의 형식은 [**Microsoft/QuantumLibraries**](https://github.com/Microsoft/QuantumLibraries/) 리포지토리에서 개발의 일부로 자동으로 테스트 됩니다.
예를 들어 새 끌어오기 요청을 열면 [Azure Pipelines](https://azure.microsoft.com/services/devops/pipelines/) 구성에서 끌어오기 요청의 변경 내용이 퀀텀 프로그래밍 커뮤니티에 의존 하는 기존 기능을 중단 하지 않았는지 확인 합니다.

최신 Q # 버전을 사용 하 여 단위 테스트는 `@Test("QuantumSimulator")` 특성을 사용 하 여 정의 됩니다. 인수는 "QuantumSimulator", "ToffoliSimulator", "TraceSimulator" 또는 실행 대상을 지정 하는 정규화 된 이름일 수 있습니다. 다른 실행 대상을 정의 하는 여러 특성이 동일한 호출 가능에 연결 될 수 있습니다. 일부 테스트는 `Test`에서 끝나는 모든 Q # 함수 및 작업을 [xunit](https://xunit.github.io/) 프레임 워크로 노출 하는 사용 되지 않는 [Microsoft.](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) n e t. n e t 장치 패키지를 계속 사용 합니다. 이 패키지는 더 이상 단위 테스트를 정의 하는 데 필요 하지 않습니다. 

다음 함수를 사용 하 여 <xref:microsoft.quantum.canon.fst> 및 <xref:microsoft.quantum.canon.snd> 함수에서 대표적인 예의 올바른 출력을 반환 하는지 확인할 수 있습니다.
`Fst` 또는 `Snd`의 출력이 잘못 된 경우 `fail` 문을 사용 하 여 테스트 실패를 발생 시킵니다.

```qsharp
@Test("QuantumSimulator")
function PairTest () : Unit {
    let pair = (12, PauliZ);

    if (Fst(pair) != 12) {
        let actual = Fst(pair);
        fail $"Expected 12, actual {actual}.";
    }

    if (Snd(pair) != PauliZ) {
        let actual = Snd(pair);
        fail $"Expected PauliZ, actual {actual}.";
    }
}
```

표준 라이브러리 가이드의 [테스트 섹션](xref:microsoft.quantum.libraries.diagnostics) 에 있는 기술을 사용 하 여 더 복잡 한 조건을 확인할 수 있습니다.
예를 들어 다음 테스트는 <xref:microsoft.quantum.canon.applywith>에 의해 호출 되는 `H(q); X(q); H(q);` `Z(q)`와 동일한 지 확인 합니다.

```qsharp
@Test("QuantumSimulator")
operation TestApplyWith() : Unit {
    let actual = ApplyWith(H, X, _);
    let expected = Z;
    AssertOperationsEqualReferenced(ApplyToEach(actual, _), ApplyToEachA(expected, _), 4);
}
```

새 기능을 추가 하는 경우 새 테스트를 추가 하 여 기여도가 예상 하는 작업을 수행 하는 것이 좋습니다.
이렇게 하면 나머지 커뮤니티에서 기능을 유지 관리 하 고 개발할 수 있으며, 특히 다른 개발자가 기능을 사용할 수 있다는 것을 알 수 있습니다.

> [!NOTE]
> 이는 다른 방법으로도 작동 합니다.
> 일부 테스트가 누락 된 기존 기능이 있는 경우 테스트 검사를 추가 하면 커뮤니티에 훌륭한 기여를 내릴 수 있습니다.

로컬에서 단위 테스트는 Visual Studio 테스트 탐색기 또는 `dotnet test` 명령을 사용 하 여 실행할 수 있으므로 끌어오기 요청을 열기 전에 기여를 확인할 수 있습니다.

<!-- TODO:
### Comments and Documentation ###

### Citations and References ### -->

## <a name="when-well-reject-a-pull-request"></a>끌어오기 요청을 거부 하는 경우 ##

경우에 따라 끌어오기 요청이 기여를 거부 합니다.
이러한 상황이 발생 하는 경우에는 특정 기여를 수락 하지 못할 수 있는 여러 가지 이유가 있으므로 잘못 된 것입니다.
가장 일반적으로 퀀텀 프로그래밍 커뮤니티에 기여 하는 것은 매우 좋지만 퀀텀 개발 키트 리포지토리를 개발 하기에 적합 하지 않습니다.
이러한 경우에는 사용자 고유의---리포지토리를 사용 하는 것이 좋습니다 .이는 NuGet.org을 배포 하는 것과 동일한 방식으로 GitHub 및를 사용 하 여 고유한 라이브러리를 쉽게 만들고 배포할 수 있다는 것입니다. 지금 바로 라이브러리를 만드세요.

그 외에는 아직 유지 관리 및 개발할 준비가 되지 않았기 때문에 좋은 기여를 거부할 수 있습니다.
모든 작업을 수행 하기 어려울 수 있으므로 로드맵으로 작업 하는 데 가장 적합 한 기능을 계획 하 고 있습니다.
이는 기능을 타사 라이브러리로 해제 하는 것이 좋은 경우도 있습니다.
또는 microsoft에서 제공 하는 최상의 작업을 수행할 수 있도록 로드맵에 보다 적합 한 기능을 수정 하는 데 도움을 요청할 수 있습니다.

또한 더 많은 설명서 또는 단위 테스트가 필요한 경우에도 끌어오기 요청에 대 한 변경 사항을 요청 하 여 사용자가 기능을 찾는 것이 더 어려워질 수 있도록 하는 데 도움이 됩니다.
이러한 경우 추가 하거나 변경할 수 있는 항목에 대 한 코드 검토에 몇 가지 조언을 제공 하 여 참여를 더 쉽게 포함할 수 있도록 합니다.

마지막으로 [Microsoft 오픈 소스 준수](https://opensource.microsoft.com/codeofconduct/)에 설명 된 대로 퀀텀 컴퓨팅 커뮤니티를 손상 시키는 기여를 수락할 수 없습니다.
Microsoft는 현재 훌륭한 다양성에서 전체 퀀텀 컴퓨팅 커뮤니티를 제공 하 고 향후 더 포괄적으로 성장 하 고 있습니다.
이러한 목표를 실현 하는 데 도움을 주셔서 감사 합니다.

## <a name="next-steps"></a>다음 단계 ##

퀀텀 개발 키트를 전체 퀀텀 프로그래밍 커뮤니티에서 사용할 수 있도록 하는 데 도움을 주셔서 감사 합니다.
자세히 알아보려면 Q # 스타일에 대 한 다음 가이드를 계속 진행 하세요.

> [!div class="nextstepaction"]
> [Q # 스타일 지침에 대해 알아보기](xref:microsoft.quantum.contributing.style)
