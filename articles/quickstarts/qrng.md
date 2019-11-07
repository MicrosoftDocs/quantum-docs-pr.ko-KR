---
title: 양자 난수 생성기 만들기
description: 양자 난수 생성기를 만들어서 중첩 같은 기본적인 양자 개념을 보여주는 Q# 프로젝트를 빌드합니다.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: c3039b92c4b3235a397d5cf31280ac2673706e9d
ms.sourcegitcommit: 2ca4755d1a63431e3cb2d2918a10ad477ec2e368
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/03/2019
ms.locfileid: "73462841"
---
# <a name="quickstart-implement-a-quantum-random-number-generator-in-q"></a><span data-ttu-id="1a8ce-103">빠른 시작: Q#에서 양자 난수 생성기 구현</span><span class="sxs-lookup"><span data-stu-id="1a8ce-103">Quickstart: Implement a Quantum Random Number Generator in Q#</span></span>
<span data-ttu-id="1a8ce-104">Q#으로 양자 난수 생성기를 작성하는 간단한 양자 알고리즘 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-104">A simple example of a quantum algorithm written in Q# is a quantum random number generator.</span></span> <span data-ttu-id="1a8ce-105">이 알고리즘은 양자 메커니즘의 특성을 활용하여 난수를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-105">This algorithm leverages the nature of quantum mechanics to produce a random number.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="1a8ce-106">필수 조건</span><span class="sxs-lookup"><span data-stu-id="1a8ce-106">Prerequisites</span></span>

- <span data-ttu-id="1a8ce-107">Microsoft [Quantum Development Kit](xref:microsoft.quantum.install)</span><span class="sxs-lookup"><span data-stu-id="1a8ce-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- [<span data-ttu-id="1a8ce-108">Q# 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="1a8ce-108">Create a Q# Project</span></span>](xref:microsoft.quantum.howto.createproject)


## <a name="write-a-q-operation"></a><span data-ttu-id="1a8ce-109">Q# 연산 작성</span><span class="sxs-lookup"><span data-stu-id="1a8ce-109">Write a Q# operation</span></span>

### <a name="q-operation-code"></a><span data-ttu-id="1a8ce-110">Q# 연산 코드</span><span class="sxs-lookup"><span data-stu-id="1a8ce-110">Q# operation code</span></span>

1. <span data-ttu-id="1a8ce-111">Operation.qs 파일의 내용을 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-111">Replace the contents of the Operation.qs file with the following code:</span></span>

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

<span data-ttu-id="1a8ce-112">[양자 컴퓨팅이란?](xref:microsoft.quantum.overview.what) 문서에서 언급했듯이, 큐비트는 중첩에 있을 수 있는 양자 정보의 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-112">As mentioned in our [What is Quantum Computing?](xref:microsoft.quantum.overview.what) article, a qubit is a unit of quantum information that can be in superposition.</span></span> <span data-ttu-id="1a8ce-113">측정된 큐비트는 0 또는 1 중 하나만 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-113">When measured, a qubit can only be either 0 or 1.</span></span> <span data-ttu-id="1a8ce-114">하지만 실행 중인 동안 큐비트 상태는 측정값이 0 또는 1일 수 있는 확률을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-114">However, during execution the state of the qubit represents the probability of reading either a 0 or a 1 with a measurement.</span></span> <span data-ttu-id="1a8ce-115">이 확률적 상태를 중첩이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-115">This probabilistic state is known as superposition.</span></span> <span data-ttu-id="1a8ce-116">이 확률을 사용하여 난수를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-116">We can use this probability to generate random numbers.</span></span>

<span data-ttu-id="1a8ce-117">Q# 연산에서는 Q#의 기본 형식인 `Qubit` 데이터 형식을 도입합니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-117">In our Q# operation, we introduce the `Qubit` datatype, native to Q#.</span></span> <span data-ttu-id="1a8ce-118">`Qubit`는 `using` 문으로만 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-118">We can only allocate a `Qubit` with a `using` statement.</span></span> <span data-ttu-id="1a8ce-119">할당된 큐비트는 항상 `Zero` 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-119">When it gets allocated a qubit is always in the `Zero`  state.</span></span> 

