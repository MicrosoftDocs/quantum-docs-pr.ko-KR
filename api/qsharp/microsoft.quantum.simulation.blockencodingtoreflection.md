---
uid: Microsoft.Quantum.Simulation.BlockEncodingToReflection
title: BlockEncodingToReflection 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingToReflection
qsharp.summary: >-
  Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.

  That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$. This increases the size of the auxiliary register of $U$ by one qubit.
ms.openlocfilehash: 742d4f5623c7c26810998f6c96e2c7b05cc452d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225349"
---
# <a name="blockencodingtoreflection-function"></a><span data-ttu-id="685dc-102">BlockEncodingToReflection 함수</span><span class="sxs-lookup"><span data-stu-id="685dc-102">BlockEncodingToReflection function</span></span>

<span data-ttu-id="685dc-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="685dc-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="685dc-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="685dc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="685dc-105">을 해당 하는으로 변환 합니다 `BlockEncoding` `BLockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="685dc-105">Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.</span></span>

<span data-ttu-id="685dc-106">즉, 특정 `BlockEncoding` $H 연산자 ($)를 인코딩하는 단일 $U $가 지정 된 경우,이 연산자를 `BlockEncodingReflection` 동일한 연산자를 인코딩하는 $U ' $로 변환 하 고, $U ' ^ \A턴 = U ' $를 충족 합니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-106">That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$.</span></span>
<span data-ttu-id="685dc-107">그러면 $U $의 보조 레지스터 크기가 1 배 비트로 늘어납니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-107">This increases the size of the auxiliary register of $U$ by one qubit.</span></span>

```qsharp
function BlockEncodingToReflection (blockEncoding : Microsoft.Quantum.Simulation.BlockEncoding) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a><span data-ttu-id="685dc-108">입력</span><span class="sxs-lookup"><span data-stu-id="685dc-108">Input</span></span>

### <a name="blockencoding--blockencoding"></a><span data-ttu-id="685dc-109">blockEncoding: [Blockencoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)</span><span class="sxs-lookup"><span data-stu-id="685dc-109">blockEncoding : [BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)</span></span>

<span data-ttu-id="685dc-110">`BlockEncoding`리플렉션으로 변환할 단일 $U $입니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-110">A `BlockEncoding` unitary $U$ to be converted into a reflection.</span></span>



## <a name="output--blockencodingreflection"></a><span data-ttu-id="685dc-111">출력: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="685dc-111">Output : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="685dc-112">단일 $U ' $는 레지스터에 대해 공동으로 작동 `a` 하며 `s` $H $를 차단 하 고 $U ' ^ \A턴 = U ' $를 충족 합니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-112">A unitary $U'$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U'^\dagger = U'$.</span></span>

## <a name="remarks"></a><span data-ttu-id="685dc-113">설명</span><span class="sxs-lookup"><span data-stu-id="685dc-113">Remarks</span></span>

<span data-ttu-id="685dc-114">그러면 $U $의 보조 레지스터 크기가 1 배 비트로 늘어납니다.</span><span class="sxs-lookup"><span data-stu-id="685dc-114">This increases the size of the auxiliary register of $U$ by one qubit.</span></span>

## <a name="references"></a><span data-ttu-id="685dc-115">참조 항목</span><span class="sxs-lookup"><span data-stu-id="685dc-115">References</span></span>

- <span data-ttu-id="685dc-116">Hamiltonian 시뮬레이션의 Guang Jia-hao Low, Isaac Chuang https://arxiv.org/abs/1610.06546</span><span class="sxs-lookup"><span data-stu-id="685dc-116">Hamiltonian Simulation by Qubitization Guang Hao Low, Isaac L. Chuang https://arxiv.org/abs/1610.06546</span></span>

## <a name="see-also"></a><span data-ttu-id="685dc-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="685dc-117">See Also</span></span>

- [<span data-ttu-id="685dc-118">Microsoft 양자. 블록 인코딩</span><span class="sxs-lookup"><span data-stu-id="685dc-118">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="685dc-119">BlockEncodingReflection.</span><span class="sxs-lookup"><span data-stu-id="685dc-119">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)