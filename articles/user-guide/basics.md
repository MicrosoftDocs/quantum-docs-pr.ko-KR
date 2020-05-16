---
title: 'Q # 기본 사항'
description: 'Q의 기본 개념 #'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 02/28/2020
ms.topic: article
uid: microsoft.quantum.guide.basics
ms.openlocfilehash: fd0ea47f00b1456ec460808ef7d451c8427677cd
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431158"
---
# <a name="q-basics"></a>Q # 기본 사항

이 섹션에서는 Q #의 기본 구성 요소에 대 한 간략 한 소개를 제공 합니다.

Q #가 무엇 인지와 이러한 항목이 퀀텀 개발 키트의 기본 구성 요소로 적합 한지에 대 한 간략 한 개요는 [q #?를](xref:microsoft.quantum.overview.q-sharp)확인할 수 있습니다. 

## <a name="what-is-a-quantum-program"></a>퀀텀 프로그램 이란?

기술적 측면에서 볼 때 퀀텀 프로그램은 특정 한 기존 서브루틴 집합으로 볼 수 있습니다 .이를 호출 하면 퀀텀 시스템에서 특정 작업을 수행할 수 있습니다.
이 보기의 중요 한 결과는 Q #으로 작성 된 프로그램이 직접 직접 모델을 모델링 하는 것이 아니라 클래식 제어 컴퓨터가 해당 하는 비트와 상호 작용 하는 방식을 설명 하는 것입니다.
따라서 Q #은 기본적으로 퀀텀 상태 또는 퀀텀 메커니즘의 다른 속성을 직접 정의 하지 않습니다.
예를 들어 퀀텀 컴퓨팅 개념 가이드에 설명 된 $ \ket{+} = \left (\ket {0} + \ket {1} \left)/\left {2} $ [Quantum Computing Concepts](xref:microsoft.quantum.concepts.intro) 상태를 고려 합니다.
Q #에서이 상태를 준비 하기 위해 $ \ket $ 상태에서이 상태를 초기화 하는 팩트와 $ {0} \ket{+} = H\ket {0} $를 사용 합니다. 여기서 $H $은 [ `H` operation] (] (f:)에 의해 구현 된 Hadamard 변환입니다.

```qsharp
using (qubit = Qubit()) {
    // At this point, qubit is in the state |0⟩.
    H(qubit);
    // We've now applied H, such that our qubit is in H|0⟩ = |+⟩, as we wanted.
}
```

## <a name="quantum-states-in-q"></a>Q의 퀀텀 상태 #

중요 한 점은 위의 프로그램을 작성할 때 Q # 내에서 상태를 명시적으로 참조 하지 않고 프로그램에서 상태를 *변환* 하는 방법을 설명 하는 것입니다.
이를 통해 각 대상 컴퓨터 *에도 있는 퀀텀 상태를 완전히* 제어할 수 있으며,이는 컴퓨터에 따라 서로 다르게 해석 될 수 있습니다. 

Q # 프로그램에는 introspect의 상태로 전환 하는 기능이 없습니다.
대신, 프로그램은 등의 작업을 호출 하 여이를 [`Measure`](xref:microsoft.quantum.intrinsic.measure) 통해 정보를 파악 하 고, 등의 작업을 호출 하 여 해당 [`X`](xref:microsoft.quantum.intrinsic.x) 상태에 대 한 작업을 수행할 수 있습니다 [`H`](xref:microsoft.quantum.intrinsic.h) .
이러한 작업은 실제로 *수행* 하는 작업은 특정 Q # 프로그램을 실행 하는 데 사용 하는 대상 컴퓨터에만 구체적으로 적용 됩니다.
예를 들어 [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)에서 프로그램을 실행 하는 경우 시뮬레이터는 시뮬레이션 된 퀀텀 시스템에 해당 하는 수학적 작업을 수행 합니다.
하지만 향후에는 대상 컴퓨터가 실제 퀀텀 컴퓨터인 경우 Q #에서 이러한 작업을 호출 하면 *실제* 퀀텀 시스템에서 해당 하는 *실제* 작업을 수행 하도록 퀀텀 컴퓨터가 지시 합니다 (예: 정확히 시간이 지정 된 레이저 펄스).

Q # 프로그램은 대상 컴퓨터에서 정의한 대로 이러한 작업을 다시 결합 하 여 퀀텀 계산을 표현할 수 있는 새로운 수준의 새 작업을 만듭니다.
이러한 방식으로 Q #를 사용 하면 대상 컴퓨터 또는 시뮬레이터의 구조와 관련 하 여 일반적으로 사용 되는 논리 퀀텀 및 하이브리드 퀀텀 – 기존 알고리즘을 쉽게 표현할 수 있습니다.

## <a name="q-operations-and-functions"></a>Q # 작업 및 함수

구체적으로 Q # 프로그램은 *작업*, *함수*및 사용자 정의 형식으로 구성 됩니다. 

작업은 퀀텀 시스템의 변환을 설명 하는 데 사용 되며 Q # 프로그램의 가장 기본적인 구성 요소입니다. Q #에 정의 된 각 작업은 원하는 수 만큼 다른 작업을 호출할 수 있습니다.

