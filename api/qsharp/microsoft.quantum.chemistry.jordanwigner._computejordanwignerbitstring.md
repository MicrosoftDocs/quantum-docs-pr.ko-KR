---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: _ComputeJordanWignerBitString 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 31b957a435c3f578bc03d432609cde14c2ef5ced
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714701"
---
# <a name="_computejordanwignerbitstring-function"></a><span data-ttu-id="5c1e1-102">_ComputeJordanWignerBitString 함수</span><span class="sxs-lookup"><span data-stu-id="5c1e1-102">_ComputeJordanWignerBitString function</span></span>

<span data-ttu-id="5c1e1-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="5c1e1-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="5c1e1-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5c1e1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5c1e1-105">Fermion 개의 생성/annihilation 연산자를 사용 하 여 fermionic 연산자의 인덱스 사이에서 요르단 – Wigner 문자열의 Z 구성 요소를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1e1-105">Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.</span></span>

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a><span data-ttu-id="5c1e1-106">입력</span><span class="sxs-lookup"><span data-stu-id="5c1e1-106">Input</span></span>

### <a name="nfermions--int"></a><span data-ttu-id="5c1e1-107">nFermions: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5c1e1-107">nFermions : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5c1e1-108">시스템의 fermions 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1e1-108">The Number of fermions in the system.</span></span>


### <a name="idxfermions--int"></a><span data-ttu-id="5c1e1-109">idxFermions: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5c1e1-109">idxFermions : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5c1e1-110">fermionic 연산자 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1e1-110">fermionic operator indices.</span></span>



## <a name="output--bool"></a><span data-ttu-id="5c1e1-111">Output: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="5c1e1-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="5c1e1-112">`Bool[]` `true` 를 적용 해야 하는 비트 문자열입니다 `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="5c1e1-112">Bitstring `Bool[]` that is `true` where a `PauliZ` should be applied.</span></span>