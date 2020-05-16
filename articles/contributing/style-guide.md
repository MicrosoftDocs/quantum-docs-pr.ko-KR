---
title: 'Microsoft Q # 스타일 가이드'
description: 'Q # 프로그램 및 라이브러리에 대 한 이름 지정, 입력, 설명서 및 서식 규칙에 대해 알아봅니다.'
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.style
ms.openlocfilehash: dfb2b1779e3ddc77fc74697bc4dc2904b1a0c70f
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426920"
---
# <a name="q-style-guide"></a>Q # 스타일 가이드 #
## <a name="general-conventions"></a>일반 규칙 ##

이 가이드에서 제안 하는 규칙은 Q #으로 작성 된 프로그램 및 라이브러리를 읽고 이해할 수 있도록 하기 위한 것입니다.

## <a name="guidance"></a>지침

다음을 권장 합니다.

- 사용자에 게 더 읽기 쉽고 이해 하기 쉬운 코드를 제공 하기 위해 의도적으로 수행 하는 경우가 아니면 규칙을 무시 하지 마십시오.

## <a name="naming-conventions"></a>명명 규칙 ##

퀀텀 개발 키트를 제공할 때 퀀텀 개발자가 쉽게 읽을 수 있는 프로그램을 작성 하는 데 도움이 되는 함수 및 작업 이름에 대해 노력 하 고 있으며이를 최소화 합니다.
의 중요 한 부분은 함수, 작업 및 형식에 대 한 이름을 선택할 때 프로그래머가 퀀텀 개념을 표현 하는 데 사용 하는 *어휘* 를 설정 하는 것입니다. 이 옵션을 사용 하면 명확 하 게 통신할 수 있도록 도와 드릴 수 있습니다.
이는 도입 된 이름이 은둔 대신 명확성을 제공 하는지 확인 하는 책임을 집니다.
이 섹션에서는 Q # 개발 커뮤니티에서 가장 잘 활용 하는 데 도움이 되는 명시적 지침을 기준으로이 의무를 어떻게 충족 하는지 자세히 설명 합니다.

### <a name="operations-and-functions"></a>작업 및 함수 ###

이름을 설정 해야 하는 첫 번째 작업 중 하나는 지정 된 기호가 함수 또는 작업을 나타내는지 여부입니다.
함수 및 작업 간의 차이점은 코드 블록이 동작 하는 방식을 이해 하는 데 중요 합니다.
함수와 작업을 사용자에 게 구분 하기 위해이 질문에는 의도 하지 않은 결과를 사용 하 여 퀀텀 작업을 모델링 하는 데 사용 됩니다.
즉, 작업은 어떤 작업을 *수행* 합니다.

이와 대조적으로 함수는 데이터 간의 수학적 관계를 설명 합니다.
식은 이며 `Sin(PI() / 2.0)` *is* `1.0` 프로그램이 나 그 이상 비트의 상태에 대해서는 아무 것도 의미 하지 않습니다.

요약 하면 함수는 작업을 수행 합니다.
이러한 구분은 작업을 명사로 서 동사와 함수로 이름을 지정할 것을 제안 합니다.

> [!NOTE]
> 사용자 정의 형식이 선언 되 면 해당 형식의 인스턴스를 생성 하는 새 함수가 암시적으로 동시에 정의 됩니다.
> 이러한 관점에서 사용자 정의 형식은 형식 자체와 생성자 함수에 일관 된 이름을 갖도록 명사로 이름을 지정 해야 합니다.

적절 한 경우 작업 이름이 작업에서 수행한 효과를 명확 하 게 나타내는 동사로 시작 되는지 확인 합니다.
예들 들어 다음과 같습니다.

- `MeasureInteger`
- `EstimateEnergy`
- `SampleInt`

특별 한 언급할 만한 사례는 작업이 다른 작업을 입력으로 사용 하 고 호출 하는 경우입니다.
이러한 경우에는 외부 작업이 정의 될 때 입력 작업에서 수행 하는 동작이 명확 하지 않으므로 오른쪽 동사가 명확 하지 않습니다.
`Apply`, 및에서와 같이 동사를 권장 합니다 `ApplyIf` `ApplyToEach` `ApplyToFirst` .
다른 동사는이 경우에도 유용 하 게 사용할 수 있습니다 `IterateThroughCartesianPower` .

