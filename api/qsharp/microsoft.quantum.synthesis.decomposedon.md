---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: DecomposedOn 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: fb7aa5af8f3eb07399e0d2dd2d50723f4e6b169a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855520"
---
# <a name="decomposedon-function"></a><span data-ttu-id="85fd2-102">DecomposedOn 함수</span><span class="sxs-lookup"><span data-stu-id="85fd2-102">DecomposedOn function</span></span>

<span data-ttu-id="85fd2-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="85fd2-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="85fd2-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="85fd2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="85fd2-105">변수에서 순열 분해</span><span class="sxs-lookup"><span data-stu-id="85fd2-105">Decomposes a permutation on a variable</span></span>

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a><span data-ttu-id="85fd2-106">설명</span><span class="sxs-lookup"><span data-stu-id="85fd2-106">Description</span></span>

<span data-ttu-id="85fd2-107">순열 $ \pi $ ( `perm` ) 및 인덱스 $i $ ( `index` )이 지정 된 경우이 메서드는 세 개의 순열 $ ((\ pi_l, \ pi_r), \pi ') $를 반환 하 여 $ \ pi_l $ 및 $ \ pi_r $의 이미지가 $i $ 이외의 인덱스에 있는 요소의 비트를 변경 하지 않도록 하 고 해당 요소에서 $ \pi의 이미지를 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="85fd2-107">Given a permutation $\pi$ (`perm`) and an index $i$ (`index`), this method returns three permutations $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>

## <a name="input"></a><span data-ttu-id="85fd2-108">입력</span><span class="sxs-lookup"><span data-stu-id="85fd2-108">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="85fd2-109">perm: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="85fd2-109">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="index--int"></a><span data-ttu-id="85fd2-110">인덱스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="85fd2-110">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intintint"></a><span data-ttu-id="85fd2-111">Output: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="85fd2-111">Output : (([Int](xref:microsoft.quantum.lang-ref.int)[],[Int](xref:microsoft.quantum.lang-ref.int)[]),[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>



## <a name="example"></a><span data-ttu-id="85fd2-112">예</span><span class="sxs-lookup"><span data-stu-id="85fd2-112">Example</span></span>

<span data-ttu-id="85fd2-113">입력이 perm = [0, 2, 3, 5, 7, 1, 4, 6] 및 인덱스 = 0 인 것으로 가정 합니다 .이 함수는 다음 표를 기준으로 세 개의 순열 ( `perm` 그룹 A의 요소와 그룹 D의 이미지)을 포함 하는 이진 표기법의 순열 목록을 계산 합니다.  열에는 비트 인덱스가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85fd2-113">Assume that the input is perm = [0, 2, 3, 5, 7, 1, 4, 6] and index = 0, then this function computes three permutations based on the following table, which lists the permutation `perm` in binary notation with elements in group A and images in group D.  The columns list the bit indices.</span></span>

<span data-ttu-id="85fd2-114">|   A |   B |   C |   D |</span><span class="sxs-lookup"><span data-stu-id="85fd2-114">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="85fd2-115">2 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-115">2 1 0</span></span> | <span data-ttu-id="85fd2-116">2 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-116">2 1 0</span></span> | <span data-ttu-id="85fd2-117">2 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-117">2 1 0</span></span> | <span data-ttu-id="85fd2-118">2 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-118">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="85fd2-119">0 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-119">0 0 0</span></span> |       |       | <span data-ttu-id="85fd2-120">0 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-120">0 0 0</span></span> | <span data-ttu-id="85fd2-121">0</span><span class="sxs-lookup"><span data-stu-id="85fd2-121">0</span></span>
| <span data-ttu-id="85fd2-122">0 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-122">0 0 1</span></span> |       |       | <span data-ttu-id="85fd2-123">0 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-123">0 1 0</span></span> | <span data-ttu-id="85fd2-124">2</span><span class="sxs-lookup"><span data-stu-id="85fd2-124">2</span></span>
| <span data-ttu-id="85fd2-125">0 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-125">0 1 0</span></span> |       |       | <span data-ttu-id="85fd2-126">0 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-126">0 1 1</span></span> | <span data-ttu-id="85fd2-127">3</span><span class="sxs-lookup"><span data-stu-id="85fd2-127">3</span></span>
| <span data-ttu-id="85fd2-128">0 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-128">0 1 1</span></span> |       |       | <span data-ttu-id="85fd2-129">1 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-129">1 0 1</span></span> | <span data-ttu-id="85fd2-130">5</span><span class="sxs-lookup"><span data-stu-id="85fd2-130">5</span></span>
| <span data-ttu-id="85fd2-131">1 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-131">1 0 0</span></span> |       |       | <span data-ttu-id="85fd2-132">1 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-132">1 1 1</span></span> | <span data-ttu-id="85fd2-133">7</span><span class="sxs-lookup"><span data-stu-id="85fd2-133">7</span></span>
| <span data-ttu-id="85fd2-134">1 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-134">1 0 1</span></span> |       |       | <span data-ttu-id="85fd2-135">0 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-135">0 0 1</span></span> | <span data-ttu-id="85fd2-136">1</span><span class="sxs-lookup"><span data-stu-id="85fd2-136">1</span></span>
| <span data-ttu-id="85fd2-137">1 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-137">1 1 0</span></span> |       |       | <span data-ttu-id="85fd2-138">1 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-138">1 0 0</span></span> | <span data-ttu-id="85fd2-139">4</span><span class="sxs-lookup"><span data-stu-id="85fd2-139">4</span></span>
| <span data-ttu-id="85fd2-140">1 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-140">1 1 1</span></span> |       |       | <span data-ttu-id="85fd2-141">1 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-141">1 1 0</span></span> | <span data-ttu-id="85fd2-142">6</span><span class="sxs-lookup"><span data-stu-id="85fd2-142">6</span></span>

<span data-ttu-id="85fd2-143">인덱스의 모든 값이 0 (= 인덱스)이 아닌 경우 A에서 B로, D에서 C로 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85fd2-143">All values for indices not equal to 0 (= index) are copied from A to B and from D to C.</span></span>

<span data-ttu-id="85fd2-144">|   A |   B |   C |   D |</span><span class="sxs-lookup"><span data-stu-id="85fd2-144">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="85fd2-145">2 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-145">2 1 0</span></span> | <span data-ttu-id="85fd2-146">2 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-146">2 1 0</span></span> | <span data-ttu-id="85fd2-147">2 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-147">2 1 0</span></span> | <span data-ttu-id="85fd2-148">2 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-148">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="85fd2-149">0 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-149">0 0 0</span></span> | <span data-ttu-id="85fd2-150">0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-150">0 0</span></span>   | <span data-ttu-id="85fd2-151">0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-151">0 0</span></span>   | <span data-ttu-id="85fd2-152">0 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-152">0 0 0</span></span> |
| <span data-ttu-id="85fd2-153">0 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-153">0 0 1</span></span> | <span data-ttu-id="85fd2-154">0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-154">0 0</span></span>   | <span data-ttu-id="85fd2-155">0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-155">0 1</span></span>   | <span data-ttu-id="85fd2-156">0 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-156">0 1 0</span></span> |
| <span data-ttu-id="85fd2-157">0 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-157">0 1 0</span></span> | <span data-ttu-id="85fd2-158">0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-158">0 1</span></span>   | <span data-ttu-id="85fd2-159">0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-159">0 1</span></span>   | <span data-ttu-id="85fd2-160">0 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-160">0 1 1</span></span> |
| <span data-ttu-id="85fd2-161">0 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-161">0 1 1</span></span> | <span data-ttu-id="85fd2-162">0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-162">0 1</span></span>   | <span data-ttu-id="85fd2-163">1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-163">1 0</span></span>   | <span data-ttu-id="85fd2-164">1 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-164">1 0 1</span></span> |
| <span data-ttu-id="85fd2-165">1 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-165">1 0 0</span></span> | <span data-ttu-id="85fd2-166">1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-166">1 0</span></span>   | <span data-ttu-id="85fd2-167">1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-167">1 1</span></span>   | <span data-ttu-id="85fd2-168">1 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-168">1 1 1</span></span> |
| <span data-ttu-id="85fd2-169">1 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-169">1 0 1</span></span> | <span data-ttu-id="85fd2-170">1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-170">1 0</span></span>   | <span data-ttu-id="85fd2-171">0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-171">0 0</span></span>   | <span data-ttu-id="85fd2-172">0 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-172">0 0 1</span></span> |
| <span data-ttu-id="85fd2-173">1 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-173">1 1 0</span></span> | <span data-ttu-id="85fd2-174">1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-174">1 1</span></span>   | <span data-ttu-id="85fd2-175">1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-175">1 0</span></span>   | <span data-ttu-id="85fd2-176">1 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-176">1 0 0</span></span> |
| <span data-ttu-id="85fd2-177">1 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-177">1 1 1</span></span> | <span data-ttu-id="85fd2-178">1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-178">1 1</span></span>   | <span data-ttu-id="85fd2-179">1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-179">1 1</span></span>   | <span data-ttu-id="85fd2-180">1 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-180">1 1 0</span></span> |

<span data-ttu-id="85fd2-181">다음은 블록 B의 열 0에 빈 인덱스가 있는 첫 번째 요소에 대해 0이 배치 된 다음 1이 B에 배치 되 고 (첫 번째 경우에는 인덱스가 0 0 인 다른 행) B에 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85fd2-181">Next a 0 is placed for the first element with an empty index at column 0 in block B and then a 1 is placed in B where the prefix matches (in the first case the other row with indices 0 0).</span></span>
<span data-ttu-id="85fd2-182">그런 다음 블록 C의 동일한 행에 1이 추가 된 다음 블록 C의 해당 접두사에 대해 0이 추가 됩니다.  이 프로세스는 모든 인덱스가 B 및 C 블록의 0 열에 배치 될 때까지 반복 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85fd2-182">Afterwards, a 1 is added in the same row in block C, and then a 0 for the corresponding prefix in block C.  This process is repeated, until all indices have been placed in column 0 in blocks B and C.</span></span>

<span data-ttu-id="85fd2-183">|   A |   B |   C |   D |</span><span class="sxs-lookup"><span data-stu-id="85fd2-183">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="85fd2-184">2 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-184">2 1 0</span></span> | <span data-ttu-id="85fd2-185">2 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-185">2 1 0</span></span> | <span data-ttu-id="85fd2-186">2 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-186">2 1 0</span></span> | <span data-ttu-id="85fd2-187">2 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-187">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="85fd2-188">0 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-188">0 0 0</span></span> | <span data-ttu-id="85fd2-189">0 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-189">0 0 0</span></span> | <span data-ttu-id="85fd2-190">0 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-190">0 0 0</span></span> | <span data-ttu-id="85fd2-191">0 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-191">0 0 0</span></span> |
| <span data-ttu-id="85fd2-192">0 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-192">0 0 1</span></span> | <span data-ttu-id="85fd2-193">0 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-193">0 0 1</span></span> | <span data-ttu-id="85fd2-194">0 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-194">0 1 1</span></span> | <span data-ttu-id="85fd2-195">0 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-195">0 1 0</span></span> |
| <span data-ttu-id="85fd2-196">0 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-196">0 1 0</span></span> | <span data-ttu-id="85fd2-197">0 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-197">0 1 0</span></span> | <span data-ttu-id="85fd2-198">0 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-198">0 1 0</span></span> | <span data-ttu-id="85fd2-199">0 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-199">0 1 1</span></span> |
| <span data-ttu-id="85fd2-200">0 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-200">0 1 1</span></span> | <span data-ttu-id="85fd2-201">0 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-201">0 1 1</span></span> | <span data-ttu-id="85fd2-202">1 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-202">1 0 1</span></span> | <span data-ttu-id="85fd2-203">1 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-203">1 0 1</span></span> |
| <span data-ttu-id="85fd2-204">1 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-204">1 0 0</span></span> | <span data-ttu-id="85fd2-205">1 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-205">1 0 0</span></span> | <span data-ttu-id="85fd2-206">1 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-206">1 1 0</span></span> | <span data-ttu-id="85fd2-207">1 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-207">1 1 1</span></span> |
| <span data-ttu-id="85fd2-208">1 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-208">1 0 1</span></span> | <span data-ttu-id="85fd2-209">1 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-209">1 0 1</span></span> | <span data-ttu-id="85fd2-210">0 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-210">0 0 1</span></span> | <span data-ttu-id="85fd2-211">0 0 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-211">0 0 1</span></span> |
| <span data-ttu-id="85fd2-212">1 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-212">1 1 0</span></span> | <span data-ttu-id="85fd2-213">1 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-213">1 1 0</span></span> | <span data-ttu-id="85fd2-214">1 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-214">1 0 0</span></span> | <span data-ttu-id="85fd2-215">1 0 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-215">1 0 0</span></span> |
| <span data-ttu-id="85fd2-216">1 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-216">1 1 1</span></span> | <span data-ttu-id="85fd2-217">1 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-217">1 1 1</span></span> | <span data-ttu-id="85fd2-218">1 1 1</span><span class="sxs-lookup"><span data-stu-id="85fd2-218">1 1 1</span></span> | <span data-ttu-id="85fd2-219">1 1 0</span><span class="sxs-lookup"><span data-stu-id="85fd2-219">1 1 0</span></span> |

<span data-ttu-id="85fd2-220">테이블에서 다음과 같은 세 가지 새 순열을 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85fd2-220">We can read three new permutations from the table:</span></span>

- <span data-ttu-id="85fd2-221">$ \ pi_l $ (요소 포함), B의 이미지 (왼쪽)</span><span class="sxs-lookup"><span data-stu-id="85fd2-221">$\pi_l$ with elements in A, images in B (left)</span></span>
- <span data-ttu-id="85fd2-222">D의 요소가 포함 된 $ \ pi_r $, C (오른쪽)의 이미지</span><span class="sxs-lookup"><span data-stu-id="85fd2-222">$\pi_r$ with elements in D, images in C (right)</span></span>
- <span data-ttu-id="85fd2-223">$ \pi ' $ (B의 요소 포함), C의 이미지 (나머지)</span><span class="sxs-lookup"><span data-stu-id="85fd2-223">$\pi'$  with elements in B, images in C (remainder)</span></span>

<span data-ttu-id="85fd2-224">인덱스 1과 2에 대 한 $ \ pi_l $ 및 $ \ pi_r $에서 디자인 비트 값은 변경 되지 않으며 인덱스 0의 경우 $ \ pi_ ' $의 비트 값은 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85fd2-224">Note that by design bit values do not change in $\pi_l$ and $\pi_r$ for indices 1 and 2, and bit values do not change for in $\pi_'$ for index 0.</span></span>  <span data-ttu-id="85fd2-225">또한 $ \ pi_l $ 및 $ \ pi_r $은 (는) 자체 역 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="85fd2-225">Also note that $\pi_l$ and $\pi_r$ must be self-inverse.</span></span>

<span data-ttu-id="85fd2-226">파생 된 순열 및 반환 된 순열: left = [0, 1, 2, 3, 4, 5, 6, 7] right = [0, 1, 3, 2, 4, 5, 7, 6] 나머지가 = [0, 3, 2, 5, 6, 1, 4, 7]</span><span class="sxs-lookup"><span data-stu-id="85fd2-226">The derived and returned permutations are: left      = [0, 1, 2, 3, 4, 5, 6, 7] right     = [0, 1, 3, 2, 4, 5, 7, 6] remainder = [0, 3, 2, 5, 6, 1, 4, 7]</span></span>