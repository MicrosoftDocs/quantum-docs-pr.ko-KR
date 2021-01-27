---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver
title: ApplyOpRepeatedlyOver 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOver
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 263eff8ec31f5ee36485eb1d2ed52bf15cef4bef
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844793"
---
# <a name="applyoprepeatedlyover-operation"></a><span data-ttu-id="c32e1-102">ApplyOpRepeatedlyOver 작업</span><span class="sxs-lookup"><span data-stu-id="c32e1-102">ApplyOpRepeatedlyOver operation</span></span>

<span data-ttu-id="c32e1-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c32e1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c32e1-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c32e1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c32e1-105">단일 비트 레지스터에 대해 동일한 op를 여러 번 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c32e1-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOver (op : (Qubit[] => Unit), targets : Int[][], register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c32e1-106">입력</span><span class="sxs-lookup"><span data-stu-id="c32e1-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="c32e1-107">op:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c32e1-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c32e1-108">이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c32e1-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="c32e1-109">대상: [Int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="c32e1-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="c32e1-110">Op의 대상을 설명 하는 중첩 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="c32e1-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="c32e1-111">각 배열에는 사용할 비트를 설명 하는 정수 목록이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c32e1-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="c32e1-112">register: [](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c32e1-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c32e1-113">작업할의 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="c32e1-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c32e1-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c32e1-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="c32e1-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c32e1-115">See Also</span></span>

- [<span data-ttu-id="c32e1-116">ApplySeriesOfOps입니다.</span><span class="sxs-lookup"><span data-stu-id="c32e1-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)