| 동사 | 예상 효과 |
| ---- | ------ |
| 적용 | 입력으로 제공 된 작업을 라고 합니다. |
| Assert | 가능한 퀀텀 측정의 결과에 대 한 가설은 시뮬레이터에 의해 확인 됩니다. |
| 견적 | 하나 이상의 측정값 으로부터 그려진 추정치를 나타내는 고전 값이 반환 됩니다. |
| 측정값 | 퀀텀 측정이 수행 되며 결과가 사용자에 게 반환 됩니다. |
| 준비 | 지정 된 비트 레지스터가 특정 상태로 초기화 됩니다. |
| 샘플 | 일부 분포에서 무작위로 값이 반환 됩니다. |

함수의 경우 일반적인 명사를 선호 하는 동사를 사용 하지 않는 것이 좋습니다 (아래의 적절 한 명사에 대 한 지침 참조).

- `ConstantArray`
- `Head`
- `LookupFunction`

특히 거의 모든 경우에, 함수 이름이 퀀텀 프로그램의 다른 위치에 있는 작업 또는 부작용에 강력 하 게 연결 되어 있음을 나타내기 위해 해당 하는 경우 과거 participles를 사용 하는 것이 좋습니다.
예를 들어는 `ControlledOnInt` 동사 "control"의 part 분사 폼을 사용 하 여 함수에서 인수를 수정 하는 형용사로 동작 함을 표시 합니다.
이 이름에는 아래에서 설명한 대로 기본 제공 함수의 의미 체계와 일치 하는 추가 혜택이 있습니다 `Controlled` .
마찬가지로 _에이전트 명사_ 는와 강력 하 게 연결 된 udt의 이름에 대 한 작업 이름에서 함수와 UDT 이름을 생성 하는 데 사용할 수 있습니다 `Encoder` `Encode` .

# <a name="guidance"></a>[지침](#tab/guidance)

다음을 권장 합니다.

- 작업 이름에 대 한 동사를 사용 합니다.
- 함수 이름에 명사 또는 형용사를 사용 합니다.
- 사용자 정의 형식 및 특성에는 명사를 사용 합니다.
- 모든 호출 가능 이름의 경우 `CamelCase` , 또는에 대해 강력한 기본 설정으로를 사용 `pascalCase` `snake_case` `ANGRY_CASE` 합니다. 특히 호출 가능 이름이 대문자로 시작 하는지 확인 합니다.
- 모든 지역 변수의 경우 `pascalCase` , 또는에 대해 강력한 기본 설정으로를 사용 `CamelCase` `snake_case` `ANGRY_CASE` 합니다. 특히 지역 변수가 소문자로 시작 하는지 확인 합니다.
- `_`함수 및 작업 이름에 밑줄을 사용 하지 마십시오. 계층의 추가 수준이 필요한 경우 네임 스페이스 및 네임 스페이스 별칭을 사용 합니다.

# <a name="examples"></a>[예](#tab/examples)

|   | 속성 | Description |
|---|------|-------------|
| ☑ | `operation ReflectAboutStart` | 작업의 효과를 나타내려면 동사 ("반사")를 사용 하지 않습니다. |
| ☒ | <s>`operation XRotation`</s> | 명사구를 사용 하는 것은 연산이 아니라 함수를 제안 합니다. |
| ☒ | <s>`operation search_oracle`</s> | `snake_case`Contravenes Q # 표기법을 사용 합니다. |
| ☒ | <s>`operation Search_Oracle`</s> | 작업 이름 contravenes Q # notation 내부에 밑줄을 사용 합니다. |
| ☑ | `function StatePreparationOracle` | 명사구를 사용 하면 함수가 연산을 반환 하는 것을 의미 합니다. |
| ☑ | `function EqualityFact` | 명사 ("fact")를 명확 하 게 사용 하 여 함수가 함수 임을 나타내야 합니다. |
| ☒ | <s>`function GetRotationAngles`</s> | 동사 ("get")를 사용 하는 것은 이것이 작업 임을 나타냅니다. |
| ☑ | `newtype GeneratorTerm` | 명사 구를 사용 하면 UDT 생성자 호출 결과를 명확 하 게 참조할 수 있습니다. |
| ☒ | <s>`@Attribute() newtype RunOnce()`</s> | 동사 구를 사용 하면 UDT 생성자가 연산이 됩니다. |
| ☑ | `@Attribute() newtype Deprecated(Reason : String)` | 명사구를 사용 하면 특성의 사용이 전달 됩니다. |

***

### <a name="shorthand-and-abbreviations"></a>약어 및 약어 ###

