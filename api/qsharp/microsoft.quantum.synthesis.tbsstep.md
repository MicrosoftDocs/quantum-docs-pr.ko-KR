---
uid: Microsoft.Quantum.Synthesis.TBSStep
title: TBSStep 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: TBSStep
qsharp.summary: Computes gate masks to transform perm[x] to x and updates the current permutation.
ms.openlocfilehash: b33269afc2ac14106a18a09e855a8d067b9c558b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725450"
---
# <a name="tbsstep-function"></a><span data-ttu-id="768ba-102">TBSStep 함수</span><span class="sxs-lookup"><span data-stu-id="768ba-102">TBSStep function</span></span>

<span data-ttu-id="768ba-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="768ba-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="768ba-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="768ba-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="768ba-105">[X] perm을 x로 변환 하 고 현재 순열을 업데이트 하는 게이트 마스크를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="768ba-105">Computes gate masks to transform perm[x] to x and updates the current permutation.</span></span>

```qsharp
function TBSStep (state : (Int[], Microsoft.Quantum.Synthesis.MCMTMask[]), x : Int) : (Int[], Microsoft.Quantum.Synthesis.MCMTMask[])
```


## <a name="input"></a><span data-ttu-id="768ba-106">입력</span><span class="sxs-lookup"><span data-stu-id="768ba-106">Input</span></span>

### <a name="state--intmcmtmask"></a><span data-ttu-id="768ba-107">상태: ([Int](xref:microsoft.quantum.lang-ref.int)[],[mcmtmask](xref:Microsoft.Quantum.Synthesis.MCMTMask)[])</span><span class="sxs-lookup"><span data-stu-id="768ba-107">state : ([Int](xref:microsoft.quantum.lang-ref.int)[],[MCMTMask](xref:Microsoft.Quantum.Synthesis.MCMTMask)[])</span></span>




### <a name="x--int"></a><span data-ttu-id="768ba-108">x: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="768ba-108">x : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intmcmtmask"></a><span data-ttu-id="768ba-109">Output: ([Int](xref:microsoft.quantum.lang-ref.int)[],[mcmtmask](xref:Microsoft.Quantum.Synthesis.MCMTMask)[])</span><span class="sxs-lookup"><span data-stu-id="768ba-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int)[],[MCMTMask](xref:Microsoft.Quantum.Synthesis.MCMTMask)[])</span></span>

