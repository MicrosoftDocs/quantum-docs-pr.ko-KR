---
uid: Microsoft.Quantum.Intrinsic.I
title: I 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: I
qsharp.summary: Performs the identity operation (no-op) on a single qubit.
ms.openlocfilehash: 5aae7a5e3b5b441829de8f10f4df539ffc374954
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198948"
---
# <a name="i-operation"></a><span data-ttu-id="d1c1c-102">I 작업</span><span class="sxs-lookup"><span data-stu-id="d1c1c-102">I operation</span></span>

<span data-ttu-id="d1c1c-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="d1c1c-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="d1c1c-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d1c1c-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="d1c1c-105">단일 비트의 id 연산 (no op)을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c1c-105">Performs the identity operation (no-op) on a single qubit.</span></span>

```qsharp
operation I (target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d1c1c-106">입력</span><span class="sxs-lookup"><span data-stu-id="d1c1c-106">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="d1c1c-107">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d1c1c-107">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="d1c1c-108">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d1c1c-108">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d1c1c-109">설명</span><span class="sxs-lookup"><span data-stu-id="d1c1c-109">Remarks</span></span>

<span data-ttu-id="d1c1c-110">이는 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c1c-110">This is a no-op.</span></span> <span data-ttu-id="d1c1c-111">이는 완전성을 위해 제공 되며, 경우에 따라 알고리즘에서 id를 호출 하거나 매개 변수로 전달 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c1c-111">It is provided for completeness and because sometimes it is useful to call the identity in an algorithm or to pass it as a parameter.</span></span>