위의 충고도 불구는 퀀텀 컴퓨팅에서 공통적이 고 널리 사용 되는 여러 가지 형태의 축약형입니다.
특히 대상 컴퓨터의 작업에 내장 된 작업의 경우 기존 및 일반적인 약어를 사용 하는 것이 좋습니다.
예를 들어 대신 및 대신 이름을 선택 `X` `ApplyX` `Rz` `RotateAboutZ` 합니다.
이러한 약어를 사용 하는 경우 작업 이름은 모두 대문자 여야 합니다 (예: `MAJ` ).

일반적으로 사용 되는 머리글자어의 경우에는 "퀀텀 푸리에 변환"의 경우 "QFT"와 같은의 두문자어 정의에이 규칙을 적용할 때 주의 해야 합니다.
전체 이름에 머리글자어 및의 두문자어 정의를 사용 하는 데 일반적인 .NET 규칙을 사용 하는 것이 좋습니다 .이에 대 한 자세한 내용은 다음과 같습니다.

- 두 문자로 된 머리글자어와의 두문자어 정의는 대문자로 명명 됩니다 (예: `BE` "빅 endian"의 경우).
- 모든 긴 머리글자어 및의 두문자어 정의는 `CamelCase` (예: `Qft` "퀀텀 푸리에 변환"의 경우)로 이름이 지정 됩니다.

따라서 QFT를 구현 하는 작업을 `QFT` 약어로 호출 하거나로 작성할 수 있습니다 `ApplyQft` .

특히 일반적으로 사용 되는 작업 및 함수에 대해 더 긴 형식의 _별칭_ 으로 약식 이름을 제공 하는 것이 좋을 수 있습니다.

```qsharp
operation CCNOT(control0 : Qubit, control1 : Qubit, target : Qubit)
is Adj + Ctl {
    Controlled X([control0, control1], target);
}
```

# <a name="guidance"></a>[지침](#tab/guidance)

다음을 권장 합니다.

- 적절 한 경우 일반적으로 허용 되 고 널리 사용 되는 약식 이름을 고려 합니다.
- 약어에 대문자를 사용 합니다.
- Short (2 자) 머리글자어 및의 두문자어 정의에 대문자를 사용 합니다.
- `CamelCase`더 긴 (3 자 이상) 머리글자어 및의 두문자어 정의에 사용 합니다.

# <a name="examples"></a>[예](#tab/examples)

|   | 속성 | Description |
|---|------|-------------|
| ☑ | `X` | "$X $ 변환 적용"의 이해 하기 쉬운 약어 |
| ☑ | `CNOT` | "제어-없음"에 대 한 이해 하기 쉬운 약어 |
| ☒ | <s>`Cnot`</s> | 약어는에 사용할 수 없습니다 `CamelCase` . |
| ☑ | `ApplyQft` | 일반적인 initialism "QFT"는 긴 형식 이름의 일부로 표시 됩니다. |
| ☑ | `QFT` | 일반적인 initialism "QFT"는 약식 이름의 일부로 표시 됩니다. |



***


### <a name="proper-nouns-in-names"></a>이름에 적절 한 명사 ###

물리학에는 첫 번째 사람이 게시 한 후 이름을 변경 하는 것이 일반적 이지만 대부분의 비 physicists은 모든 사용자의 이름 및 모든 기록에 대해 잘 알고 있지 않습니다.
다른 배경의 사용자는 일반적인 작업 및 개념을 사용 하기 위해 많은 수의 불투명 한 이름을 알아야 하므로, 물리의 명명 규칙에 너무 많이 의존 하는 것은 매우 중요 한 항목입니다.
<!-- An important part of the task of reducing confusion is to make code more accessible.
Especially in a field such as quantum computing that is rich with domain expertise, we must at all times be cognizant of the demands we place on that expertise as we design quantum software.
In naming code symbols, one way that this cognizance expresses itself is as an awareness of the convention from physics of adopting as the names of algorithms and operations the names of their original publishers.
While we must maintain the history and intellectual provenance of concepts in quantum computing, demanding that all users be versed in this history to use even the most basic of functions and operations places a barrier to entry that is in most cases severe enough to even present an ethical compromise. -->
따라서 개념을 설명 하는 적절 한 일반적인 명사를 개념의 게시 기록을 설명 하는 적절 한 명사에 적용 하는 것이 좋습니다.
특정 한 예로, 단일 제어 교환 및 이중 제어 되지 않는 작업을 교육용 자료에서 "Fredkin" 및 "Toffoli" 작업 이라고 하지만 Q #에서는 주로 및로 식별 됩니다 `CSWAP` `CCNOT` .
두 경우 모두 적절 한 명사와 함께 적절 한 명사를 기반으로 하는 동의어 이름을 제공 합니다.

