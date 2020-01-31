---
title: '모두 통합-Q # 기술 | Microsoft Docs'
description: '모든 것을 함께 저장-Q # 기술'
uid: microsoft.quantum.techniques.puttingittogether
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 3605826da159757d4b321dbf4ec6acd7f4e6be05
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820167"
---
# <a name="putting-it-all-together-teleportation"></a><span data-ttu-id="e0451-103">모두 함께 배치: Teleportation</span><span class="sxs-lookup"><span data-stu-id="e0451-103">Putting It All Together: Teleportation</span></span> #
<span data-ttu-id="e0451-104">[퀀텀 회로](xref:microsoft.quantum.concepts.circuits)에 정의 된 teleportation 회로의 예제로 돌아가 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-104">Let's return to the example of the teleportation circuit defined in [Quantum Circuits](xref:microsoft.quantum.concepts.circuits).</span></span> <span data-ttu-id="e0451-105">지금까지 배운 개념을 설명 하는 데이 방법을 사용할 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-105">We're going to use this to illustrate the concepts we've learned so far.</span></span> <span data-ttu-id="e0451-106">퀀텀 teleportation에 대 한 설명은 아래에 설명 되어 있으며, 그 다음에는 Q #의 코드 구현 연습이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-106">An explanation of quantum teleportation is provided below for those who are unfamiliar with the theory, followed by a walkthrough of the code implementation in Q#.</span></span> 

## <a name="quantum-teleportation-theory"></a><span data-ttu-id="e0451-107">퀀텀 Teleportation: 이론</span><span class="sxs-lookup"><span data-stu-id="e0451-107">Quantum Teleportation: Theory</span></span>
<span data-ttu-id="e0451-108">퀀텀 teleportation은 알 수 없는 퀀텀 상태 ('__메시지__' 라고 함)를 한 위치에 있는 특정 위치에서 다른 위치에 있는 이상으로 전송 하는 기술입니다 (각각 ' 여기 ' 및 '__여기__ __'로__표시 됨).</span><span class="sxs-lookup"><span data-stu-id="e0451-108">Quantum teleportation is a technique for sending an unknown quantum state (which we'll refer to as the '__message__') from a qubit in one location to a qubit in another location (we'll refer to these qubits as '__here__' and '__there__', respectively).</span></span> <span data-ttu-id="e0451-109">__메시지__ 는 다음과 같이 diac 표기법을 사용 하 여 벡터로 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-109">We can represent our __message__ as a vector using Dirac notation:</span></span> 

<span data-ttu-id="e0451-110">$ $ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $ $</span><span class="sxs-lookup"><span data-stu-id="e0451-110">$$ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $$</span></span>

<span data-ttu-id="e0451-111">$ \Alpha $ 및 $ \alpha $ 값을 알 수 없으므로 __메시지__ 의 상태를 알 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-111">The __message__ qubit's state is unknown to us as we do not know the values of $\alpha$ and $\beta$.</span></span>

### <a name="step-1-create-an-entangled-state"></a><span data-ttu-id="e0451-112">1 단계: entangled 상태 만들기</span><span class="sxs-lookup"><span data-stu-id="e0451-112">Step 1: Create an entangled state</span></span>
<span data-ttu-id="e0451-113">__메시지__ 를 보내려면 __여기__ 에는 원하는 비트를 사용 하 여이를 위한 것이 __좋습니다.__</span><span class="sxs-lookup"><span data-stu-id="e0451-113">In order to send the __message__ we need for the qubit __here__ to be entangled with the qubit __there__.</span></span> <span data-ttu-id="e0451-114">이는 Hadamard 게이트를 적용 하 고 CNOT 게이트를 적용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-114">This is achieved by applying a Hadamard gate, followed by a CNOT gate.</span></span> <span data-ttu-id="e0451-115">이러한 게이트 작업 뒤의 수치를 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-115">Let's look at the math behind these gate operations.</span></span>

<span data-ttu-id="e0451-116">__여기서는 여기에 나와__ 있는 것과 $ \ket{0}$ 상태 모두로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-116">We will begin with the qubits __here__ and __there__ both in the $\ket{0}$ state.</span></span> <span data-ttu-id="e0451-117">이러한 entangling 후에는 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-117">After entangling these qubits, they are in the state:</span></span>

