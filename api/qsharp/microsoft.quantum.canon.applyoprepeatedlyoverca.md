---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverCA
title: Applyoprepeatedly과잉 Ca 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverCA
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: b7d401f323d7affc27697744bb659c687e252682
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209112"
---
# <a name="applyoprepeatedlyoverca-operation"></a><span data-ttu-id="bfc1c-102">Applyoprepeatedly과잉 Ca 작업</span><span class="sxs-lookup"><span data-stu-id="bfc1c-102">ApplyOpRepeatedlyOverCA operation</span></span>

<span data-ttu-id="bfc1c-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bfc1c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bfc1c-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bfc1c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bfc1c-105">단일 비트 레지스터에 대해 동일한 op를 여러 번 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc1c-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOverCA (op : (Qubit[] => Unit is Adj + Ctl), targets : Int[][], register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="bfc1c-106">입력</span><span class="sxs-lookup"><span data-stu-id="bfc1c-106">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="bfc1c-107">op: [이상](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Adj + Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc1c-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="bfc1c-108">이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc1c-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="bfc1c-109">대상: [Int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="bfc1c-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="bfc1c-110">Op의 대상을 설명 하는 중첩 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc1c-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="bfc1c-111">각 배열에는 사용할 비트를 설명 하는 정수 목록이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc1c-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="bfc1c-112">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="bfc1c-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bfc1c-113">작업할의 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc1c-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bfc1c-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bfc1c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="bfc1c-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="bfc1c-115">See Also</span></span>

- [<span data-ttu-id="bfc1c-116">ApplySeriesOfOps입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc1c-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)