이 기본 설정은 특히 적절 한 명사를 사용 하는 경우에 특히 중요 합니다. Q #은 다양 한 기존 언어에 의해 설정 된 전통을을 따르고, 예를 들어, `Bool` 부울 논리에 대 한 참조의 형식을 참조 하며,이는 George Boole의 준수에서 이름이 지정 됩니다.
이와 비슷한 몇 가지 퀀텀 개념은 비슷한 방식으로 명명 되며 `Pauli` Q # 언어에 대 한 기본 제공 형식을 포함 합니다.
이러한 사용법이 필수적이 지 않은 적절 한 명사 사용을 최소화 하면 적절 한 명사를 피할 수 없는 영향을 줄일 수 있습니다.

# <a name="guidance"></a>[지침](#tab/guidance) 

다음을 권장 합니다.

- 이름에 적절 한 명사를 사용 하지 마십시오.

# <a name="examples"></a>[예](#tab/examples)

***

### <a name="type-conversions"></a>형식 변환 ###

Q #은 강력 하 고 staticly 지정 된 언어 이기 때문에 형식 변환 함수에 대 한 명시적 호출을 사용 하 여 한 형식의 값을 다른 형식의 값 으로만 사용할 수 있습니다.
이는 값이 암시적으로 (예: 유형 프로 모션) 형식을 변경 하거나 캐스팅을 통해 변경할 수 있는 언어와는 대조적입니다.
따라서 형식 변환 함수는 Q # 라이브러리 개발에서 중요 한 역할을 수행 하 고 명명에 대 한 보다 일반적으로 발생 하는 사항 중 하나를 구성 합니다.
그러나 형식 변환은 항상 _결정적_이므로 함수로 작성 될 수 있으므로 위의 권장 사항 아래에 있습니다.
특히 형식 변환 함수에는 동사 (예:) 또는 부사 prepositional 구 ()로 이름을 지정 하지 않는 것이 좋지만,이 경우에 `ConvertToX` `ToX` 는 소스 및 대상 형식 ()을 나타내는 형용사 prepositional 구로 명명 되어야 합니다 `XAsY` .
형식 변환 함수 이름에 배열 형식을 나열할 때 줄임을 권장 `Arr` 합니다.
예외적인 상황을 제외 하 고,를 사용 하 여 모든 형식 변환 함수 이름을 지정 하 여 신속 하 게 식별할 수 있도록 하는 것이 좋습니다 `As` .

# <a name="guidance"></a>[지침](#tab/guidance)

다음을 권장 합니다.

- 함수가 형식의 값을 형식의 값으로 변환 하는 경우 `X` `Y` 이름 또는을 사용 `AsY` `XAsY` 합니다.

# <a name="examples"></a>[예](#tab/examples)

|   | 속성 | Description |
|---|------|-------------|
| ☒ | <s>`ToDouble`</s> | 전치사 "to"는 동사가 아닌 연산을 나타내는 동사 구를 생성 합니다. |
| ☒ | <s>`AsDouble`</s> | 입력 형식이 함수 이름에서 명확 하지 않습니다. |
| ☒ | <s>`PauliArrFromBoolArr`</s> | 입력 및 출력 형식이 잘못 된 순서로 나타납니다. |
| ☑ | `ResultArrAsBoolArr` | 입력 형식과 출력 형식은 모두 명확 하지 않습니다. |

***

### <a name="private-or-internal-names"></a>개인 또는 내부 이름 ###

대부분의 경우 이름은 라이브러리 또는 프로젝트 내부에서 사용 하기 위한 것 이며 라이브러리에서 제공 하는 API의 보장 된 부분이 아닙니다.
내부 전용 코드에 대 한 실수로 종속성이 명확 하 게 적용 되도록 함수 및 작업의 이름을 지정 하는 경우이를 명확 하 게 표시 하는 것이 좋습니다.
작업 또는 함수가 직접 사용 하기 위한 것이 아니며, 부분 응용 프로그램에서 작동 하는 일치 하는 호출 가능에서 사용 해야 하는 경우에는 부분적으로 `_` 적용 되는 호출 가능에서로 시작 하는 이름을 사용 하는 것이 좋습니다.

# <a name="guidance"></a>[지침](#tab/guidance)

다음을 권장 합니다.

