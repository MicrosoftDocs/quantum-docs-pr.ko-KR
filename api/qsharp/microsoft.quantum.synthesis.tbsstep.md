---
uid: Microsoft.Quantum.Synthesis.TBSStep
title: TBSStep 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: TBSStep
qsharp.summary: Computes gate masks to transform perm[x] to x and updates the current permutation.
ms.openlocfilehash: 272ab3221e02127074fe6bfc65aee47c40eb88b5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231061"
---
# <a name="tbsstep-function"></a><span data-ttu-id="c39dd-102">TBSStep 함수</span><span class="sxs-lookup"><span data-stu-id="c39dd-102">TBSStep function</span></span>

<span data-ttu-id="c39dd-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="c39dd-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="c39dd-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c39dd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c39dd-105">[X] perm을 x로 변환 하 고 현재 순열을 업데이트 하는 게이트 마스크를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="c39dd-105">Computes gate masks to transform perm[x] to x and updates the current permutation.</span></span>

```qsharp
function TBSStep (state : (Int[], Microsoft.Quantum.Synthesis.MCMTMask[]), x : Int) : (Int[], Microsoft.Quantum.Synthesis.MCMTMask[])
```


## <a name="input"></a><span data-ttu-id="c39dd-106">입력</span><span class="sxs-lookup"><span data-stu-id="c39dd-106">Input</span></span>

### <a name="state--intmcmtmask"></a><span data-ttu-id="c39dd-107">상태: ([Int](xref:microsoft.quantum.lang-ref.int)[],[mcmtmask](xref:Microsoft.Quantum.Synthesis.MCMTMask)[])</span><span class="sxs-lookup"><span data-stu-id="c39dd-107">state : ([Int](xref:microsoft.quantum.lang-ref.int)[],[MCMTMask](xref:Microsoft.Quantum.Synthesis.MCMTMask)[])</span></span>




### <a name="x--int"></a><span data-ttu-id="c39dd-108">x: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c39dd-108">x : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intmcmtmask"></a><span data-ttu-id="c39dd-109">Output: ([Int](xref:microsoft.quantum.lang-ref.int)[],[mcmtmask](xref:Microsoft.Quantum.Synthesis.MCMTMask)[])</span><span class="sxs-lookup"><span data-stu-id="c39dd-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int)[],[MCMTMask](xref:Microsoft.Quantum.Synthesis.MCMTMask)[])</span></span>

