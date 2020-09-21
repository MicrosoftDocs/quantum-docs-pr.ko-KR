---
title: QDK 사용자 고유의 분류자 디자인
description: 퀀텀 회로 중심 분류자에 대 한 회로 모델 디자인의 기본 개념을 알아봅니다.
author: geduardo
ms.author: v-edsanc
ms.date: 02/17/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.design
no-loc:
- Q#
- $$v
ms.openlocfilehash: 3515279dd4d03b2a512035af0b13e084dd91f9dc
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835709"
---
# <a name="design-your-own-classifier"></a><span data-ttu-id="25a34-103">사용자 고유의 분류자 설계</span><span class="sxs-lookup"><span data-stu-id="25a34-103">Design your own classifier</span></span>

<span data-ttu-id="25a34-104">이 가이드에서는 퀀텀 회로 중심 분류자에 대 한 회로 모델 디자인의 기본 개념을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-104">In this guide you will learn the basic concepts behind the design of circuit models for the quantum circuit centric classifier.</span></span>

<span data-ttu-id="25a34-105">기존 심층 학습 에서처럼 특정 아키텍처를 선택 하는 일반적인 규칙은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-105">As in classical deep learning, there is no general rule for choosing a specific architecture.</span></span> <span data-ttu-id="25a34-106">문제에 따라 일부 아키텍처는 다른 아키텍처 보다 성능이 향상 됩니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-106">Depending on the problem some architectures will perform better than others.</span></span> <span data-ttu-id="25a34-107">그러나 회로를 설계할 때 유용할 수 있는 몇 가지 개념이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-107">But, there are some concepts that might be useful when designing the circuit:</span></span>

- <span data-ttu-id="25a34-108">많은 수의 매개 변수는 복잡 한 분류 경계를 그리는 데 적합할 수 있지만 과잉 맞춤에 더 취약할 수 있는 보다 유연한 모델을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-108">A large number of parameters implies a more flexible model, which may be suitable to draw complicated classification boundaries but which may also be more susceptible to overfitting.</span></span>

- <span data-ttu-id="25a34-109">Entangling 게이트는 퀀텀 기능 간의 상관 관계를 캡처하기 위해 반드시 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-109">Entangling gates between qubits are essential to capture the correlations between the quantum features.</span></span>

## <a name="how-to-build-a-classifier-with-q"></a><span data-ttu-id="25a34-110">Q를 사용 하 여 분류자를 빌드하는 방법\#</span><span class="sxs-lookup"><span data-stu-id="25a34-110">How to build a classifier with Q\#</span></span>

<span data-ttu-id="25a34-111">분류자를 빌드하기 위해 회로 모델에서 매개 변수가 있는 제어 되는 회전을 연결 하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-111">To build a classifier we are going to concatenate parametrized controlled rotations in our circuit model.</span></span> <span data-ttu-id="25a34-112">이렇게 하려면 [`ControlledRotation`](xref:microsoft.quantum.machinelearning.controlledrotation) 퀀텀 Machine Learning 라이브러리에 정의 된 형식을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-112">To do it we can use the type [`ControlledRotation`](xref:microsoft.quantum.machinelearning.controlledrotation) defined in the Quantum Machine Learning library.</span></span> <span data-ttu-id="25a34-113">이 형식에는 대상의 인덱스, 컨트롤의 인덱스 배열, 회전 축 및 모델을 정의 하는 매개 변수 배열에 있는 연결 된 매개 변수의 인덱스를 결정 하는 네 개의 인수가 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-113">This type accepts four arguments that determine: the index of the target qubit, the array of indices of the control qubits, the axis of rotation, and index of the associated parameter in the array of parameters defining the model.</span></span>

<span data-ttu-id="25a34-114">분류자의 예를 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-114">Let's see an example of a classifier.</span></span> <span data-ttu-id="25a34-115">[절반 moons 샘플](https://github.com/microsoft/Quantum/tree/main/samples/machine-learning/half-moons)에서는 파일에 정의 된 다음 분류자를 찾을 수 있습니다 `Training.qs` .</span><span class="sxs-lookup"><span data-stu-id="25a34-115">In the [half-moons sample](https://github.com/microsoft/Quantum/tree/main/samples/machine-learning/half-moons), we can find the following classifier defined in the file `Training.qs`.</span></span>

```qsharp
    function ClassifierStructure() : ControlledRotation[] {
        return [
            ControlledRotation((0, new Int[0]), PauliX, 4),
            ControlledRotation((0, new Int[0]), PauliZ, 5),
            ControlledRotation((1, new Int[0]), PauliX, 6),
            ControlledRotation((1, new Int[0]), PauliZ, 7),
            ControlledRotation((0, [1]), PauliX, 0),
            ControlledRotation((1, [0]), PauliX, 1),
            ControlledRotation((1, new Int[0]), PauliZ, 2),
            ControlledRotation((1, new Int[0]), PauliX, 3)
        ];
    }
 ```