- 함수, 작업 또는 사용자 정의 형식이 Q # 라이브러리 또는 프로그램에 대 한 공용 API의 일부가 아니면 이름이 선행 밑줄 ()로 시작 하는지 확인 `_` 합니다.

# <a name="examples"></a>[예](#tab/examples)

|   | 속성 | Description |
|---|------|-------------|
| ☒ | <s>`ApplyDecomposedOperation_`</s> | 밑줄은 `_` 이름의 끝에 표시 되어서는 안 됩니다. |
| ☑ | `_ApplyDecomposedOperation` | `_`시작 부분에 있는 밑줄은이 작업이 내부용 으로만 사용 됨을 나타냅니다. |

***

### <a name="variants"></a>변형 ###

이후 버전의 Q #에서는이 제한 사항이 유지 되지 않을 수 있지만, 현재는 해당 입력을 함수 하는 것과 관련 된 작업 또는 함수의 그룹이 나 구체적으로 해당 인수의 그룹이 있는 경우가 많습니다.
이러한 그룹은 동일한 루트 이름과 해당 변형을 나타내는 하나 또는 두 개의 문자를 사용 하 여 구분할 수 있습니다.

| 접미사 | 의미 |
|--------|---------|
| `A` | 지원 해야 하는 입력`Adjoint` |
| `C` | 지원 해야 하는 입력`Controlled` |
| `CA` | 입력은 및를 지원 해야 합니다. `Controlled``Adjoint` |
| `I` | 입력 또는 입력은 형식입니다.`Int` |
| `D` | 입력 또는 입력은 형식입니다.`Double` |
| `L` | 입력 또는 입력은 형식입니다.`BigInt` |

# <a name="guidance"></a>[지침](#tab/guidance)

다음을 권장 합니다.

- 함수 또는 작업이 해당 입력의 유형 및 함수 지원에 의해 유사한 함수 또는 작업과 관련이 없는 경우에는 접미사를 사용 하지 마십시오.
- 함수 또는 작업이 해당 입력의 유형 및 함수 지원에 의해 유사한 함수 또는 작업과 관련 된 경우에는 위의 표에서와 같이 접미사를 사용 하 여 변형을 구분 합니다.

# <a name="examples"></a>[예](#tab/examples)

***

### <a name="arguments-and-variables"></a>인수 및 변수 ###

함수 또는 작업에 대 한 Q # 코드의 핵심 목표는 쉽게 읽고 이해할 수 있도록 하는 것입니다.
마찬가지로 입력 및 형식 인수의 이름은 제공 된 후 함수 또는 인수가 사용 되는 방식에 대해 통신 해야 합니다.


# <a name="guidance"></a>[지침](#tab/guidance)

다음을 권장 합니다.

- 모든 변수 및 입력 이름에 대해 `pascalCase` 강력한 기본 설정에서, 또는로를 사용 `CamelCase` `snake_case` `ANGRY_CASE` 합니다.
- 입력 이름은 설명적 이어야 합니다. 가능 하면 하나 또는 두 개의 문자 이름을 사용 하지 마십시오.
- 정확히 하나의 형식 인수를 허용 하는 작업 및 함수는 `T` 해당 역할이 명확 하 게 될 때에서 해당 형식 인수를 나타냅니다.
- 함수 또는 작업에서 여러 형식 인수를 사용 하거나 단일 형식 인수의 역할이 명확 하지 않은 경우 각 형식에 대해 앞에 오는 짧은 대문자 단어 `T` (예:)를 사용 하는 것이 좋습니다 `TOutput` .
- 인수 및 변수 이름에 형식 이름을 포함 하지 마십시오. 이 정보는 개발 환경에서 제공 해야 합니다.
- 리터럴 이름 ( `flagQubit` ) 및 배열 형식 ()으로 스칼라 형식을 나타냅니다 `measResults` .
  구체적 비트 배열의 경우에는 `Register` 이름이 특정 방식으로 밀접 하 게 관련 된 다양 한 비트 시퀀스를 참조 하는 방식으로 이러한 형식을 나타내는 것이 좋습니다.
- 배열로 인덱스로 사용 되는 변수는로 시작 해야 `idx` 하며 단수형 (예:) 이어야 합니다. `things[idxThing]`
  특히 단일 문자 변수 이름을 인덱스로 사용 하지 않는 것이 좋습니다. `idx`최소한을 사용 하십시오.
- 배열의 길이를 포함 하는 데 사용 되는 변수는로 시작 해야 `n` 하 고 복수화 해야 합니다 (예: `nThings` ).