<span data-ttu-id="e0451-118">$ $ \ket{\phi ^ +} = \frac{1}{\sqrt{2}} (\ket{00} + \ket{11}) $ $</span><span class="sxs-lookup"><span data-stu-id="e0451-118">$$ \ket{\phi^+} = \frac{1}{\sqrt{2}}(\ket{00} + \ket{11}) $$</span></span>

### <a name="step-2-send-the-message"></a><span data-ttu-id="e0451-119">2 단계: 메시지 보내기</span><span class="sxs-lookup"><span data-stu-id="e0451-119">Step 2: Send the message</span></span>
<span data-ttu-id="e0451-120">__메시지__ 를 보내려면 먼저 __메시지__ 를 사용 하 여 cnot gate를 적용 합니다. __여기서__ 는 (컨트롤이 제어 하는 데 사용 되는 __메시지__ 이 고, __여기서__ 는이 인스턴스에서 대상의 비트입니다.)</span><span class="sxs-lookup"><span data-stu-id="e0451-120">To send the __message__ we first apply a CNOT gate with the __message__ qubit and __here__ qubit as inputs (the __message__ qubit being the control and the __here__ qubit being the target qubit, in this instance).</span></span> <span data-ttu-id="e0451-121">이 입력 상태를 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-121">This input state can be written:</span></span>

<span data-ttu-id="e0451-122">$ $ \ket{\psi}\ket{\phi ^ +} = (\alpha\ket{0} + \beta\ket{1}) (\frac{1}{\sqrt{2}} (\ket{00} + \ket{11})) $ $</span><span class="sxs-lookup"><span data-stu-id="e0451-122">$$ \ket{\psi}\ket{\phi^+} = (\alpha\ket{0} + \beta\ket{1})(\frac{1}{\sqrt{2}}(\ket{00} + \ket{11})) $$</span></span>

<span data-ttu-id="e0451-123">다음과 같이 확장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-123">This expands to:</span></span>

<span data-ttu-id="e0451-124">$ $ \ket{\psi}\ket{\phi ^ +} = \frac{\alpha}{\sqrt{2}} \ket{000} + \frac{\alpha}{\sqrt{2}} \ket{011} + \frac{\beta}{\sqrt{2}} \ket{100} + \frac{\beta}{\sqrt{2}} \ket{111} $ $</span><span class="sxs-lookup"><span data-stu-id="e0451-124">$$ \ket{\psi}\ket{\phi^+} = \frac{\alpha}{\sqrt{2}}\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{100} + \frac{\beta}{\sqrt{2}}\ket{111} $$</span></span>

<span data-ttu-id="e0451-125">이에 대 한 미리 알림으로 CNOT gate는 컨트롤의가 1 인 경우 대상의 목표를 대칭 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-125">As a reminder, the CNOT gate flips the target qubit when the control qubit is 1.</span></span> <span data-ttu-id="e0451-126">예를 들어 $ \ket{000}$의 입력으로 인해 첫 번째 (컨트롤)가 0 이므로 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-126">So for example, an input of $\ket{000}$ will result in no change as the first qubit (the control) is 0.</span></span> <span data-ttu-id="e0451-127">그러나 첫 번째 인수를 1로 사용 하는 경우 (예: $ \ket{100}$의 입력)</span><span class="sxs-lookup"><span data-stu-id="e0451-127">However, take a case where the first qubit is 1 - for example an input of $\ket{100}$.</span></span> <span data-ttu-id="e0451-128">이 경우 두 번째 \ket (대상)는 CNOT gate에 의해 대칭 이동 되므로 출력은 ${110}$입니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-128">In this instance, the output is $\ket{110}$ as the second qubit (the target) is flipped by the CNOT gate.</span></span>

<span data-ttu-id="e0451-129">이제 CNOT gate가 위의 입력을 처리 한 후 출력을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-129">Let's now consider our output once the CNOT gate has acted on our input above.</span></span> <span data-ttu-id="e0451-130">결과는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-130">The result is:</span></span>