<span data-ttu-id="1a8ce-120">`H` 연산을 사용하여 `Qubit`를 중첩 상태로 전환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-120">Using the `H` operation, we are able to put our `Qubit` in superposition.</span></span> <span data-ttu-id="1a8ce-121">큐비트를 측정하고 값을 읽으려면 `M` 내장 연산을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-121">To measure a qubit and read its value, you use the `M` intrinsic operation.</span></span>

<span data-ttu-id="1a8ce-122">`Qubit`를 중첩 상태로 전환하고 측정하면 코드가 호출될 때마다 다른 값이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-122">By putting our `Qubit` in superposition and measuring it, our result will be a different value each time the code is invoked.</span></span> 

<span data-ttu-id="1a8ce-123">`Qubit`를 할당 취소하면 큐비트가 명시적으로 다시 `Zero` 상태로 설정되어야 합니다. 그렇지 않으면 시뮬레이터가 런타임 오류를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-123">When a `Qubit` is de-allocated it must be explicitly set back to the `Zero` state, otherwise the simulator will report a runtime error.</span></span> <span data-ttu-id="1a8ce-124">이렇게 하는 쉬운 방법은 `Reset`을 호출하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-124">An easy way to achieve this is invoking `Reset`.</span></span>

### <a name="visualizing-the-code-with-the-bloch-sphere"></a><span data-ttu-id="1a8ce-125">블로흐 구를 사용하여 코드 시각화</span><span class="sxs-lookup"><span data-stu-id="1a8ce-125">Visualizing the code with the Bloch sphere</span></span>

<span data-ttu-id="1a8ce-126">블로흐 구의 북극은 클래식 값 **0**을 나타내고, 남극은 클래식 값 **1**을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-126">In the Bloch sphere the north pole represents the classical value **0** and the south pole represents the classical value **1**.</span></span> <span data-ttu-id="1a8ce-127">모든 중첩은 구의 점으로 표현할 수 있습니다(화살표로 표시).</span><span class="sxs-lookup"><span data-stu-id="1a8ce-127">Any superposition can be represented by a point on the sphere (represented by an arrow).</span></span> <span data-ttu-id="1a8ce-128">화살표의 끝부분이 극에 가까울수록 큐비트가 측정될 경우 해당 극에 할당된 클래식 값으로 축소될 확률이 높습니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-128">When the closer the end of the arrow to a pole, the higher the probability the qubit collapses into the classical value assigned to that pole when measured.</span></span> <span data-ttu-id="1a8ce-129">예를 들어 아래쪽 빨간색 화살표로 표현되는 큐비트 상태는 측정될 경우 **0** 값을 제공할 확률이 높습니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-129">For example, the qubit state represented by the red arrow below has a higher probability of giving the value **0** if we measure it.</span></span>

<img src="./Bloch.svg" width="175">

<span data-ttu-id="1a8ce-130">이 표현을 사용하여 코드가 하는 일을 시각화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-130">We can use this representation to visualize what the code is doing:</span></span>

* <span data-ttu-id="1a8ce-131">먼저 **0** 상태에서 시작된 큐비트로 시작하고, `H`를 적용하여 **0**과 **1**의 확률이 동일한 중첩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-131">First we start with a qubit initalizated in the state **0** and apply `H` to create a superposition in which the probabilities for **0** and **1** are the same.</span></span>

<img src="./H.svg" width="450">

* <span data-ttu-id="1a8ce-132">그런 다음, 큐비트를 측정하고 출력을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-132">Then we measure the qubit and save the output:</span></span>

<img src="./Measurement2.svg" width="450">

<span data-ttu-id="1a8ce-133">측정 결과는 완전히 임의적이므로 임의의 비트를 얻었습니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-133">Since the outcome of the measurement is completely random, we have obtained a random bit.</span></span> <span data-ttu-id="1a8ce-134">이 연산을 여러 번 호출하여 정수를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-134">We can call this operation several times to create integers.</span></span> <span data-ttu-id="1a8ce-135">예를 들어 이 연산을 세 번 호출하여 세 개의 임의 비트를 얻으면 임의의 3비트 숫자(즉, 0~7 사이의 임의 숫자)를 빌드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-135">For example, if we call the operation three times to obtain three random bits, we can build random 3-bit numbers (that is, a random number between 0 and 7).</span></span>