# <a name="examples"></a>[예](#tab/examples)

***

### <a name="user-defined-type-named-items"></a>사용자 정의 형식 항목 ###

사용자 정의 형식의 명명 된 항목은 `CamelCase` UDT 생성자에 대 한 입력으로도로 이름을 지정 해야 합니다.
이를 통해 접근자 표기법 (예: `callable::Apply` ) 또는 복사 및 업데이트 표기법 ()을 사용할 때 명명 된 항목을 지역 범위 변수에 대 한 참조에서 명확 하 게 구분할 수 있습니다. `set arr w/= Data <- newData`

# <a name="guidance"></a>[지침](#tab/guidance)

다음을 권장 합니다.

- UDT 생성자의 명명 된 항목 이름은로 지정 해야 합니다. `CamelCase` 즉, 초기 대문자로 시작 해야 합니다.
- 작업으로 확인 되는 명명 된 항목은 동사 단계로 명명 되어야 합니다.
- 작업을 확인 하지 않는 명명 된 항목은 명사 구로 명명 되어야 합니다.
- 작업을 래핑하는 Udt의 경우 라는 이름의 단일 항목을 `Apply` 정의 해야 합니다.

# <a name="examples"></a>[예](#tab/examples)

|   | 코드 조각 | Description |
|---|---------|-------------|
| ☑ | `newtype Oracle = (Apply : Qubit[] => Unit is Adj + Ctl)` | 이름은 `Apply` `CamelCase` 형식이 지정 된 동사 구로, 명명 된 항목이 작업 임을 제안 합니다. |
| ☒ | <s>`newtype Oracle = (apply : Qubit[] => Unit is Adj + Ctl) `</s> | 명명 된 항목은 초기 대문자로 시작 해야 합니다. |
| ☒ | <s>`newtype Collection = (Length : Int, Get : Int -> (Qubit => Unit)) `</s> | 함수를 확인 하는 명명 된 항목은 동사 구가 아닌 명사 구로 명명 되어야 합니다. |

***

## <a name="input-conventions"></a>입력 규칙 ##

개발자가 작업 또는 함수를 호출 하는 경우 해당 작업 또는 함수에 대 한 다양 한 입력을 특정 순서로 지정 하 여 개발자가 라이브러리를 사용 하기 위해 직면 하 게 되는 인지 부하를 늘려야 합니다.
특히 입력 순서 기억 하는 작업은 일반적으로 퀀텀 알고리즘의 구현 프로그래밍의 작업에서 혼란 스 러가 됩니다.
풍부한 IDE 지원으로 인해이를 매우 광범위 하 게 완화할 수 있지만 일반적인 규칙을 잘 설계 하 고 준수 하는 것은 API에 의해 적용 되는 인지 부하를 최소화 하는 데도 도움이 될 수 있습니다.

가능 하면 작업이 나 함수에 필요한 입력 수를 줄이는 것이 도움이 될 수 있습니다. 그러면 각 입력의 역할이 해당 작업 또는 함수를 호출 하는 개발자와 나중에 해당 코드를 읽는 개발자에 게 더 즉각적으로 표시 됩니다.
특히 작업이 나 함수에 대 한 인수 수를 줄이는 것이 불가능 하거나 적절 하지 않은 경우 입력 순서를 예측할 때 사용자가 직면 하는 갑작스러운 요소를 최소화 하는 일관 된 순서를 지정 하는 것이 중요 합니다.

Currying f (x, y) ≡ f (x) (y)의 일반화로 부분 응용 프로그램의 생각에서 주로 파생 되는 입력 순서 지정 규칙을 권장 합니다.
따라서 첫 번째 인수를 부분적으로 적용 하면 적절 한 경우 항상 적절 한 권한으로 사용할 수 있는 호출 가능이 발생 합니다.
이 원칙에 따라 다음과 같은 인수 순서를 사용 하는 것이 좋습니다.

- 각도, 거듭제곱 벡터 등의 호출 가능 하지 않은 클래식 인수
- 호출 가능 인수 (함수 및 인수)
  함수와 연산이 모두 인수로 사용 되는 경우 함수 뒤에 작업을 배치 하는 것이 좋습니다.
- ,, 및와 비슷한 방식으로 호출 가능한 인수에 의해 처리 된 컬렉션 `Map` `Iter` `Enumerate` `Fold` 입니다.
- 컨트롤로 사용 되는 인수입니다.
- 대상으로 사용 되는 인수입니다.