<span data-ttu-id="e0451-131">$ $ \frac{\alpha}{\sqrt{2}} \ket{000} + \frac{\alpha}{\sqrt{2}} \ket{011} + \frac{\beta}{\sqrt{2}} \ket{110} + \frac{\beta}{\sqrt{2}} \ket{101} $ $</span><span class="sxs-lookup"><span data-stu-id="e0451-131">$$ \frac{\alpha}{\sqrt{2}}\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{110} + \frac{\beta}{\sqrt{2}}\ket{101} $$</span></span>

<span data-ttu-id="e0451-132">__메시지__ 를 전송 하는 다음 단계는 Hadamard gate를 __메시지의 메시지__ 에 적용 하는 것입니다 (각 용어의 첫 번째 비트율 비트).</span><span class="sxs-lookup"><span data-stu-id="e0451-132">The next step to send the __message__ is to apply a Hadamard gate to the __message__ qubit (that's the first qubit of each term).</span></span> 

<span data-ttu-id="e0451-133">Hadamard gate는 다음과 같은 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-133">As a reminder, the Hadamard gate does the following:</span></span>

<span data-ttu-id="e0451-134">입력</span><span class="sxs-lookup"><span data-stu-id="e0451-134">Input</span></span> | <span data-ttu-id="e0451-135">출력</span><span class="sxs-lookup"><span data-stu-id="e0451-135">Output</span></span>
---------------------------| ---------------------------------------------------------------
<span data-ttu-id="e0451-136">$ \ket{0}$</span><span class="sxs-lookup"><span data-stu-id="e0451-136">$\ket{0}$</span></span>  | <span data-ttu-id="e0451-137">$ \frac{1}{\sqrt{2}} (\ket{0} + \ket{1}) $</span><span class="sxs-lookup"><span data-stu-id="e0451-137">$\frac{1}{\sqrt{2}}(\ket{0} + \ket{1})$</span></span>
<span data-ttu-id="e0451-138">$ \ket{1}$</span><span class="sxs-lookup"><span data-stu-id="e0451-138">$\ket{1}$</span></span>  | <span data-ttu-id="e0451-139">$ \frac{1}{\sqrt{2}} (\ket{0}-\ket{1}) $</span><span class="sxs-lookup"><span data-stu-id="e0451-139">$\frac{1}{\sqrt{2}}(\ket{0} - \ket{1})$</span></span>

<span data-ttu-id="e0451-140">위의 출력의 각 용어에 대 한 첫 번째 Hadamard를 적용 하는 경우 다음과 같은 결과를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-140">If we apply the Hadamard gate to the first qubit of each term of our output above, we get the following result:</span></span>

<span data-ttu-id="e0451-141">$ $ \frac{\alpha}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0} + \ket{1})) \ket{00} + \frac{\alpha}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0} + \ket{1})) \ket{11} + \frac{\beta}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0}-\ket{1})) \ket{10} + \frac{\beta}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0}-\ket{1})) \ket{01} $ $</span><span class="sxs-lookup"><span data-stu-id="e0451-141">$$ \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} + \ket{1}))\ket{00} + \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} + \ket{1}))\ket{11} + \frac{\beta}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} - \ket{1}))\ket{10} + \frac{\beta}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} - \ket{1}))\ket{01} $$</span></span>

<span data-ttu-id="e0451-142">각 용어에는 $2 \frac{1}{\sqrt{2}} $ 요인이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-142">Note that each term has two $\frac{1}{\sqrt{2}}$ factors.</span></span> <span data-ttu-id="e0451-143">다음 결과를 제공 하는 것과 같은 결과를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-143">We can multiply these out giving the following result:</span></span>

<span data-ttu-id="e0451-144">$ $ \frac{\alpha}{2}(\ket{0} + \ket{1}) \ket{00} + \frac{\alpha}{2}(\ket{0} + \ket{1}) \ket{11} + \frac{\beta}{2}(\ket{0}-\ket{1}) \ket{10} + \frac{\beta}{2}(\ket{0}-\ket{1}) \ket{01} $ $</span><span class="sxs-lookup"><span data-stu-id="e0451-144">$$ \frac{\alpha}{2}(\ket{0} + \ket{1})\ket{00} + \frac{\alpha}{2}(\ket{0} + \ket{1})\ket{11} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{10} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{01} $$</span></span>

