---
title: Q#기본 사항
description: 의 기본 개념Q#
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 02/28/2020
ms.topic: article
uid: microsoft.quantum.guide.basics
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4f4a75cdaaa070fd763d7f75429b7c39357d25a5
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869650"
---
# <a name="no-locq-basics"></a>Q#기본 사항

이 문서에서는의 기본 구성 요소에 대 한 간략 한 소개를 제공 Q# 합니다.

에 대 한 개요 Q# 와 퀀텀 개발 키트의 기본 구성 요소로 사용할 수 있는 위치에 대 한 개요는 [무엇 Q# 인가요?](xref:microsoft.quantum.overview.q-sharp)를 참조 하세요. 

## <a name="what-is-a-quantum-program"></a>퀀텀 프로그램 이란?

기술적 측면에서 퀀텀 프로그램은 호출 시 퀀텀 시스템에서 특정 작업을 수행 하는 특별 한 특정 서브루틴 집합입니다.
이 보기의 중요 한 결과는 프로그램에서 Q# 직접 직접 모델링 하지 않고 일반적으로 제어 컴퓨터가 해당 하는 비트와 상호 작용 하는 방식을 설명 하는 것입니다.
의도적으로는 퀀텀 Q# 상태 또는 퀀텀 메커니즘의 다른 속성을 직접 정의 하지 않습니다.
예를 들어 퀀텀 컴퓨팅 개념 가이드에 설명 된 $ \ket{+} = \left (\ket {0} + \ket {1} \left)/\left {2} $ [Quantum Computing Concepts](xref:microsoft.quantum.concepts.intro) 상태를 고려 합니다.
에서이 상태를 준비 하려면 Q# 먼저 $ \ket $ 상태에서이를 초기화 하 {0} 고 $ \ket{+} = H\ket {0} $를 사용 합니다. 여기서 $H $은 [ `H` 작업](xref:microsoft.quantum.intrinsic.h)에 의해 구현 되는 [Hadamard 변환](xref:microsoft.quantum.glossary#hadamard)입니다. 을 Q# 초기화 하 고이를 변환 하는 기본 코드는 다음과 같습니다.

```qsharp
using (qubit = Qubit()) {
    // At this point, the qubit is in the state |0⟩.
    H(qubit);
    // H is now applied, such that the qubit is in H|0⟩ = |+⟩, as desired.
}
```
을 초기화 하거나 *할당*하는 방법에 대 한 자세한 내용은 [작업](xref:microsoft.quantum.guide.qubits)을 참조 하세요.

## <a name="quantum-states-in-no-locq"></a>퀀텀 상태Q#

중요 한 점은 이전 프로그램은 내에서 상태를 명시적으로 참조 하지 Q# 않지만 프로그램이 상태를 *변환* 하는 방법을 설명 했습니다.
이 접근 방식을 사용 하면 각 대상 컴퓨터 *에도 있는 퀀텀 상태를 완전히* 제어할 수 없으며, 컴퓨터에 따라 서로 다른 해석이 있을 수 있습니다. 

Q#프로그램은 introspect의 상태로 전환 될 수 없습니다.
대신, 프로그램은 등의 작업을 호출 하 여이를 [`Measure`](xref:microsoft.quantum.intrinsic.measure) 통해 정보를 파악 하 고, 등의 작업을 호출 하 여 해당 [`X`](xref:microsoft.quantum.intrinsic.x) 상태에 대 한 작업을 수행할 수 있습니다 [`H`](xref:microsoft.quantum.intrinsic.h) .
이러한 작업은 실제로 *수행* 하는 작업은 특정 프로그램을 실행 하는 데 사용 되는 대상 컴퓨터에 의해서만 구체적으로 적용 됩니다 Q# .
예를 들어 [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)에서 프로그램을 실행 하는 경우 시뮬레이터는 시뮬레이션 된 퀀텀 시스템에 해당 하는 수치 연산을 수행 합니다.
하지만 나중에 대상 컴퓨터가 실제 퀀텀 컴퓨터인 경우에서 이러한 작업을 호출 하면 Q# *실제* 퀀텀 시스템에서 해당 하는 *실제* 작업을 수행 하도록 퀀텀 컴퓨터가 지시 합니다 (예: 정확히 시간이 지정 된 레이저 펄스).

Q#프로그램은 대상 컴퓨터에서 정의한 대로 이러한 작업을 다시 결합 하 여 퀀텀 계산을 표현할 수 있는 새로운 수준의 새 작업을 만듭니다.
이러한 방식으로를 사용 하면 Q# 대상 컴퓨터 또는 시뮬레이터의 구조와 관련 하 여 일반적으로 사용 되는 논리 퀀텀 및 하이브리드 퀀텀 – 기존 알고리즘을 쉽게 표현할 수 있습니다.

## <a name="no-locq-operations-and-functions"></a>Q#작업 및 함수

구체적으로 프로그램은 Q# *작업*, *함수*및 사용자 정의 형식으로 구성 됩니다. 

작업은 퀀텀 시스템의 변환을 설명 하는 데 사용 되며 가장 기본적인 프로그램 구성 요소입니다 Q# . 에서 정의 된 각 작업 Q# 은 다른 작업을 원하는 수 만큼 호출할 수 있습니다.