<span data-ttu-id="25a34-116">여기에서 정의 하는 것은 요소 배열을 반환 하는 함수입니다 .이 함수는 `ControlledRotation` 매개 변수의 배열과 함께 사용 되며 바이어스가를 정의 [`SequentialModel`](xref:microsoft.quantum.machinelearning.sequentialmodel) 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-116">What we are defining here is a function that returns an array of `ControlledRotation` elements, that together with an array of parameters and a bias will define our [`SequentialModel`](xref:microsoft.quantum.machinelearning.sequentialmodel).</span></span> <span data-ttu-id="25a34-117">이 형식은 퀀텀 Machine Learning 라이브러리에서 기본 이며 분류자를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-117">This type is fundamental in the Quantum Machine Learning library and defines the classifier.</span></span> <span data-ttu-id="25a34-118">위의 함수에서 정의 된 회로는 데이터 집합의 각 샘플에 두 가지 기능이 포함 된 분류자의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-118">The circuit defined in the function above is part of a classifier in which each sample of the dataset contains two features.</span></span> <span data-ttu-id="25a34-119">따라서 두 개의 비트 비트만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-119">Therefore we only need two qubits.</span></span> <span data-ttu-id="25a34-120">회로의 그래픽 표현은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-120">The graphical representation of the circuit is:</span></span>

 ![회로 모델 예](~/media/circuit_model_1.PNG)

<span data-ttu-id="25a34-122">기본적으로 퀀텀 Machine Learning 라이브러리의 작업은 분류 확률을 예측 하기 위해 레지스터의 마지막 계산을 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-122">Note that by default the operations of the Quantum Machine Learning library measure the last qubit of the register to estimate the classification probabilities.</span></span> <span data-ttu-id="25a34-123">회로를 설계할 때이 사실을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-123">You should keep in mind this fact when designing your circuit.</span></span>

## <a name="use-the-library-functions-to-write-layers-of-gates"></a><span data-ttu-id="25a34-124">라이브러리 함수를 사용 하 여 게이트 계층 작성</span><span class="sxs-lookup"><span data-stu-id="25a34-124">Use the library functions to write layers of gates</span></span>

<span data-ttu-id="25a34-125">인스턴스당 784 기능이 포함 된 데이터 집합 (예: MNIST 데이터 집합 같은 28 × 28 픽셀 이미지)이 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-125">Suppose we have a dataset with 784 features per instance, e.g. images of 28×28 pixels like the MNIST dataset.</span></span> <span data-ttu-id="25a34-126">이 경우 회로의 너비는 충분 한 크기를 가지 므로 각 개별 gate를 편리 하 게 작성할 수 있지만 실용적이 지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-126">In this case, the width of the circuit becomes large enough so that writing by hand each individual gate becomes a possible but impractical task.</span></span> <span data-ttu-id="25a34-127">이 때문에 퀀텀 Machine Learning 라이브러리는 매개 변수가 있는 회전 레이어를 자동으로 생성 하는 도구 집합을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-127">This is why the Quantum Machine Learning library provides a set of tools to automatically generate layers of parametrized rotations.</span></span> <span data-ttu-id="25a34-128">예를 들어 함수는 [`LocalRotationsLayer`](xref:microsoft.quantum.machinelearning.localrotationslayer) 지정 된 축을 따라 지정 된 축을 따라 제어 가능한 단일 각도 비트 회전의 배열을 반환 합니다. 각는 레지스터의 각 매개 변수가 있는에 대해 한 번 회전 하 고 각각 다른 모델 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-128">For instance, the function [`LocalRotationsLayer`](xref:microsoft.quantum.machinelearning.localrotationslayer) returns an array of uncontrolled single-qubit rotations along a given axis, with one rotation for each qubit in the register, each parametrized by a different model parameter.</span></span> <span data-ttu-id="25a34-129">예를 들어는 `LocalRotationsLayer(4, X)` 다음 게이트 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-129">For example, `LocalRotationsLayer(4, X)` returns the following set of gates:</span></span>

 ![로컬 회전 계층](~/media/local_rotations_layer.PNG)

<span data-ttu-id="25a34-131">회로 디자인을 간소화 하는 데 사용할 수 있는 모든 도구를 검색 하려면 [퀀텀 Machine Learning 라이브러리의 API 참조](xref:microsoft.quantum.machinelearning) 를 탐색 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-131">We recommend you explore the [API reference of the Quantum Machine Learning library](xref:microsoft.quantum.machinelearning) to discover all the tools available to streamline the circuit design.</span></span>

## <a name="next-steps"></a><span data-ttu-id="25a34-132">다음 단계</span><span class="sxs-lookup"><span data-stu-id="25a34-132">Next steps</span></span>

 <span data-ttu-id="25a34-133">샘플에서 제공 하는 예제에서 다른 구조를 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-133">Try different structures in the examples provided by the samples.</span></span> <span data-ttu-id="25a34-134">모델의 성능에 대 한 변경 내용이 표시 되나요?</span><span class="sxs-lookup"><span data-stu-id="25a34-134">Do you see any changes in the performance of the model?</span></span> <span data-ttu-id="25a34-135">다음 자습서에서는 [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load) 데이터 집합을 로드 하 여 분류자의 새 아키텍처를 시험해 보고 탐색 하는 방법을 배웁니다.</span><span class="sxs-lookup"><span data-stu-id="25a34-135">In the next tutorial, [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load), you will learn how to load datasets to try and explore new architectures of classifiers.</span></span>