<span data-ttu-id="e0451-145">$ \Frac{1}{2}$ 요인은 각 용어에 공통적으로 적용 되므로 이제는 괄호를 벗어날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-145">The  $\frac{1}{2}$ factor is common to each term so we can now take it outside the brackets:</span></span>

<span data-ttu-id="e0451-146">$ $ \frac{1}{2}\big [\alpha (\ket{0} + \ket{1}) \ket{00} + \alpha (\ket{0} + \ket{1}) \ket{11} + \beta (\ket{0}-\ket{1}) \ket{10} + \beta (\ket{0}-\ket{1}) \ket{01}\big] $ $</span><span class="sxs-lookup"><span data-stu-id="e0451-146">$$ \frac{1}{2}\big[\alpha(\ket{0} + \ket{1})\ket{00} + \alpha(\ket{0} + \ket{1})\ket{11} + \beta(\ket{0} - \ket{1})\ket{10} + \beta(\ket{0} - \ket{1})\ket{01}\big] $$</span></span>

<span data-ttu-id="e0451-147">그러면 다음을 제공 하는 각 용어에 대해 괄호를 곱합니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-147">We can then multiply out the brackets for each term giving:</span></span>

<span data-ttu-id="e0451-148">$ $ \frac{1}{2}\big [\alpha\ket{000} + \alpha\ket{100} + \alpha\ket{011} + \alpha\ket{111} + \beta\ket{010}-\beta\ket{110} + \beta\ket{001}-\beta\ket{101}\big] $ $</span><span class="sxs-lookup"><span data-stu-id="e0451-148">$$ \frac{1}{2}\big[\alpha\ket{000} + \alpha\ket{100} + \alpha\ket{011} + \alpha\ket{111} + \beta\ket{010} - \beta\ket{110} + \beta\ket{001} - \beta\ket{101}\big] $$</span></span>

### <a name="step-3-measure-the-result"></a><span data-ttu-id="e0451-149">3 단계: 결과 측정</span><span class="sxs-lookup"><span data-stu-id="e0451-149">Step 3: Measure the result</span></span>

<span data-ttu-id="e0451-150">__여기__ __에는이__로 __인해,__ __여기서__ 의 모든 측정은 상태에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-150">Due to __here__ and __there__ being entangled, any measurement on __here__ will affect the state of __there__.</span></span> <span data-ttu-id="e0451-151">첫 번째 및 두 번째 비트 (__메시지__ 및 __여기__)를 측정 하는 경우 되거나 얽 히의이 속성으로 인해에 __있는 상태를__ 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-151">If we measure the first and second qubit (__message__ and __here__) we can learn what state __there__ is in, due to this property of entanglement.</span></span> 

