---
title: '표준 라이브러리의 오류 수정 :::no-loc(Q#):::'
description: '프로그램에서 오류 수정 코드를 사용 하는 방법에 대해 알아봅니다 :::no-loc(Q#)::: .'
author: QuantumWriter
uid: microsoft.quantum.libraries.error-correction
ms.author: martinro
ms.date: 12/11/2017
ms.topic: article
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: 94251e185cea65c5fc08ed70d5fba9b7b19501e3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92692035"
---
# <a name="error-correction"></a><span data-ttu-id="85233-103">오류 수정</span><span class="sxs-lookup"><span data-stu-id="85233-103">Error Correction</span></span> #

## <a name="introduction"></a><span data-ttu-id="85233-104">소개</span><span class="sxs-lookup"><span data-stu-id="85233-104">Introduction</span></span> ##

<span data-ttu-id="85233-105">기존 컴퓨팅에서 오류 로부터 비트를 보호 하려는 경우에는 데이터 비트를 반복 하 여 *논리 비트* 를 통해 비트를 나타내는 것이 충분할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-105">In classical computing, if one wants to protect a bit against errors, it can often suffice to represent that bit by a *logical bit* by repeating the data bit.</span></span>
<span data-ttu-id="85233-106">예를 들어 $ \overline {0} = $0은 데이터 비트 0의 인코딩입니다. 여기서 레이블 0 위의 줄을 사용 하 여 0 상태에 있는 비트의 인코딩입니다.</span><span class="sxs-lookup"><span data-stu-id="85233-106">For instance, let $\overline{0} = 000$ be the encoding of the data bit 0, where we use the a line above the label 0 to indicate that it is an encoding of a bit in the 0 state.</span></span>
<span data-ttu-id="85233-107">마찬가지로 $ \overline {1} = $111를 사용 하는 경우 단일 비트 대칭 이동 오류 로부터 보호 하는 간단한 반복 코드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-107">If we similarly let $\overline{1} = 111$, then we have a simple repetition code that protects against any one bit flip error.</span></span>
<span data-ttu-id="85233-108">즉, 3 비트 중 하나라도 대칭 이동 하는 경우 과반수 투표를 수행 하 여 논리 비트의 상태를 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-108">That is, if any of the three bits are flipped, then we can recover the state of the logical bit by taking a majority vote.</span></span>
<span data-ttu-id="85233-109">이 특정 예제에서는 클래식 오류 수정이 훨씬 더 다양 한 주제 이지만 ( [코딩 이론에 대 한 보푸라기가를 도입 하](https://www.springer.com/us/book/9783540641339)는 것이 권장 됨) 위의 반복 코드는 이미 퀀텀 정보를 보호할 때 발생할 수 있는 문제를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="85233-109">Though classical error correction is a much richer subject that this particular example (we recommend [Lint's introduction to coding theory](https://www.springer.com/us/book/9783540641339)), the repetition code above already points to a possible problem in protecting quantum information.</span></span>
<span data-ttu-id="85233-110">즉, [복제 안 함 정리](xref:microsoft.quantum.concepts.pauli#the-no-cloning-theorem) 는 각 개별의 비트를 측정 하 고 위의 클래식 코드와 유사한 방식으로 과반수 투표를 수행 하는 경우 보호 하려고 하는 정확한 정보를 잃어버린 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="85233-110">Namely, the [no-cloning theorem](xref:microsoft.quantum.concepts.pauli#the-no-cloning-theorem) implies that if we measure each individual qubit and take a majority vote by analogy to classical code above, then we have lost the precise information that we are trying to protect.</span></span>

<span data-ttu-id="85233-111">퀀텀 설정에서 측정이 문제가 있음을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-111">In the quantum setting, we will see that the measurement is problematic.</span></span> <span data-ttu-id="85233-112">위의 인코딩을 여전히 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-112">We can still implement the encoding above.</span></span>
<span data-ttu-id="85233-113">이를 통해 퀀텀 사례에 대 한 오류 수정을 일반화 하는 방법을 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-113">It is helpful to do so to see how we can generalize error correction to the quantum case.</span></span>
<span data-ttu-id="85233-114">따라서 $ \ket{\overline {0} } = \ket {000} = \ket {0} \otimes \ket {0} \otimes \ket {0} $ 및 let $ \ket{\overline {1} } = \ket $를 사용 {111} 합니다.</span><span class="sxs-lookup"><span data-stu-id="85233-114">Thus, let $\ket{\overline{0}} = \ket{000} = \ket{0} \otimes \ket{0} \otimes \ket{0}$, and let $\ket{\overline{1}} = \ket{111}$.</span></span>
<span data-ttu-id="85233-115">그런 다음, 선형으로 모든 입력에 대 한 반복 코드를 정의 했습니다. 예를 들어 $ \ket{\overline{+}} = (\ket{\overline {0} } + \ket{\overline {1} })/\sqrt {2} = (\ket {000} + \ket {111} )/\sqrt {2} $입니다.</span><span class="sxs-lookup"><span data-stu-id="85233-115">Then, by linearity, we have defined our repetition code for all inputs; for instance, $\ket{\overline{+}} = (\ket{\overline{0}} + \ket{\overline{1}}) / \sqrt{2} = (\ket{000} + \ket{111}) / \sqrt{2}$.</span></span>
<span data-ttu-id="85233-116">특히, 비트 대칭 이동 오류 $X는 중간의 두 분기에 필요한 수정 내용이 정확 하 게 $X _1 $: $ $ \begin{align} X_1 \ket{\overline{+}} & = \frac {1} {\sqrt {2} } \left (X_1 \ket {000} + X_1 \ket {111} \right) \\ \\ & = \frac {1} {\sqrt {2} } \left (\ket {010} + \ket {101} \right) 인 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-116">In particular, letting a bit-flip error $X_1$ act on the middle qubit, we see that the correction needed in both branches is precisely $X_1$: $$ \begin{align} X_1 \ket{\overline{+}} & = \frac{1}{\sqrt{2}} \left( X_1 \ket{000} + X_1 \ket{111} \right) \\\\ & = \frac{1}{\sqrt{2}} \left( \ket{010} + \ket{101} \right).</span></span>
<span data-ttu-id="85233-117">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="85233-117">\end{align} $$</span></span>

<span data-ttu-id="85233-118">보호 하려는 상태를 측정 하지 않고이를 어떻게 확인할 수 있는지 확인 하려면 각각의 서로 다른 비트 대칭 이동 오류가 다음 논리 상태에 미치는 것을 기록 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-118">To see how we can identify that this is the case without measuring the very state we are trying to protect, it is helpful to write down what each different bit flip error does to our logical states:</span></span>

| <span data-ttu-id="85233-119">오류 $E $</span><span class="sxs-lookup"><span data-stu-id="85233-119">Error $E$</span></span> | <span data-ttu-id="85233-120">$E \ket{\overline {0} } $</span><span class="sxs-lookup"><span data-stu-id="85233-120">$E\ket{\overline{0}}$</span></span> | <span data-ttu-id="85233-121">$E \ket{\overline {1} } $</span><span class="sxs-lookup"><span data-stu-id="85233-121">$E\ket{\overline{1}}$</span></span> |
| --- | --- | --- |
| <span data-ttu-id="85233-122">$\boldone$</span><span class="sxs-lookup"><span data-stu-id="85233-122">$\boldone$</span></span> | <span data-ttu-id="85233-123">$ \ket {000} $</span><span class="sxs-lookup"><span data-stu-id="85233-123">$\ket{000}$</span></span> | <span data-ttu-id="85233-124">$ \ket {111} $</span><span class="sxs-lookup"><span data-stu-id="85233-124">$\ket{111}$</span></span> |
| <span data-ttu-id="85233-125">$X_0$</span><span class="sxs-lookup"><span data-stu-id="85233-125">$X_0$</span></span> | <span data-ttu-id="85233-126">$ \ket {100} $</span><span class="sxs-lookup"><span data-stu-id="85233-126">$\ket{100}$</span></span> | <span data-ttu-id="85233-127">$ \ket {011} $</span><span class="sxs-lookup"><span data-stu-id="85233-127">$\ket{011}$</span></span> |
| <span data-ttu-id="85233-128">$X_1$</span><span class="sxs-lookup"><span data-stu-id="85233-128">$X_1$</span></span> | <span data-ttu-id="85233-129">$ \ket {010} $</span><span class="sxs-lookup"><span data-stu-id="85233-129">$\ket{010}$</span></span> | <span data-ttu-id="85233-130">$ \ket {101} $</span><span class="sxs-lookup"><span data-stu-id="85233-130">$\ket{101}$</span></span> |
| <span data-ttu-id="85233-131">$X_2$</span><span class="sxs-lookup"><span data-stu-id="85233-131">$X_2$</span></span> | <span data-ttu-id="85233-132">$ \ket {001} $</span><span class="sxs-lookup"><span data-stu-id="85233-132">$\ket{001}$</span></span> | <span data-ttu-id="85233-133">$ \ket {110} $</span><span class="sxs-lookup"><span data-stu-id="85233-133">$\ket{110}$</span></span> |

<span data-ttu-id="85233-134">인코딩할 상태를 보호 하기 위해 $ \ket{\overline {0} } $ 및 $ \ket{\overline} $를 구별 하지 않고 세 개의 오류와 id $ \boldone $를 구별할 수 있어야 합니다 {1} .</span><span class="sxs-lookup"><span data-stu-id="85233-134">In order to protect the state that we're encoding, we need to be able to distinguish the three errors from each other and from the identity $\boldone$ without distinguishing between $\ket{\overline{0}}$ and $\ket{\overline{1}}$.</span></span>
<span data-ttu-id="85233-135">예를 들어 _0 $ $Z를 측정 하 {0} 는 경우 오류 없음 사례에서 $ \ket{\overline} $ 및 $ \ket{\overline} $에 대해 다른 결과를 얻게 {1} 되므로는 인코딩된 상태를 축소 합니다.</span><span class="sxs-lookup"><span data-stu-id="85233-135">For example, if we measure $Z_0$, we get a different result for $\ket{\overline{0}}$ and $\ket{\overline{1}}$ in the no-error case, so that collapses the encoded state.</span></span>
<span data-ttu-id="85233-136">반면, 각 계산 기준 상태에서 처음 두 비트의 패리티 $Z _0 Z_1 $을 측정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-136">On the other hand, consider measuring $Z_0 Z_1$, the parity of the first two bits in each computational basis state.</span></span>
<span data-ttu-id="85233-137">Pauli 연산자의 각 측정 측정은 측정 되는 상태에 해당 하는 eigenvalue를 확인 하므로, 위의 표에 있는 각 state $ \ket{\psi} $에 대해 $Z _0 Z_1 \ket{\psi} $을 계산 하 여 $ \pm\ket{\psi} $가 있는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-137">Recall that each measurement of a Pauli operator checks which eigenvalue  the state being measured corresponds to, so for each state $\ket{\psi}$ in the table above, we can compute $Z_0 Z_1 \ket{\psi}$ to see if we get $\pm\ket{\psi}$.</span></span>
<span data-ttu-id="85233-138">$Z _0 Z_1 \ket {000} = \ket {000} $ 이며 {111} {111} 이 측정값이 두 인코딩된 상태에 대해 동일한 작업을 수행 하는 것으로 결론을 Z_1 $Z 합니다.</span><span class="sxs-lookup"><span data-stu-id="85233-138">Note that $Z_0 Z_1 \ket{000} = \ket{000}$ and that $Z_0 Z_1 \ket{111} = \ket{111}$, so that we conclude that this measurement does the same thing to both encoded states.</span></span>
<span data-ttu-id="85233-139">반면에 _0 Z_1 \ket {100} =-\ket {100} $ 및 $Z _0 Z_1 \ket {011} =-\ket $를 $Z 합니다 {011} . 따라서 $Z _0 Z_1 $를 측정 하면 발생 한 오류에 대 한 유용한 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85233-139">On the other hand, $Z_0 Z_1 \ket{100} = - \ket{100}$ and $Z_0 Z_1 \ket{011} = -\ket{011}$, so the result of measuring $Z_0 Z_1$ reveals useful information about which error occurred.</span></span>

<span data-ttu-id="85233-140">이를 강조 하기 위해 위의 표를 반복 하지만 각 행에 $Z _0 Z_1 $ 및 $Z _1 Z_2 $의 측정 결과를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="85233-140">To emphasize this, we repeat the table above, but add the results of measuring $Z_0 Z_1$ and $Z_1 Z_2$ on each row.</span></span>
<span data-ttu-id="85233-141">각 측정 결과는 :::no-loc(Q#)::: `Result` 각각 및의 값에 해당 하는 $ + $ 또는 $-$ 중에서 관찰 된 eigenvalue의 부호를 기준으로 합니다 `Zero` `One` .</span><span class="sxs-lookup"><span data-stu-id="85233-141">We denote the results of each measurement by the sign of the eigenvalue that is observed, either $+$ or $-$, corresponding to the :::no-loc(Q#)::: `Result` values of `Zero` and `One`, respectively.</span></span>

| <span data-ttu-id="85233-142">오류 $E $</span><span class="sxs-lookup"><span data-stu-id="85233-142">Error $E$</span></span> | <span data-ttu-id="85233-143">$E \ket{\overline {0} } $</span><span class="sxs-lookup"><span data-stu-id="85233-143">$E\ket{\overline{0}}$</span></span> | <span data-ttu-id="85233-144">$E \ket{\overline {1} } $</span><span class="sxs-lookup"><span data-stu-id="85233-144">$E\ket{\overline{1}}$</span></span> | <span data-ttu-id="85233-145">$Z _0 Z_1 $ 결과</span><span class="sxs-lookup"><span data-stu-id="85233-145">Result of $Z_0 Z_1$</span></span> | <span data-ttu-id="85233-146">$Z _1 Z_2 $의 결과</span><span class="sxs-lookup"><span data-stu-id="85233-146">Result of $Z_1 Z_2$</span></span> |
| --- | --- | --- | --- | --- |
| <span data-ttu-id="85233-147">$\boldone$</span><span class="sxs-lookup"><span data-stu-id="85233-147">$\boldone$</span></span> | <span data-ttu-id="85233-148">$ \ket {000} $</span><span class="sxs-lookup"><span data-stu-id="85233-148">$\ket{000}$</span></span> | <span data-ttu-id="85233-149">$ \ket {111} $</span><span class="sxs-lookup"><span data-stu-id="85233-149">$\ket{111}$</span></span> | $+$ | $+$ |
| <span data-ttu-id="85233-150">$X_0$</span><span class="sxs-lookup"><span data-stu-id="85233-150">$X_0$</span></span> | <span data-ttu-id="85233-151">$ \ket {100} $</span><span class="sxs-lookup"><span data-stu-id="85233-151">$\ket{100}$</span></span> | <span data-ttu-id="85233-152">$ \ket {011} $</span><span class="sxs-lookup"><span data-stu-id="85233-152">$\ket{011}$</span></span> | $-$ | $+$ |
| <span data-ttu-id="85233-153">$X_1$</span><span class="sxs-lookup"><span data-stu-id="85233-153">$X_1$</span></span> | <span data-ttu-id="85233-154">$ \ket {010} $</span><span class="sxs-lookup"><span data-stu-id="85233-154">$\ket{010}$</span></span> | <span data-ttu-id="85233-155">$ \ket {101} $</span><span class="sxs-lookup"><span data-stu-id="85233-155">$\ket{101}$</span></span> | $-$ | $-$ |
| <span data-ttu-id="85233-156">$X_2$</span><span class="sxs-lookup"><span data-stu-id="85233-156">$X_2$</span></span> | <span data-ttu-id="85233-157">$ \ket {001} $</span><span class="sxs-lookup"><span data-stu-id="85233-157">$\ket{001}$</span></span> | <span data-ttu-id="85233-158">$ \ket {110} $</span><span class="sxs-lookup"><span data-stu-id="85233-158">$\ket{110}$</span></span> | $+$ | $-$ |

<span data-ttu-id="85233-159">따라서 두 측정값의 결과는 어떤 비트 대칭 오류가 발생 했는지를 고유 하 게 결정 하지만 인코딩된 상태에 대 한 정보는 노출 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-159">Thus, the results of the two measurements uniquely determines which bit-flip error occurred, but without revealing any information about which state we encoded.</span></span>
<span data-ttu-id="85233-160">이러한 결과를 *증후군* 로 호출 하 고 증후군를 *복구* 로 발생 시킨 오류에 다시 매핑하는 프로세스를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="85233-160">We call these results a *syndrome* , and refer to the process of mapping a syndrome back to the error that caused it as *recovery* .</span></span>
<span data-ttu-id="85233-161">특히 복구는 발생 하는 증후군의 입력으로 사용 되는 *기존* 유추 프로시저 이며 발생 했을 수 있는 오류를 해결 하는 방법에 대 한 prescription를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="85233-161">In particular, we emphasize that recovery is a *classical* inference procedure which takes as its input the syndrome which occurred, and returns a prescription for how to fix any errors that may have occurred.</span></span>

> [!NOTE]
> <span data-ttu-id="85233-162">위의 비트 대칭 이동 코드는 단일 비트 대칭 오류에 대해서만 수정할 수 있습니다. 즉, `X` 단일 비트에 대해 작동 하는 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="85233-162">The bit-flip code above can only correct against single bit-flip errors; that is, an `X` operation acting on a single qubit.</span></span>
> <span data-ttu-id="85233-163">둘 이상의 `X` 추가 비트에 적용 하면 $ \ket{\overline {0} } $가 $ \ket{\overline {1} } $에 다음 복구에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="85233-163">Applying `X` to more than one qubit will map $\ket{\overline{0}}$ to $\ket{\overline{1}}$ following recovery.</span></span>
> <span data-ttu-id="85233-164">마찬가지로 단계 전환 작업을 적용 하면 $ `Z` \ket{\overline {1} } $가 $-\ket{\overline} $에 매핑되고 $ {1} \ket{\overline{+}} $가 $ \ket{\overline {-} } $로 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="85233-164">Similarly, applying a phase flip operation `Z` will map $\ket{\overline{1}}$ to $-\ket{\overline{1}}$, and hence will map $\ket{\overline{+}}$ to $\ket{\overline{-}}$.</span></span>
> <span data-ttu-id="85233-165">보다 일반적으로 더 많은 오류를 처리 하 고 $Z $ errors 및 $X $ errors를 처리 하는 코드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-165">More generally, codes can be created to handle larger number of errors, and to handle $Z$ errors as well as $X$ errors.</span></span>

<span data-ttu-id="85233-166">모든 코드 상태에서 동일한 방식으로 작동 하는 퀀텀 오류 수정의 측정을 설명할 수 있는 정보는 *안정기 정해진* 의 핵심입니다.</span><span class="sxs-lookup"><span data-stu-id="85233-166">The insight that we can describe measurements in quantum error correction that act the same way on all code states, is the essence of the *stabilizer formalism* .</span></span>
<span data-ttu-id="85233-167">:::no-loc(Q#):::라고은 안정기 코드에서의 인코딩 및 디코딩을 설명 하 고, 오류에서 복구 하는 방법을 설명 하기 위한 프레임 워크를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="85233-167">The :::no-loc(Q#)::: canon provides a framework for describing encoding into and decoding from stabilizer codes, and for describing how one recovers from errors.</span></span>
<span data-ttu-id="85233-168">이 섹션에서는 몇 가지 간단한 퀀텀 오류 수정 코드에이 프레임 워크 및 해당 응용 프로그램을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="85233-168">In this section, we describe this framework and its application to a few simple quantum error-correcting codes.</span></span>

> [!TIP]
> <span data-ttu-id="85233-169">안정기 정해진에 대 한 전체 소개는이 섹션의 범위를 벗어나는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="85233-169">A full introduction to the stabilizer formalism is beyond the scope of this section.</span></span>
> <span data-ttu-id="85233-170">[Gottesman 2009](https://arxiv.org/abs/0904.2557)에 대 한 자세한 내용은 독자를 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="85233-170">We refer readers interested in learning more to [Gottesman 2009](https://arxiv.org/abs/0904.2557).</span></span>

## <a name="representing-error-correcting-codes-in-no-locq"></a><span data-ttu-id="85233-171">오류 수정 코드 표시 :::no-loc(Q#):::</span><span class="sxs-lookup"><span data-stu-id="85233-171">Representing Error Correcting Codes in :::no-loc(Q#):::</span></span> ##

<span data-ttu-id="85233-172">오류 수정 코드를 지정 하는 데 도움이 되도록 :::no-loc(Q#)::: 라고은 다음과 같이 여러 가지 고유한 사용자 정의 형식을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="85233-172">To help specify error correcting codes, the :::no-loc(Q#)::: canon provides several distinct user-defined types:</span></span>

- <span data-ttu-id="85233-173"><xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister>`= Qubit[]`: 비트 레지스터는 오류 수정 코드의 코드 블록으로 해석 되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="85233-173"><xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister> `= Qubit[]`: Denotes that a register of qubits should be interpreted as the code block of an error-correcting code.</span></span>
- <span data-ttu-id="85233-174"><xref:Microsoft.Quantum.ErrorCorrection.Syndrome>`= Result[]`: 측정 결과 배열을 코드 블록에서 측정 된 증후군 해석 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="85233-174"><xref:Microsoft.Quantum.ErrorCorrection.Syndrome> `= Result[]`: Denotes that an array of measurement results should be interpreted as the syndrome measured on a code block.</span></span>
- <span data-ttu-id="85233-175"><xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn>`= (Syndrome -> Pauli[])`: *기존* 함수를 사용 하 여 증후군를 해석 하 고 적용 해야 하는 수정 사항을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="85233-175"><xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn> `= (Syndrome -> Pauli[])`: Denotes that a *classical* function should be used to interpret a syndrome and return a correction that should be applied.</span></span>
- <span data-ttu-id="85233-176"><xref:Microsoft.Quantum.ErrorCorrection.EncodeOp>`= ((Qubit[], Qubit[]) => LogicalRegister)`: 오류 수정 코드의 코드 블록을 생성 하기 위해 작업에서 새로운 ancilla 된 비트와 함께 데이터를 표현 하는 데 필요한 비트를 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="85233-176"><xref:Microsoft.Quantum.ErrorCorrection.EncodeOp> `= ((Qubit[], Qubit[]) => LogicalRegister)`: Denotes that an operation takes qubits representing data along with fresh ancilla qubits in order to produce a code block of an error-correcting code.</span></span>
- <span data-ttu-id="85233-177"><xref:Microsoft.Quantum.ErrorCorrection.DecodeOp>`= (LogicalRegister => (Qubit[], Qubit[]))`: 분해는 작업에서 코드 블록을 데이터 요소에 수정 하 고 증후군 정보를 나타내는 데 사용 되는 ancilla을 사용 하는 작업을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="85233-177"><xref:Microsoft.Quantum.ErrorCorrection.DecodeOp> `= (LogicalRegister => (Qubit[], Qubit[]))`: Denotes than an operation decomposes a code block of an error correcting code into the data qubits and the ancilla qubits used to represent syndrome information.</span></span>
- <span data-ttu-id="85233-178"><xref:Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp>`= (LogicalRegister => Syndrome)`: 코드에서 보호 되는 상태를 방해 하지 않고 코드 블록에서 증후군 정보를 추출 하는 데 사용 해야 하는 작업을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="85233-178"><xref:Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp> `= (LogicalRegister => Syndrome)`: Denotes an operation that should be used to extract syndrome information from a code block, without disturbing the state protected by the code.</span></span>

<span data-ttu-id="85233-179">마지막으로 라고은 <xref:Microsoft.Quantum.ErrorCorrection.QECC> 퀀텀 오류 수정 코드를 정의 하는 데 필요한 다른 형식을 수집 하기 위한 형식을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="85233-179">Finally, the canon provides the <xref:Microsoft.Quantum.ErrorCorrection.QECC> type to collect the other types required to define a quantum error-correcting code.</span></span> <span data-ttu-id="85233-180">각 안정기 퀀텀 코드와 연결 된 코드 $n 길이는 $, logical st$d bits의 숫자 $k $, ⟦ $n $, $k $, $d $ ⟧ 표기법에서 편리 하 게 그룹화 되는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="85233-180">Associated with each stabilizer quantum code is the code length $n$, the number $k$ of logical qubits, and the minimum distance $d$, often conveniently grouped together in the notation ⟦$n$, $k$, $d$⟧.</span></span> <span data-ttu-id="85233-181">예를 들어 <xref:Microsoft.Quantum.ErrorCorrection.BitFlipCode> 함수는 ⟦ 3, 1, 1 ⟧ 비트 대칭 코드를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="85233-181">For example, the <xref:Microsoft.Quantum.ErrorCorrection.BitFlipCode> function defines the ⟦3, 1, 1⟧ bit flip code:</span></span>

```qsharp
let encodeOp = EncodeOp(BitFlipEncoder);
let decodeOp = DecodeOp(BitFlipDecoder);
let syndMeasOp = SyndromeMeasOp(MeasureStabilizerGenerators([
    [PauliZ, PauliZ, PauliI],
    [PauliI, PauliZ, PauliZ]
], _, MeasureWithScratch));
let code = QECC(encodeOp, decodeOp, syndMeasOp);
```

<span data-ttu-id="85233-182">형식에는 `QECC` 복구 기능이 포함 되어 *있지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-182">Notice that the `QECC` type does *not* include a recovery function.</span></span>
<span data-ttu-id="85233-183">이렇게 하면 코드 자체의 정의를 변경 하지 않고 오류를 수정 하는 데 사용 되는 복구 기능을 변경할 수 있습니다. 이러한 기능은 특성화 측정의 피드백을 복구로 간주 되는 모델로 통합할 때 특히 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="85233-183">This allows us to change the recovery function that is used in correcting errors without changing the definition of the code itself; this ability is in particular useful when incorporating feedback from characterization measurements into the model assumed by recovery.</span></span>

<span data-ttu-id="85233-184">이러한 방식으로 코드를 정의한 후에는 작업을 사용 하 여 <xref:Microsoft.Quantum.ErrorCorrection.Recover> 오류를 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-184">Once a code is defined in this way, we can use the <xref:Microsoft.Quantum.ErrorCorrection.Recover> operation to recover from errors:</span></span>

```qsharp
let code = BitFlipCode();
let fn = BitFlipRecoveryFn();
let X0 = ApplyPauli([PauliX, PauliI, PauliI], _);
using (scratch = Qubit[nScratch]) {
    let logicalRegister = encode(data, scratch);
    // Cause an error.
    X0(logicalRegister);
    Recover(code, fn, logicalRegister);
    let (decodedData, decodedScratch) = decode(logicalRegister);
    ApplyToEach(Reset, decodedScratch);
}
```

<span data-ttu-id="85233-185">이에 대 한 자세한 내용은 [비트 대칭 코드 샘플](https://github.com/microsoft/Quantum/tree/main/samples/error-correction/bit-flip-code)을 살펴보세요.</span><span class="sxs-lookup"><span data-stu-id="85233-185">We explore this in more detail in the [bit flip code sample](https://github.com/microsoft/Quantum/tree/main/samples/error-correction/bit-flip-code).</span></span>

<span data-ttu-id="85233-186">비트 대칭 코드 외에도 :::no-loc(Q#)::: 라고은 [5 ~ 5 비트 코드](https://arxiv.org/abs/quant-ph/9602019)및 [일곱 번째 비트 코드](https://arxiv.org/abs/quant-ph/9705052)의 구현과 함께 제공 되며, 둘 다 임의의 단일 기능 비트 오류를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85233-186">Aside from the bit-flip code, the :::no-loc(Q#)::: canon is provided with implementations of the [five-qubit perfect code](https://arxiv.org/abs/quant-ph/9602019), and the [seven-qubit code](https://arxiv.org/abs/quant-ph/9705052), both of which can correct an arbitrary single-qubit error.</span></span>