연산과는 달리 함수는 순수 하 게 *결정적인* 클래식 동작을 설명 하는 데 사용 되며, 기존 값을 계산 하는 것 외에는 영향을 주지 않습니다. 예를 들어 프로그램의 끝에서 원하는 비트를 측정 하 고 배열에 측정 결과를 추가 한다고 가정 합니다.
이 경우 `Measure` 는 대상 컴퓨터에서 (실제 또는 시뮬레이트된)의 측정을 수행 하도록 지시 하는 *작업* 입니다. 동시에 *함수* 는 반환 된 결과를 배열에 추가 하는 기존 프로세스를 처리 합니다.

작업 및 함수를 함께 *callables*이라고 합니다. 의 기본 구조와 동작은 [의 Q# 작업 및 함수 ](xref:microsoft.quantum.guide.operationsfunctions)에서 도입 되 고 자세히 설명 합니다.


## <a name="no-locq-syntax-overview"></a>Q#구문 개요

언어의 구문은 구문상 올바른 프로그램을 구성 하는 기호의 여러 조합을 설명 합니다.
에서 Q# 구문 요소는 형식, 식 및 문과 같은 세 가지 그룹으로 분류 됩니다.

### <a name="types"></a>유형
Q#는 강력한 형식의 언어 이며, 신중 하 게 형식을 사용 하면 컴파일러가 Q# 컴파일 시간에 프로그램에 대 한 강력한 보증을 제공할 수 있습니다.
표준 및 퀀텀 관련 기본 제공 기본 형식 (예:,, 및) 외에 `Int` 도 `Bool` `Qubit` `Result` Q# 사용자 정의 형식에 대 한 지원을 제공 합니다.

모든 기본 형식, 배열 및 튜플 형식에 대 한 자세한 내용 및 파일 내에 새 형식을 정의 하는 단계에 대 한 설명은 Q# [의 Q# 형식 ](xref:microsoft.quantum.guide.types)을 참조 하세요.

### <a name="expressions"></a>표현식
프로그래밍 언어의 식은 프로그래밍 언어가 해석 하 고 특정 값으로 평가 하는 하나 이상의 상수, 변수, 연산자 및 함수의 조합입니다.
대부분의 경우 언어의 모든 형식에 대해 해당 형식의 식은 해당 형식의 값에 바인딩된 *리터럴* 또는 기호 중 하나일 수 있습니다.
예를 들어 `5` 는 `Int` 리터럴 (따라서 형식의 식 `Int` )이 고 기호가 `count` 정수 값에 바인딩되면는 `5` `count` 정수 식 이기도 합니다.

또한 식은 특정 연산자에 의해 결합 된 다른 식으로 구성 될 수 있습니다.
예를 들어 `Int` 로 계산 되는 다른 식은입니다 `5` `2+3` .

의 식 및 호환 연산자에 대 한 자세한 내용은 Q# [의 Q# 형식 식 ](xref:microsoft.quantum.guide.expressions)을 참조 하세요. 

### <a name="statements"></a>문 
문은 수행할 작업을 표현 하는 명령형 프로그래밍 언어의 구문 단위입니다. 문에 있는 식과의 대조는 결과를 반환 하지 않으며 의도 하지 않은 결과에 대해서만 실행 됩니다. 그러나 식은 항상 결과를 반환 하며 부작용이 없는 경우가 많습니다. 즉, Q# 식이 계산 되는 동안 문이 실행 됩니다.

에서 문의 간단한 예는 Q# 식에 기호를 할당 하는 것입니다.
```qsharp
let count = 5;
```

더 흥미로운 예는 반복을 `for` 지원 하 고 *문 블록*을 포함 하는 문입니다.
`qubits`는 (기술적으로는 형식 또는 형식의 배열인)의 레지스터에 바인딩된 기호가 있다고 가정 `Qubit[]` `Qubit` 합니다. 결과
```qsharp
for (qubit in qubits) {
    H(qubit);
}
```
는 레지스터의 각 비트를 반복 하 여 `H` 각각에 대해 작업을 수행 하는 문입니다. 는 `H(qubit);` 자체의 문입니다.

형식 `Unit` (정보를 반환 하지 않는 형식)의 호출 식을 문으로 사용할 수 있습니다 `Unit` .
이 식 형식은 `Unit` 문의 목적이 암시적 퀀텀 상태를 수정 하기 때문에를 반환 하는 작업을 호출 하는 경우에 유용 합니다.
식 계산 문에는 종료 세미콜론이 필요 합니다.

문을 사용 하 여 프로그램의 거의 모든 측면을 빌드할 수 Q# 있으며, 모든 정보를 포함 하는 모든 정보는 단일 페이지에 포함 될 수 없습니다.
해당 어휘 구조 및 서식에 대 한 자세한 내용은 [ Q# 파일 구조](xref:microsoft.quantum.guide.filestructure), 기호 바인딩 할당 및 범위에 대 한 자세한 내용은 [의 Q# 변수 ](xref:microsoft.quantum.guide.variables)를 참조 하 고,와 같은 제어 흐름 루프의 `for` 경우 [ Q# 제어 흐름 ](xref:microsoft.quantum.guide.controlflow)을 참조 하세요.

## <a name="next-steps"></a>다음 단계

[의 형식 Q# ](xref:microsoft.quantum.guide.types)에 대 한 학습을 시작 합니다.

기반이 되는 것과 그에 대 한 자세한 배경 정보는 Q# [왜 필요 Q# 합니까?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/)를 참조 하세요.