* <span data-ttu-id="e0451-152">결과 00을 측정 하 고 가져오는 경우 superposition 축소 되 고이 결과와 일치 하는 용어를 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-152">If we measure and get a result 00, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="e0451-153">$ \Alpha\ket{000} + \beta\ket{001}$입니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-153">That's $\alpha\ket{000} +\beta\ket{001}$.</span></span> <span data-ttu-id="e0451-154">$ \Ket{00}(\alpha\ket{0} + \beta\ket{1}) $로 리팩터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-154">This can be refactored to $\ket{00}(\alpha\ket{0} +\beta\ket{1})$.</span></span> <span data-ttu-id="e0451-155">따라서 첫 번째 및 두 번째 비트를 00으로 측정 하는 경우 세 번째 비트는 $ (\alpha\ket{0} + \beta\ket{1}) $ 상태에 있음을 알 수 __있습니다__.</span><span class="sxs-lookup"><span data-stu-id="e0451-155">Therefore if we measure the first and second qubit to be 00, we know that the third qubit, __there__, is in the state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="e0451-156">결과 01을 측정 하 고 가져오는 경우 superposition 축소 되 고이 결과와 일치 하는 용어를 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-156">If we measure and get a result 01, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="e0451-157">$ \Alpha\ket{011} + \beta\ket{010}$입니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-157">That's $\alpha\ket{011} +\beta\ket{010}$.</span></span> <span data-ttu-id="e0451-158">$ \Ket{01}(\alpha\ket{1} + \beta\ket{0}) $로 리팩터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-158">This can be refactored to $\ket{01}(\alpha\ket{1} +\beta\ket{0})$.</span></span> <span data-ttu-id="e0451-159">따라서 첫 번째 및 두 번째 비트를 01로 측정 하는 경우 세 번째 비트는 $ (\alpha\ket{1} + \beta\ket{0}) $ 상태에 __있습니다__.</span><span class="sxs-lookup"><span data-stu-id="e0451-159">Therefore if we measure the first and second qubit to be 01, we know that the third qubit, __there__, is in the state $(\alpha\ket{1} +\beta\ket{0})$.</span></span>
* <span data-ttu-id="e0451-160">결과 10을 측정 하 고 얻을 경우이 결과와 일치 하는 용어를 그대로 두고 superposition 축소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-160">If we measure and get a result 10, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="e0451-161">$ \Alpha\ket{100} \beta\ket{101}$입니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-161">That's $\alpha\ket{100} -\beta\ket{101}$.</span></span> <span data-ttu-id="e0451-162">$ \Ket{10}(\alpha\ket{0}-\beta\ket{1}) $로 리팩터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-162">This can be refactored to $\ket{10}(\alpha\ket{0} -\beta\ket{1})$.</span></span> <span data-ttu-id="e0451-163">따라서 첫 번째 및 두 번째 __비트를 10__으로 측정 하는 경우 세 번째 \alpha\ket는 상태 $ ({0}-\beta\ket{1}) $입니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-163">Therefore if we measure the first and second qubit to be 10, we know that the third qubit, __there__, is in the state $(\alpha\ket{0} -\beta\ket{1})$.</span></span>
* <span data-ttu-id="e0451-164">결과 11을 측정 하 여 얻을 경우 superposition 축소 되 고이 결과와 일치 하는 용어를 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-164">If we measure and get a result 11, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="e0451-165">$ \Alpha\ket{111} \beta\ket{110}$입니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-165">That's $\alpha\ket{111} -\beta\ket{110}$.</span></span> <span data-ttu-id="e0451-166">$ \Ket{11}(\alpha\ket{1}-\beta\ket{0}) $로 리팩터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-166">This can be refactored to $\ket{11}(\alpha\ket{1} -\beta\ket{0})$.</span></span> <span data-ttu-id="e0451-167">따라서 첫 번째 및 두 번째 __비트를 11__로 측정 하는 경우 세 번째 \alpha\ket는 상태 $ ({1}-\beta\ket{0}) $입니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-167">Therefore if we measure the first and second qubit to be 11, we know that the third qubit, __there__, is in the state $(\alpha\ket{1} -\beta\ket{0})$.</span></span>

### <a name="step-4-interpret-the-result"></a><span data-ttu-id="e0451-168">4 단계: 결과 해석</span><span class="sxs-lookup"><span data-stu-id="e0451-168">Step 4: Interpret the result</span></span>

<span data-ttu-id="e0451-169">보내려는 원래 __메시지__ 는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-169">As a reminder, the original __message__ we wished to send was:</span></span>

<span data-ttu-id="e0451-170">$ $ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $ $</span><span class="sxs-lookup"><span data-stu-id="e0451-170">$$ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $$</span></span>

<span data-ttu-id="e0451-171">수신 된 상태가 의도 된 상태가 되도록이 상태를이 상태로 __가져와야 합니다.__</span><span class="sxs-lookup"><span data-stu-id="e0451-171">We need to get the __there__ qubit into this state, so that the received state is the one that was intended.</span></span> 

