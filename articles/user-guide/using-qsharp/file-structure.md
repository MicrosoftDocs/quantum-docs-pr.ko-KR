---
title: Q# 파일 구조
description: 파일의 구조 및 구문에 대해 설명 합니다 Q# .
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
no-loc:
- Q#
- $$v
ms.openlocfilehash: 98b3a2e35186989b8191cc566a5d5310bc26eafc
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833316"
---
# <a name="no-locq-file-structure"></a>Q# 파일 구조

Q#파일은 *네임 스페이스 선언*시퀀스로 구성 됩니다.
각 네임 스페이스 선언에는 사용자 정의 형식, 작업 및 함수에 대 한 선언이 포함 되며, 각 선언 형식 및 순서에 관계 없이 임의 개수의 형식을 포함할 수 있습니다.
네임 스페이스의 선언에 대 한 자세한 내용은 [사용자 정의 형식](xref:microsoft.quantum.guide.types#user-defined-types), [작업](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)및 [함수](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions)를 참조 하세요.

네임 스페이스 선언 외부에 나타날 수 있는 유일한 텍스트는 주석입니다.
특히 네임 스페이스에 대 한 문서 주석은 선언 앞에 나옵니다. 자세한 내용은이 문서의 [문서 주석](#documentation-comments) 을 참조 하세요. 

## <a name="namespace-declarations"></a>네임스페이스 선언

Q#일반적으로 파일에는 네임 스페이스 선언이 하나만 포함 될 수 있지만, 빈 상태로 있거나 주석을 포함 하거나, 여러 네임 스페이스를 포함할 수 있습니다.
네임 스페이스 선언은 중첩할 수 없습니다.

Q#동일한 이름을 가진 형식, 작업 또는 함수 선언이 없으면 함께 컴파일되는 여러 파일에 동일한 네임 스페이스를 선언할 수 있습니다.
특히 선언이 동일한 경우에도 여러 파일에서 동일한 네임 스페이스에 동일한 형식을 정의 하는 것은 유효 하지 않습니다.

네임 스페이스 선언은 키워드로 구성 된 `namespace` 다음 네임 스페이스의 이름 및 중괄호로 묶인 네임 스페이스에 포함 된 선언으로 구성 됩니다 `{ }` .
네임 스페이스 이름은 마침표로 구분 된 하나 이상의 법적 기호의 시퀀스에 대 한 .NET 패턴을 따릅니다 `.` .
예를 들어 `MyQuantumStuff` 및 `Microsoft.Quantum.Intrinsic` 는 유효한 네임 스페이스 이름입니다.
규칙에 따라 네임 스페이스 이름에서 기호를 대문자로 표기 해야 합니다.

파일에서 나중에 선언 된 형식 또는 callables에 대 한 참조가 제대로 확인 됩니다. 형식, 작업 또는 함수 선언이 참조 앞에 오지 않아도 됩니다.

## <a name="open-directives"></a>지시문 열기

네임 스페이스 블록 내에서 지시문을 사용 `open` 하 여 특정 네임 스페이스에서 선언 된 모든 형식 및 callables을 가져오고 정규화 되지 않은 이름으로 참조 합니다.
이러한 `open` 지시문은 키워드로 구성 된 `open` 다음 열 네임 스페이스와 종료 세미콜론으로 구성 됩니다.

> [!NOTE] 
> 모든 `open` 지시문은 `function` `operation` `newtype` 네임 스페이스 블록의, 또는 선언 앞에 나와야 합니다.

필요에 따라 열린 네임 스페이스의 짧은 이름을 정의할 수 있습니다. 약식 이름이 정의 된 경우 해당 네임 스페이스의 모든 요소를 정의 된 짧은 이름으로 정규화 해야 합니다. 예를 들어 다음과 같은 네임 스페이스 선언 및 open 지시문이 있다고 가정 합니다.

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

선언 된 작업에서의 작업을 사용 하는 경우 `Op` `Microsoft.Quantum.Intrinsic` 만 사용 하 여 호출 `Op` 합니다.
그러나에서 특정 함수를 호출 하려면 `Fn` 를 `Microsoft.Quantum.Math` 사용 하 여 호출 해야 합니다 `Math.Fn` .

`open`지시문은 파일 내의 전체 네임 스페이스 블록에 적용 됩니다.
따라서 앞에서와 동일한 파일에 추가 네임 스페이스를 정의 하는 경우에는 Q# `NS` 두 번째 네임 스페이스에 정의 된 모든 작업/함수/형식이 열려 있는 지시문을 `Microsoft.Quantum.Intrinsic` 반복 하지 않는 한 또는에서 어떠한 항목에도 액세스할 수 없습니다 `Microsoft.Quantum.Math` . 

현재 네임 스페이스 *에서 열리지 않는* 다른 네임 스페이스에 정의 된 형식 또는 호출 가능를 참조 하려면 정규화 된 이름으로 참조 해야 합니다.
예를 들어 `Op` 네임 스페이스에서 라는 작업이 지정 된 경우 `X.Y` :

* `X.Y.Op` `X.Y` 네임 스페이스가 현재 블록에서 이전에 열리지 않는 한 정규화 된 이름으로 참조 해야 합니다. 
* 네임 스페이스를 열 때에도 `X` 작업을로 참조할 수 없습니다 `Y.Op` .
* `Z`해당 네임 스페이스 및 파일에서에 대 한 약식 이름을 정의한 경우를 `X.Y` 로 참조 해야 합니다 `Op` `Z.Op` . 

일반적으로 지시문을 사용 하 여 네임 스페이스를 포함 하는 것이 좋습니다 `open` .
두 네임 스페이스가 같은 이름을 사용 하 여 구문을 정의 하 고 현재 소스가 양쪽에서 구문을 사용 하는 경우 정규화 된 이름을 사용 해야 합니다.

Q# 는 다른 .NET 언어로 이름을 지정 하는 것과 동일한 규칙을 따릅니다.
그러나에서는 Q# 네임 스페이스에 대 한 상대 참조를 지원 하지 않습니다.
예를 들어 네임 스페이스가 `a.b` 열려 있으면 이라는 작업에 대 한 참조는 `c.d` 전체 이름이 있는 작업으로 확인 *되지* 않습니다 `a.b.c.d` .

## <a name="formatting"></a>서식

대부분의 Q# 문과 지시문은 종료 세미콜론 ()으로 끝납니다 `;` .
문 및 선언 (예 `for` : `operation` 다음 섹션 참조)으로 끝나는 문과 선언에는 종료 세미콜론이 필요 하지 않습니다.
각 문 설명에는 종료 세미콜론이 필요한 지 여부에 대 한 설명이 나와 있습니다.

식, 선언 및 지시문과 같은 문을 여러 줄로 나눌 수 있습니다.
여러 문을 한 줄에 배치 하지 마십시오.

## <a name="statement-blocks"></a>문 블록

Q# 문은 중괄호에 포함 된 문 블록으로 그룹화 됩니다 `{ }` . 문 블록은 여는 것으로 시작 하 `{` 고 닫는로 끝납니다 `}` .

다른 블록 내에 어휘를 싸인 문 블록은 포함 하는 블록의 하위 블록으로 간주 됩니다. 포함 및 하위 블록은 외부 및 내부 블록이 라고도 합니다.

## <a name="comments"></a>의견

주석은 두 개의 슬래시 ()로 시작 `//` 하 고 줄의 끝까지 계속 됩니다.
주석은 소스 파일의 어디에 나 나타날 수 있습니다 Q# .

## <a name="documentation-comments"></a>설명서 주석

세 개의 슬래시 ()로 시작 하는 주석은 `///` 네임 스페이스, 작업, 특수화, 함수 또는 형식 정의 바로 앞에 표시 될 때 컴파일러에서 특수 하 게 처리 됩니다.
이 경우 컴파일러는 다른 .NET 언어와 동일한 정의 된 호출 가능 또는 사용자 정의 형식에 대 한 설명서로 처리 합니다.

주석 내에서 `///` API 설명서의 일부로 표시 되는 텍스트는 특수 하 게 명명 된 헤더로 표시 되는 설명서의 여러 부분을 사용 하 여 [Markdown](https://daringfireball.net/projects/markdown/syntax)로 형식이 지정 됩니다.
Markdown에서 확장을 사용 `@"<ref target>"` 하 여의 상호 참조 작업, 함수 및 사용자 정의 형식을 사용 Q# 합니다. `<ref target>`참조 된 코드 개체의 정규화 된 이름으로 대체 합니다.
다른 설명서 엔진은 추가 Markdown 확장을 지원할 수도 있습니다.

예를 들면 다음과 같습니다.

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

다음 이름은 문서 주석 헤더로 유효 합니다.

- **요약**: 함수 또는 작업의 동작에 대 한 간단한 요약 또는 형식의 용도입니다. 요약의 첫 번째 단락은 가리키기 정보에 사용 됩니다. 일반 텍스트 여야 합니다.
- **설명**: 함수 또는 작업의 동작에 대 한 설명 또는 형식의 용도입니다. 요약 및 설명은 함께 함수, 작업 또는 형식에 대해 생성 된 설명서 파일을 구성 합니다.
  이 설명에서는 인라인 LaTeX 형식의 기호 및 수식을 지원 합니다.
- **Input**: 작업 또는 함수에 대 한 입력 튜플의 설명입니다.
  입력 튜플의 각 요소를 나타내는 추가 Markdown 하위 섹션을 포함할 수 있습니다.
- **Output**: 작업 또는 함수에서 반환 된 튜플에 대 한 설명입니다.
- **형식 매개 변수**: 각 제네릭 형식 매개 변수에 대해 하나의 추가 하위 섹션을 포함 하는 빈 섹션입니다.
- **예**: 사용 중인 작업, 함수 또는 형식의 간단한 예입니다.
- **주의**: 작업, 함수 또는 형식에 대 한 몇 가지 측면을 설명 하는 기타 prose.
- **참고**항목: 관련 된 함수, 작업 또는 사용자 정의 형식을 나타내는 정규화 된 이름 목록입니다.
- **참조**: 문서화 된 항목에 대 한 참조 및 인용의 목록입니다.

## <a name="next-steps"></a>다음 단계

의 [작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions) 에 대해 알아봅니다 Q# .