연산과는 달리 함수는 순수 하 게 *결정적인* 클래식 동작을 설명 하는 데 사용 되며, 기존 값을 계산 하는 것 외에는 영향을 주지 않습니다. 예를 들어, 프로그램의 끝에서 원하는 비트를 측정 하 고 배열에 측정 결과를 추가 한다고 가정 합니다.
이 경우 `Measure` 대상 컴퓨터에서 (real 또는 시뮬레이션 된)의 측정을 수행 하도록 지시 하는 *연산이* 며 반환 된 결과를 배열에 추가 하는 기존 프로세스는 *함수*에 의해 처리 됩니다.

작업 및 함수를 함께 *callables*이라고 하며, [Q # 페이지의 작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions) 에 해당 기본 구조 및 동작이 도입 되었습니다.


## <a name="q-syntax-overview"></a>Q # 구문 개요

언어의 구문은 구문상 올바른 프로그램을 구성 하는 기호의 여러 조합을 설명 합니다.
Q #에서는 형식, 식 및 문과 같은 세 가지 그룹의 구문 요소를 분류할 수 있습니다.

### <a name="types"></a>형식
Q #은 강력한 형식의 언어 이며, 신중 하 게 형식을 사용 하면 컴파일러가 컴파일 시간에 Q # 프로그램에 대 한 강력한 보증을 제공 하는 데 도움이 될 수 있습니다.
표준 및 퀀텀 관련 기본 제공 기본 형식 (예:,, `Int` 및) 외에 `Bool` 도 `Qubit` `Result` Q #에서는 사용자 정의 형식에 대 한 지원을 제공 합니다.
Q #의 다양 한 기본 형식은 q # 페이지의 [형식](xref:microsoft.quantum.guide.types) , 배열 및 튜플 형식에 대 한 세부 정보 및 q # 파일 내에 새 형식을 정의 하는 방법에 설명 되어 있습니다.

### <a name="expressions"></a>식
프로그래밍 언어의 식은 프로그래밍 언어가 해석 하 고 특정 값으로 평가 하는 하나 이상의 상수, 변수, 연산자 및 함수의 조합입니다.
대부분의 경우 언어의 모든 형식에 대해 해당 형식의 식은 해당 형식의 값에 바인딩된 *리터럴* 또는 기호 중 하나일 수 있습니다.
예를 들어 `5` 는 `Int` 리터럴 (따라서 형식의 식 `Int` )이 고 기호가 `count` 정수 값에 바인딩되면는 `5` `count` 정수 식 이기도 합니다.

또한 식은 특정 연산자와 결합 된 다른 식으로 구성 될 수 있습니다.
따라서로 계산 되는 식의 또 다른 예 `Int` `5` 는입니다 `2+3` .

Q #에서 가능한 형식의 가능한 식과 이러한 연산자를 구성 하는 데 사용할 수 있는 호환 연산자는 [q # 페이지의 형식 식](xref:microsoft.quantum.guide.expressions) 에 자세히 설명 되어 있습니다. 

### <a name="statements"></a>문 
문은 수행할 작업을 표현 하는 명령형 프로그래밍 언어의 구문 단위입니다. 문은 결과를 반환 하지 않고 그 파생 작업에 대해서만 실행 되는 반면 식은 항상 결과를 반환 하며 부작용이 전혀 없는 경우가 많습니다.
이러한 구분은 일반적으로 식이 계산 되는 반면 문이 실행 되는 경우에 자주 관찰 됩니다.

Q #에 있는 문의 기본 예는 식에 기호를 할당 하는 것입니다.
```qsharp
let count = 5;
```

약간 더 흥미로운 예는 반복을 `for` 지원 하 고 *문 블록*을 포함 하는 문입니다.
이 경우에 `qubits` 는 (형식 `Qubit[]` , 즉 형식의 배열)의 레지스터에 바인딩된 기호가 있다고 가정 합니다 `Qubit` . 결과
```qsharp
for (qubit in qubits) {
    H(qubit);
}
```
는 레지스터에서 각의 각 비트를 반복 하 여 `H` 각각에 대해 작업을 수행 하는 문입니다. 는 `H(qubit);` 자체의 문입니다.

실제로 형식의 호출 식 `Unit` (정보를 반환 하지 않는 callables)은 문으로 사용 될 수 있습니다.
이는 `Unit` 문의 목적이 암시적 퀀텀 상태를 수정 하기 때문에를 반환 하는 stbits에 대 한 작업을 호출할 때 주로 사용 됩니다.
식 계산 문에는 종료 세미콜론이 필요 합니다.

Q # 프로그램의 거의 모든 측면은 문을 사용 하 여 작성 되므로 단일 페이지에 관련 된 모든 정보가 포함 되지 않을 수 있습니다.
그러나 해당 어휘 구조와 서식 지정은 q # [파일 구조](xref:microsoft.quantum.guide.filestructure) 페이지, [q #의 변수](xref:microsoft.quantum.guide.variables)에서 기호 바인딩 할당 및 범위, q `for` #의 [제어 흐름](xref:microsoft.quantum.guide.controlflow)등의 제어 흐름 루프에 설명 되어 있습니다.


## <a name="whats-next"></a>새로운 기능
이 가이드의 나머지 부분에서는 Q #을 사용 하 여 작업, 함수 및 형식의 기본 구성 요소를 통해 복잡 한 퀀텀 프로그램을 생성 하는 방법을 보여 줍니다.

시작 하려면 [Q #에서 형식](xref:microsoft.quantum.guide.types)에 대 한 학습을 시작할 수 있습니다.

Q #의 기초 및 동기에 대해 자세히 알아보려면 [q #?가 필요한 이유](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/)를 확인 하세요.