`ApplyPhaseEstimationIteration`각도와 oracle을 사용 하는 단계 추정에서 사용 하기 위한 작업을 고려 하 고, `Rz` 다른 배율 인수 배열에 의해 수정 된 각도를 전달한 다음 oracle의 응용 프로그램을 제어 합니다.
입력은 `ApplyPhaseEstimationIteration` 다음과 같은 방식으로 정렬 됩니다.

```qsharp
operation ApplyPhaseEstimationIteration(
    angle : Double,
    callable : (Qubit => () is Ctl),
    scaleFactors : Double[],
    controlQubit : Qubit,
    targetQubits : Qubit[]
)
: Unit
...
```
갑작스러운 문제를 최소화 하는 특별 한 경우에는 일부 함수 및 작업이 기본 제공 함수 및의 동작을 모방 합니다 `Adjoint` `Controlled` .
예를 들어,에는 `ControlledOnInt<'T>` `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)` `ControlledOnInt<Qubit[]>(5, _)` 함수 처럼 작동 `Controlled` 하지만 컨트롤 레지스터가 상태 $ \ket {5} = \ket $를 나타내는 조건의 {101} 형식이 있습니다.
따라서 개발자는 호출 되는 호출을 마지막으로 변환 하는 입력을 예상 하 `ControlledOnInt` 고 그 `(Qubit[], 'T)` 다음에 함수 출력을 사용 하는 것과 동일한 순서로 결과 작업을 입력---합니다 `Controlled` .

# <a name="guidance"></a>[지침](#tab/guidance)

다음을 권장 합니다.

- 부분 응용 프로그램을 사용 하는 경우 입력 순서 일치를 사용 합니다.
- 기본 제공 함수와 일치 하는 입력 순서을 사용 합니다.
- 모든 기존 입력을 퀀텀 입력 앞에 저장 합니다.

# <a name="examples"></a>[예](#tab/examples)

***

## <a name="documentation-conventions"></a>설명서 표기 규칙 ##

Q # 언어를 사용 하면 특수 형식의 문서 주석을 사용 하 여 작업, 함수 및 사용자 정의 형식에 대 한 설명서를 첨부할 수 있습니다.
삼중 슬래시 ()로 표시 되는 `///` 이러한 설명서 주석은 각 작업, 함수 및 사용자 정의 형식, 각 작업의 용도를 설명 하는 데 사용할 수 있는 작은 [docfx-flavored Markdown](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) 문서입니다.
퀀텀 개발 키트와 함께 제공 되는 컴파일러는 이러한 주석을 추출 하 고이를 사용 하 여와 비슷한 조판 설명서를 제공 https://docs.microsoft.com/quantum 합니다.
마찬가지로, 퀀텀 개발 키트와 함께 제공 되는 언어 서버는 이러한 주석을 사용 하 여 사용자가 Q # 코드에서 기호를 마우스로 가리킬 때 사용자에 게 도움을 제공 합니다.
따라서 문서 주석을 사용 하면이 문서의 다른 규칙을 사용 하 여 쉽게 표현 되지 않는 세부 정보에 대 한 유용한 참조를 제공 하 여 사용자가 코드를 이해 하는 데 도움이 될 수 있습니다.

