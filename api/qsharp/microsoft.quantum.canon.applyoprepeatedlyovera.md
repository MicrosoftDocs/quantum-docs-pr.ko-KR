---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverA
title: Applyoprepeatedly과잉 a 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverA
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 2e8ef7e943cfd2c0634f16566a018f386aad659f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717844"
---
# <a name="applyoprepeatedlyovera-operation"></a><span data-ttu-id="71367-102">Applyoprepeatedly과잉 a 작업</span><span class="sxs-lookup"><span data-stu-id="71367-102">ApplyOpRepeatedlyOverA operation</span></span>

<span data-ttu-id="71367-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="71367-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="71367-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="71367-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="71367-105">단일 비트 레지스터에 대해 동일한 op를 여러 번 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71367-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOverA (op : (Qubit[] => Unit is Adj), targets : Int[][], register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="71367-106">입력</span><span class="sxs-lookup"><span data-stu-id="71367-106">Input</span></span>

### <a name="op--qubit--unit-adj"></a><span data-ttu-id="71367-107">op: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="71367-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="71367-108">이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="71367-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="71367-109">대상: [Int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="71367-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="71367-110">Op의 대상을 설명 하는 중첩 된 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="71367-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="71367-111">각 배열에는 사용할 비트를 설명 하는 정수 목록이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="71367-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="71367-112">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="71367-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="71367-113">작업할의 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="71367-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="71367-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="71367-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="71367-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="71367-115">See Also</span></span>

- [<span data-ttu-id="71367-116">ApplySeriesOfOps입니다.</span><span class="sxs-lookup"><span data-stu-id="71367-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)