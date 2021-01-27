---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: _ComputeJordanWignerBitString 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 82b5e433f79c93c640b89e6365e5f468bacd892e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839523"
---
# <a name="_computejordanwignerbitstring-function"></a><span data-ttu-id="c6c1f-102">_ComputeJordanWignerBitString 함수</span><span class="sxs-lookup"><span data-stu-id="c6c1f-102">_ComputeJordanWignerBitString function</span></span>

<span data-ttu-id="c6c1f-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="c6c1f-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="c6c1f-104">패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="c6c1f-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="c6c1f-105">Fermion 개의 생성/annihilation 연산자를 사용 하 여 fermionic 연산자의 인덱스 사이에서 요르단 – Wigner 문자열의 Z 구성 요소를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c1f-105">Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.</span></span>

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a><span data-ttu-id="c6c1f-106">입력</span><span class="sxs-lookup"><span data-stu-id="c6c1f-106">Input</span></span>

### <a name="nfermions--int"></a><span data-ttu-id="c6c1f-107">nFermions: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c6c1f-107">nFermions : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c6c1f-108">시스템의 fermions 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c6c1f-108">The Number of fermions in the system.</span></span>


### <a name="idxfermions--int"></a><span data-ttu-id="c6c1f-109">idxFermions: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c6c1f-109">idxFermions : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c6c1f-110">fermionic 연산자 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="c6c1f-110">fermionic operator indices.</span></span>



## <a name="output--bool"></a><span data-ttu-id="c6c1f-111">Output: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="c6c1f-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="c6c1f-112">`Bool[]` `true` 를 적용 해야 하는 비트 문자열입니다 `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="c6c1f-112">Bitstring `Bool[]` that is `true` where a `PauliZ` should be applied.</span></span>

## <a name="example"></a><span data-ttu-id="c6c1f-113">예</span><span class="sxs-lookup"><span data-stu-id="c6c1f-113">Example</span></span>

<span data-ttu-id="c6c1f-114">let bitString = _ComputeJordanWignerBitString (6, [0, 1, 2, 6]); bitString은 [false, false, false, true, true, true, false]입니다.</span><span class="sxs-lookup"><span data-stu-id="c6c1f-114">let bitString = _ComputeJordanWignerBitString(6, [0,1,2,6]) ; // bitString is [false, false, false ,true, true, true, false].</span></span>