<div class="nextstepaction">
    [문서 주석 구문 참조](xref:microsoft.quantum.guide.filestructure#documentation-comments)
</div>

이 기능을 효과적으로 사용 하 여 사용자를 돕기 위해 문서 주석을 작성할 때 몇 가지 사항을 염두에 두어야 합니다.

# <a name="guidance"></a>[지침](#tab/guidance)

다음을 권장 합니다.

- 각 public 함수, 작업 및 사용자 정의 형식은 문서 주석 바로 앞에와 야 합니다.
- 최소한 각 문서 주석에는 다음 섹션이 포함 되어 있어야 합니다.
    - 요약
    - 입력
    - 출력 (해당 하는 경우)
- 모든 요약이 두 문장 이내 인지 확인 합니다. 더 많은 공간이 필요한 경우 `# Description` `# Summary` 전체 세부 정보를 사용 하 여 바로 다음 섹션을 제공 하세요.
- 모든 클라이언트에서 요약에 TeX 표기법을 지 원하는 것이 아니라 적절 한 경우 요약에 수학을 포함 하지 마세요. Prose 문서를 작성 하는 경우 (예: TeX 또는 Markdown) 더 긴 줄 길이를 사용 하는 것이 더 적합할 수 있습니다.
- 섹션에서 관련 된 모든 수학 식을 제공 `# Description` 합니다.
- 입력을 설명할 때 컴파일러에서 유추할 수 있는 각 입력의 형식과 불일치를 발생 하는 위험을 반복 해 서는 안 됩니다.
- 각각의 고유한 섹션에서 적절 한 예제를 제공 `# Example` 합니다.
- 코드를 나열 하기 전에 각 예제를 간략하게 설명 합니다.
- 섹션에서 관련 된 모든 교육용 게시 (예: 용지, proceedings of the, 블로그 게시물 및 대체 구현)를 `# References` 링크의 글머리 기호 목록으로 인용 합니다.
- 가능 하면 모든 인용 링크가 영구적이 고 변경할 수 없는 식별자 (DOIs 또는 버전이 지정 된 arXiv 번호)에 해당 하는지 확인 합니다.
- 작업 또는 함수가 함수 변형에 의해 다른 작업 또는 함수와 관련 된 경우 섹션에서 다른 변형을 글머리 기호로 나열 `# See Also` 합니다.
- 수준-1 () 섹션 사이에 빈 주석 줄을 그대로 두고 `/// #` 수준-2 () 섹션 사이에 빈 줄을 남겨 둡니다 `/// ##` .

# <a name="examples"></a>[예](#tab/examples)

#### <a name=""></a>☑ ####

```
/// # Summary
/// Applies a rotation about the X-axis by a given angle.
///
///
/// # Description
/// This operation rotates a single qubit by the unitary operation
/// \begin{align}
///     R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2}.
/// \end{align}
///
/// # Input
/// ## theta
/// Angle about which the qubit is to be rotated.
/// ## qubit
/// Qubit to which the gate should be applied.
///
/// # Remarks
/// Equivalent to:
/// ```qsharp
/// R(PauliX, theta, qubit);
/// ```
///
/// # See Also
/// - Ry
/// - Rz
operation Rx(theta : Double, qubit : Qubit) : Unit
is Adj + Ctl {
    body (...) { R(PauliX, theta, qubit); }
    adjoint (...) { R(PauliX, -theta, qubit); }
}
```

***

## <a name="formatting-conventions"></a>서식 지정 규칙 ##

앞의 제안 사항 외에도 일관 된 서식 지정 규칙을 사용 하는 코드를 가능한 한 이해 하기 쉽게 만드는 데 도움이 됩니다.
이러한 서식 지정 규칙은 본질적으로 임의로 임의적 이며 개인용 미관에 게 매우 강력 합니다.
그럼에도 불구 하 고 작업자 그룹 내에 일관 된 형식 지정 규칙 집합을 유지 하는 것이 좋습니다. 특히 퀀텀 개발 키트와 같은 초대형 Q # 프로젝트의 경우에는 특히 그렇습니다.
이러한 규칙은 Q # 컴파일러와 통합 된 서식 도구를 사용 하 여 자동으로 적용할 수 있습니다.

# <a name="guidance"></a>[지침](#tab/guidance) 

다음을 권장 합니다.

- 이식성을 위해 탭 대신 4 개의 공백을 사용 합니다.
  예를 들어 VS Code에서 다음을 수행 합니다.
  ```json
    "editor.insertSpaces": true,
    "editor.tabSize": 4
  ```
- 줄 바꿈이 적당 한 79 문자입니다.
- 이항 연산자 주위의 공백을 사용 합니다.
- 형식 주석에 사용 되는 콜론의 양쪽에 공백을 사용 합니다.
- 배열 및 튜플 리터럴 (예: 함수 및 작업에 대 한 입력)에서 쉼표 뒤에 사용 되는 단일 공백을 사용 합니다.
- 함수, 작업 또는 UDT 이름 뒤에 공백을 사용 하거나 in 특성 선언 뒤에 공백을 사용 하지 마십시오 `@` .
- 각 특성 선언은 별도의 줄에 있어야 합니다.

# <a name="examples"></a>[예](#tab/examples)

|   | 코드 조각 | Description |
|---|---------|-------------|
| ☒ | <s>`2+3`</s> | 이항 연산자 주위의 공백을 사용 합니다. |
| ☒ | <s>`target:Qubit`</s> | 형식 주석 콜론 앞뒤에 공백을 사용 합니다. |
| ☑ | `Example(a, b, c)` | 입력 튜플의 항목은 가독성을 위해 정확 하 게 배치 됩니다. |
| ☒ | <s>`Example (a, b, c)`</s> | 함수, 작업 또는 UDT 이름 뒤에는 공백을 표시 하지 않아야 합니다. |

***