* <span data-ttu-id="e0451-172">00의 결과를 측정 하 고 결과를 얻은 경우 세 번째 비트는 $ (\alpha\ket{0} + \beta\ket{1}) $ 상태에 __있습니다__.</span><span class="sxs-lookup"><span data-stu-id="e0451-172">If we measured and got a result of 00, then the third qubit, __there__, is in the state $(\alpha\ket{0} +\beta\ket{1})$.</span></span> <span data-ttu-id="e0451-173">이 메시지는 의도 된 __메시지__이므로 변경이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-173">As this is the intended __message__, no alteration is required.</span></span>
* <span data-ttu-id="e0451-174">이를 측정 하 고 결과를 01로 얻은 경우 세 번째 비트는 $ (\alpha\ket{1} + \beta\ket{0}) $ 상태에 __있습니다__.</span><span class="sxs-lookup"><span data-stu-id="e0451-174">If we measured and got a result of 01, then the third qubit, __there__, is in the state $(\alpha\ket{1} +\beta\ket{0})$.</span></span> <span data-ttu-id="e0451-175">이는 의도 한 __메시지__와 다르지만, no gate를 적용 하면 원하는 상태 $ (\alpha\ket{0} + \beta\ket{1}) $가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-175">This differs from the intended __message__, however applying a NOT gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="e0451-176">10의 결과를 측정 하 고 결과를 얻은 경우 세 번째 비트율 비트는 $ (\alpha\ket{0}-\beta\ket{1}) $ 상태에 __있습니다__.</span><span class="sxs-lookup"><span data-stu-id="e0451-176">If we measured and got a result of 10, then the third qubit, __there__, is in the state $(\alpha\ket{0} -\beta\ket{1})$.</span></span> <span data-ttu-id="e0451-177">이는 의도 한 __메시지__와 다르지만 Z 게이트를 적용 하면 원하는 상태 $ (\alpha\ket{0} + \beta\ket{1}) $가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-177">This differs from the intended __message__, however applying a Z gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="e0451-178">11의 결과를 측정 하 고 결과를 얻은 경우 세 번째 비트율 비트는 $ (\alpha\ket{1}-\beta\ket{0}) $ 상태에 __있습니다__.</span><span class="sxs-lookup"><span data-stu-id="e0451-178">If we measured and got a result of 11, then the third qubit, __there__, is in the state $(\alpha\ket{1} -\beta\ket{0})$.</span></span> <span data-ttu-id="e0451-179">이는 의도 한 __메시지__와는 다르지만, Z 게이트 뒤에, Z 게이트를 적용 하면 원하는 상태 $ (\alpha\ket{0} + \beta\ket{1}) $가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-179">This differs from the intended __message__, however applying a NOT gate followed by a Z gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>

<span data-ttu-id="e0451-180">요약 하면 측정 하 고 첫 번째 고 비트는 1 이면 Z 게이트가 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-180">To summarize, if we measure and the first qubit is 1, a Z gate is applied.</span></span> <span data-ttu-id="e0451-181">측정 하 고 두 번째 고 비트는 1 인 경우에는 게이트가 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-181">If we measure and the second qubit is 1, a NOT gate is applied.</span></span>

### <a name="summary"></a><span data-ttu-id="e0451-182">요약</span><span class="sxs-lookup"><span data-stu-id="e0451-182">Summary</span></span>
<span data-ttu-id="e0451-183">아래에는 teleportation를 구현 하는 텍스트 책 퀀텀 회로가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-183">Shown below is a text-book quantum circuit that implements the teleportation.</span></span> <span data-ttu-id="e0451-184">왼쪽에서 오른쪽으로 이동 하 여 다음을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-184">Moving from left to right you can see:</span></span>
- <span data-ttu-id="e0451-185">1 단계: Hadamard gate 및 CNOT gate를 적용 하 여 __여기__ __에서 Entangling__ .</span><span class="sxs-lookup"><span data-stu-id="e0451-185">Step 1: Entangling __here__ and __there__ by applying a Hadamard gate and CNOT gate.</span></span>
- <span data-ttu-id="e0451-186">2 단계: CNOT gate 및 Hadamard gate를 사용 하 여 __메시지__ 보내기</span><span class="sxs-lookup"><span data-stu-id="e0451-186">Step 2: Sending the __message__ using a CNOT gate and a Hadamard gate.</span></span>
- <span data-ttu-id="e0451-187">3 단계: 첫 번째 및 두 번째 비트를 측정 하 고, __메시지__ 를 __측정 합니다.__</span><span class="sxs-lookup"><span data-stu-id="e0451-187">Step 3: Taking a measurement of the first and second qubits, __message__ and __here__.</span></span>
- <span data-ttu-id="e0451-188">4 단계: 3 단계의 측정 결과에 따라 NOT gate 또는 Z 게이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-188">Step 4: Applying a NOT gate or a Z gate, depending on the result of the measurement in step 3.</span></span>

![' 텔레포트 (msg:?): Unit '](~/media/teleportation.svg)

