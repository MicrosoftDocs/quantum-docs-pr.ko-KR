---
title: 'Q # 파일 구조'
description: 'Q # 파일의 구조 및 구문에 대해 설명 합니다.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
ms.openlocfilehash: cbee92c6d7e765237a7a42532dd7012b51421708
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430971"
---
# <a name="q-file-structure"></a>Q # 파일 구조

모든 Q # 작업, 함수 및 사용자 정의 형식은 네임 스페이스 내에서 정의 됩니다.

Q # 파일은 *네임 스페이스 선언*시퀀스로 구성 됩니다.
각 네임 스페이스 선언에는 사용자 정의 형식, 작업 및 함수에 대 한 선언이 포함 됩니다.
네임 스페이스 선언에는 임의의 순서 대로 각 선언 형식이 포함 될 수 있습니다.
네임 스페이스 내에서 [사용자 정의 형식](xref:microsoft.quantum.guide.types#user-defined-types), [작업](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)및 [함수](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) 를 선언 하는 방법에 대 한 자세한 내용은 다음 링크를 참조 하세요.

네임 스페이스 선언 외부에 나타날 수 있는 유일한 텍스트는 주석입니다.
특히 네임 스페이스에 대 한 문서 주석 (아래 세부 정보)이 선언 앞에 나옵니다.

## <a name="namespace-declarations"></a>네임스페이스 선언

Q # 파일은 일반적으로 정확히 하나의 네임 스페이스 선언을 포함 하지만, 없거나 비어 있거나 주석을 포함 하거나, 여러 네임 스페이스를 포함할 수 있습니다.
네임 스페이스 선언은 중첩 될 수 없습니다.

동일한 네임 스페이스는 동일한 이름을 가진 형식, 작업 또는 함수 선언이 없으면 함께 컴파일되는 여러 Q # 파일에 선언할 수 있습니다.
특히 선언이 동일한 경우에도 여러 파일에서 동일한 네임 스페이스에 동일한 형식을 정의 하는 것은 유효 하지 않습니다.

네임 스페이스 선언은 키워드로 구성 됩니다 `namespace` . 그 다음에는 네임 스페이스 이름, 여는 중괄호 `{` , 네임 스페이스에 포함 된 선언 및 닫는 중괄호가 `}` 있습니다.
네임 스페이스 이름은 마침표로 구분 된 하나 이상의 법적 기호의 시퀀스에 대 한 .NET 패턴을 따릅니다 `.` .
예를 들어 `MyQuantumStuff` 및 `Microsoft.Quantum.Intrinsic` 는 유효한 네임 스페이스 이름입니다.
규칙에 따라 네임 스페이스 이름의 기호는 대문자로 되어 있지만 반드시 필요한 것은 아닙니다.

파일에서 나중에 선언 된 형식 또는 callables에 대 한 참조가 제대로 확인 됩니다. 형식, 작업 또는 함수 선언이 참조 앞에 오지 않아도 됩니다.

## <a name="open-directives"></a>지시문 열기

네임 스페이스 블록 내에서 `open` 지시문을 사용 하 여 특정 네임 스페이스에서 선언 된 모든 형식 및 callables을 가져와서 정규화 되지 않은 이름으로 참조할 수 있습니다.
이러한 `open` 지시문은 키워드로 구성 된 `open` 다음 열 네임 스페이스와 종료 세미콜론으로 구성 됩니다.

> [!NOTE] 
> 모든 `open` 지시문은 `function` `operation` `newtype` 네임 스페이스 블록의, 또는 선언 앞에 나와야 합니다.

필요에 따라 열린 네임 스페이스의 짧은 이름을 정의 하 여 해당 네임 스페이스의 모든 요소를 정의 된 약식 이름으로 정규화 하 고 필요에 따라 정규화 할 수 있습니다. 예를 들어 다음과 같은 네임 스페이스 선언 및 open 지시문이 있다고 가정 합니다.

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

선언 하는 작업이에서 작업을 사용 하는 경우를 `Op` `Microsoft.Quantum.Intrinsic` 사용 하 여 호출 `Op` 합니다.
그러나에서 특정 함수를 호출 하려는 경우를 `Fn` `Microsoft.Quantum.Math` 사용 하 여 호출 해야 `Math.Fn` 합니다.

`open`지시문은 파일 내의 전체 네임 스페이스 블록에 적용 됩니다.
따라서 위와 같은 Q # 파일에 추가 네임 스페이스를 정의 하는 경우에는 `NS` 두 번째 네임 스페이스에 정의 된 모든 작업/함수/형식이 열에 대 한 액세스 권한을 갖지 않습니다 `Microsoft.Quantum.Intrinsic` `Microsoft.Quantum.Math` . 

현재 네임 스페이스에서 열려 *있지* 않은 다른 네임 스페이스에 정의 된 형식 또는 호출 가능 이름은 정규화 된 이름으로 참조 되어야 합니다.
예를 들어 네임 스페이스가 `Op` `X.Y` `X.Y.Op` `X.Y` 현재 블록에서 이전에 열리지 않는 한 네임 스페이스에서 이름이 지정 된 작업은 정규화 된 이름으로 참조 되어야 합니다. 위에서 설명한 것 처럼 네임 스페이스를 연 경우에도 `X` 작업을로 참조할 수 없습니다 `Y.Op` .
의 약식 이름이 `Z` `X.Y` 해당 네임 스페이스 및 파일에 정의 된 경우에는를 `Op` 로 참조 해야 `Z.Op` 합니다. 

일반적으로 지시문을 사용 하 여 네임 스페이스를 포함 하는 것이 좋습니다 `open` .
두 네임 스페이스가 같은 이름을 사용 하 여 구문을 정의 하 고 현재 소스가 양쪽에서 구문을 사용 하는 경우 정규화 된 이름을 사용 해야 합니다.

Q #은 다른 .NET 언어로 이름을 지정 하는 것과 동일한 규칙을 따릅니다.
그러나 Q #에서는 네임 스페이스에 대 한 상대 참조를 지원 하지 않습니다.
즉, 네임 스페이스를 연 경우 이름이 인 작업에 대 `a.b` 한 참조는 `c.d` 전체 이름이 있는 작업으로 확인 *되지* 않습니다 `a.b.c.d` .

## <a name="formatting"></a>서식 지정

대부분의 Q # 문과 지시문은 종료 세미콜론 ()으로 끝납니다 `;` .
문과 `for` `operation` 문 블록 (아래 참조)으로 끝나는 문과 선언에는 종료 세미콜론이 필요 하지 않습니다.
각 문 설명에는 종료 세미콜론이 필요한 지 여부에 대 한 설명이 나와 있습니다.

식, 선언 및 지시문과 같은 문은 여러 줄에 걸쳐 분할 될 수 있습니다.
한 줄에 문이 여러 개 있는 것은 피해 야 합니다.

## <a name="statement-blocks"></a>문 블록

Q # 문은 문 블록으로 그룹화 됩니다.
문 블록은 여는 것으로 시작 하 `{` 고 닫는로 끝납니다 `}` .

다른 블록 내에 어휘를 싸인 문 블록은 포함 하는 블록의 하위 블록으로 간주 됩니다. 포함 및 하위 블록은 외부 및 내부 블록이 라고도 합니다.

## <a name="comments"></a>의견

주석은 두 개의 슬래시 ()로 시작 `//` 하 고 줄의 끝까지 계속 됩니다.
설명은 Q # 소스 파일의 어디에 나 나타날 수 있습니다.

## <a name="documentation-comments"></a>설명서 주석

세 개의 슬래시 ()로 시작 하는 주석은 `///` 네임 스페이스, 작업, 특수화, 함수 또는 형식 정의 바로 앞에 표시 될 때 컴파일러에서 특수 하 게 처리 됩니다.
이 경우 다른 .NET 언어의 경우와 같이 정의 된 호출 가능 또는 사용자 정의 형식에 대 한 설명서로 해당 내용이 사용 됩니다.

주석 내에서 `///` API 설명서의 일부로 표시 되는 텍스트는 [Markdown](https://daringfireball.net/projects/markdown/syntax)로 형식이 지정 되 고 설명서의 다른 부분은 특수 하 게 명명 된 헤더로 표시 됩니다.
Markdown에 대 한 확장으로, Q #의 작업, 함수 및 사용자 정의 형식에 대 한 상호 참조는를 사용 하 여 포함할 수 있습니다 `@"<ref target>"` `<ref target>` . 여기서는 참조 되는 코드 개체의 정규화 된 이름으로 바뀝니다.
선택적으로 설명서 엔진에서 추가 Markdown 확장을 지원할 수도 있습니다.

예들 들어 다음과 같습니다.

```qsharp
/// # Summary
/// Given an operation and a target for that operation,
/// applies the given operation twice.
///
/// # Input
/// ## op
/// The operation to be applied.
/// ## target
/// The target to which the operation is to be applied.
///
/// # Type Parameters
/// ## 'T
/// The type expected by the given operation as its input.
///
/// # Example
/// ```Q#
/// // Should be equivalent to the identity.
/// ApplyTwice(H, qubit);
/// ```
///
/// # See Also
/// - Microsoft.Quantum.Intrinsic.H
operation ApplyTwice<'T>(op : ('T => Unit), target : 'T) : Unit {
    op(target);
    op(target);
}
```

다음 이름은 문서 주석 헤더로 인식 됩니다.

- **요약**: 함수 또는 작업의 동작에 대 한 간략 한 요약 또는 형식의 용도입니다. 요약의 첫 번째 단락은 가리키기 정보에 사용 됩니다. 일반 텍스트 여야 합니다.
- **설명**: 함수 또는 작업의 동작에 대 한 설명 또는 형식의 용도에 대 한 설명입니다. 요약 및 설명은 함수, 작업 또는 형식에 대해 생성 된 설명서 파일을 구성 하기 위해 연결 됩니다.
  설명에는 인라인 LaTeX 형식의 기호 및 수식이 포함 될 수 있습니다.
- **Input**: 작업 또는 함수에 대 한 입력 튜플의 설명입니다.
  입력 튜플의 각 개별 요소를 나타내는 추가 Markdown 하위 섹션이 포함 될 수 있습니다.
- **Output**: 작업 또는 함수에서 반환 된 튜플에 대 한 설명입니다.
- **형식 매개 변수**: 각 제네릭 형식 매개 변수에 대 한 추가 하위 섹션을 하나씩 포함 하는 빈 섹션입니다.
- **예**: 사용 중인 작업, 함수 또는 형식에 대 한 간단한 예입니다.
- **주의**: 작업, 함수 또는 형식에 대 한 몇 가지 측면을 설명 하는 기타 prose.
- **참고**항목: 관련 된 함수, 작업 또는 사용자 정의 형식을 나타내는 정규화 된 이름 목록입니다.
- **참조**: 문서화 되는 항목에 대 한 참조 및 인용의 목록입니다.

## <a name="whats-next"></a>다음 단계
Q #의 [작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions) 에 대해 알아봅니다.