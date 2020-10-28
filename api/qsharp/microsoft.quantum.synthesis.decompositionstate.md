---
uid: Microsoft.Quantum.Synthesis.DecompositionState
title: DecompositionState 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecompositionState
qsharp.summary: State during decomposition based on variable indexes
ms.openlocfilehash: 0547c04828a80b4f696cc17e13c8cc57d0379f96
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725212"
---
# <a name="decompositionstate-user-defined-type"></a><span data-ttu-id="8c872-102">DecompositionState 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="8c872-102">DecompositionState user defined type</span></span>

<span data-ttu-id="8c872-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="8c872-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="8c872-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8c872-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8c872-105">변수 인덱스를 기반으로 분해 하는 동안의 상태</span><span class="sxs-lookup"><span data-stu-id="8c872-105">State during decomposition based on variable indexes</span></span>

```qsharp

newtype DecompositionState = (Perm : Int[], Lfunctions : (BigInt, Int)[], Rfunctions : (BigInt, Int)[]);
```



## <a name="named-items"></a><span data-ttu-id="8c872-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="8c872-106">Named Items</span></span>

### <a name="perm--int"></a><span data-ttu-id="8c872-107">Perm: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="8c872-107">Perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>


### <a name="lfunctions--bigintint"></a><span data-ttu-id="8c872-108">Lfunctions: ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="8c872-108">Lfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>


### <a name="rfunctions--bigintint"></a><span data-ttu-id="8c872-109">Rfunctions: ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="8c872-109">Rfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>



## <a name="description"></a><span data-ttu-id="8c872-110">Description</span><span class="sxs-lookup"><span data-stu-id="8c872-110">Description</span></span>

<span data-ttu-id="8c872-111">상태에는 현재 순열 및 왼쪽의 제어 된 게이트에 대해 현재 생성 된 함수와 오른쪽의 제어 된 게이트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c872-111">The state holds the current permutation and the currently generated functions for controlled gates on the left, and controlled gates on the right.</span></span>