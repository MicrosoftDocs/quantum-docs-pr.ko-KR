---
title: 양자 난수 생성기 만들기
description: 양자 난수 생성기를 만들어서 중첩 같은 기본적인 양자 개념을 보여주는 Q# 프로젝트를 빌드합니다.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: a7c077eda3e46430cbe6598cb899adb460451f75
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2019
ms.locfileid: "73443922"
---
# <a name="quickstart-implement-a-quantum-random-number-generator-in-q"></a>빠른 시작: Q#에서 양자 난수 생성기 구현
Q#으로 양자 난수 생성기를 작성하는 간단한 양자 알고리즘 예제입니다. 이 알고리즘은 양자 메커니즘의 특성을 활용하여 난수를 생성합니다. 

## <a name="prerequisites"></a>필수 조건

- Microsoft [Quantum Development Kit](xref:microsoft.quantum.install)
- [Q# 프로젝트 만들기](xref:microsoft.quantum.howto.createproject)


## <a name="write-a-q-operation"></a>Q# 연산 작성

### <a name="q-operation-code"></a>Q# 연산 코드

1. Operation.qs 파일의 내용을 다음 코드로 바꿉니다.

    ```qsharp
    namespace Quantum {
        open Microsoft.Quantum.Intrinsic;

        operation QuantumRandomNumberGenerator() : Result {
            using(q = Qubit())  { // Allocate a qubit.
                H(q);             // Put the qubit to superposition. It now has a 50% chance of being 0 or 1.
                let r = M(q);     // Measure the qubit value.
                Reset(q);
                return r;
            }
        }
    }
    ```

[양자 컴퓨팅이란?](xref:microsoft.quantum.overview.what) 문서에서 언급했듯이, 큐비트는 중첩에 있을 수 있는 양자 정보의 단위입니다. 측정된 큐비트는 0 또는 1 중 하나만 될 수 있습니다. 하지만 실행 중인 동안 큐비트 상태는 측정값이 0 또는 1일 수 있는 확률을 나타냅니다. 이 확률적 상태를 중첩이라고 합니다. 이 확률을 사용하여 난수를 생성할 수 있습니다.

Q# 연산에서는 Q#의 기본 형식인 `Qubit` 데이터 형식을 도입합니다. `Qubit`는 `using` 문으로만 할당할 수 있습니다. 할당된 큐비트는 항상 `Zero` 상태입니다. 

`H` 연산을 사용하여 `Qubit`를 중첩 상태로 전환할 수 있습니다. 큐비트를 측정하고 값을 읽으려면 `M` 내장 연산을 사용합니다.

`Qubit`를 중첩 상태로 전환하고 측정하면 코드가 호출될 때마다 다른 값이 반환됩니다. 

`Qubit`를 할당 취소하면 큐비트가 명시적으로 다시 `Zero` 상태로 설정되어야 합니다. 그렇지 않으면 시뮬레이터가 런타임 오류를 보고합니다. 이렇게 하는 쉬운 방법은 `Reset`을 호출하는 것입니다.

### <a name="visualizing-the-code-with-the-bloch-sphere"></a>블로흐 구를 사용하여 코드 시각화

블로흐 구의 북극은 클래식 값 **0**을 나타내고, 남극은 클래식 값 **1**을 나타냅니다. 모든 중첩은 구의 점으로 표현할 수 있습니다(화살표로 표시). 화살표의 끝부분이 극에 가까울수록 큐비트가 측정될 경우 해당 극에 할당된 클래식 값으로 축소될 확률이 높습니다. 예를 들어 아래쪽 빨간색 화살표로 표현되는 큐비트 상태는 측정될 경우 **0** 값을 제공할 확률이 높습니다.

<img src="./Bloch.svg" width="175">

이 표현을 사용하여 코드가 하는 일을 시각화할 수 있습니다.

* 먼저 **0** 상태에서 시작된 큐비트로 시작하고, `H`를 적용하여 **0**과 **1**의 확률이 동일한 중첩을 만듭니다.

<img src="./H.svg" width="450">

* 그런 다음, 큐비트를 측정하고 출력을 저장합니다.

<img src="./Measurement2.svg" width="450">

측정 결과는 완전히 임의적이므로 임의의 비트를 얻었습니다. 이 함수를 여러 번 호출하여 정수를 만들 수 있습니다. 예를 들어 이 함수를 세 번 호출하여 세 개의 임의 비트를 얻으면 임의의 3비트 숫자(즉, 0~7 사이의 임의 숫자)를 빌드할 수 있습니다.