## <a name="quantum-teleportation-code"></a><span data-ttu-id="e0451-190">퀀텀 Teleportation: 코드</span><span class="sxs-lookup"><span data-stu-id="e0451-190">Quantum Teleportation: Code</span></span>

<span data-ttu-id="e0451-191">퀀텀 teleportation에 대 한 회로가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-191">We have our circuit for quantum teleportation:</span></span>

![' 텔레포트 (msg:?): Unit '](~/media/teleportation.svg)

<span data-ttu-id="e0451-193">이제이 퀀텀 회로의 각 단계를 Q #으로 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-193">We can now translate each of the steps in this quantum circuit into Q#.</span></span>

### <a name="step-0-definition"></a><span data-ttu-id="e0451-194">0 단계: 정의</span><span class="sxs-lookup"><span data-stu-id="e0451-194">Step 0: Definition</span></span>
<span data-ttu-id="e0451-195">Teleportation을 수행 하는 경우 보내려는 __메시지__ 와이 메시지를 보낼 위치 __()를__알아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-195">When we perform teleportation, we must know the __message__ we wish to send, and where we wish to send it (__there__).</span></span> <span data-ttu-id="e0451-196">이러한 이유로 두 개의 인수를 인수로 지정 하는 새 텔레포트 작업 (`msg` 및 `there`을 정의 하는 것으로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-196">For this reason, we begin by defining a new Teleport operation that is given two qubits as arguments, `msg` and `there`:</span></span>

```qsharp
operation Teleport(msg : Qubit, there : Qubit) : Unit {
```

<span data-ttu-id="e0451-197">또한 `using` 블록을 사용 하 여 달성할 수 있는 `here`을 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-197">We also need to allocate a qubit `here` which we achieve with a `using` block:</span></span>

```qsharp
    using (here = Qubit()) {
```

### <a name="step-1-create-an-entangled-state"></a><span data-ttu-id="e0451-198">1 단계: entangled 상태 만들기</span><span class="sxs-lookup"><span data-stu-id="e0451-198">Step 1: Create an entangled state</span></span>
<span data-ttu-id="e0451-199">그런 다음 @"microsoft.quantum.intrinsic.h" 및 @"microsoft.quantum.intrinsic.cnot" 작업을 사용 하 여 `here`와 `there` 간에 entangled 쌍을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-199">We can then create the entangled pair between `here` and `there` by using the @"microsoft.quantum.intrinsic.h" and @"microsoft.quantum.intrinsic.cnot" operations:</span></span>

```qsharp
        H(here);
        CNOT(here, there);
```

### <a name="step-2-send-the-message"></a><span data-ttu-id="e0451-200">2 단계: 메시지 보내기</span><span class="sxs-lookup"><span data-stu-id="e0451-200">Step 2: Send the message</span></span>
<span data-ttu-id="e0451-201">그런 다음, 다음 $ \operatorname{CNOT} $ 및 $H $ 게이트를 사용 하 여 메시지를 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-201">We then use the next $\operatorname{CNOT}$ and $H$ gates to move our message qubit:</span></span>

```qsharp
        CNOT(msg, here);
        H(msg);
```

### <a name="step-3--4-measuring-and-interpreting-the-result"></a><span data-ttu-id="e0451-202">3 단계 & 4 단계: 결과 측정 및 해석</span><span class="sxs-lookup"><span data-stu-id="e0451-202">Step 3 & 4: Measuring and interpreting the result</span></span>
<span data-ttu-id="e0451-203">마지막으로 @"microsoft.quantum.intrinsic.m"를 사용 하 여 `if` 문으로 표시 된 대로 측정을 수행 하 고 필요한 게이트 작업을 수행 하 여 원하는 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-203">Finally, we use @"microsoft.quantum.intrinsic.m" to perform the measurements and perform the necessary gate operations to get the desired state, as denoted by `if` statements:</span></span>

```qsharp
        // Measure out the entanglement
        if (M(msg) == One)  { Z(there); }
        if (M(here) == One) { X(there); }
```

<span data-ttu-id="e0451-204">이렇게 하면 teleportation 연산자의 정의가 완료 되므로 `here`할당을 취소 하 고 본문을 종료 하 고 작업을 종료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0451-204">This finishes the definition of our teleportation operator, so we can deallocate `here`, end the body, and end the operation.</span></span>

```qsharp
    }
}
```
