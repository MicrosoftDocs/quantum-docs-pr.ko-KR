---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: ApplyDeltaParity 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: 40157b6a166b09c6fee63d86e203f92069d008f1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225757"
---
# <a name="applydeltaparity-operation"></a><span data-ttu-id="3c066-102">ApplyDeltaParity 작업</span><span class="sxs-lookup"><span data-stu-id="3c066-102">ApplyDeltaParity operation</span></span>

<span data-ttu-id="3c066-103">네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="3c066-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="3c066-104">패키지: [Microsoft](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="3c066-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="3c066-105">이전 PQRS 간 패리티 차이를 계산 합니다. 용어 및 다음 PQRS 부채.</span><span class="sxs-lookup"><span data-stu-id="3c066-105">Computes difference in parity between a previous PQRS... terms and the next PQRS... term.</span></span> <span data-ttu-id="3c066-106">이 차이는 보조 비트에서 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c066-106">This difference is computed on a auxiliary qubit.</span></span>

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3c066-107">입력</span><span class="sxs-lookup"><span data-stu-id="3c066-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="3c066-108">prevFermionicTerm: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="3c066-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="3c066-109">이전 PQRS에 대 한 인덱스 목록 ... 표현을.</span><span class="sxs-lookup"><span data-stu-id="3c066-109">List of indices to previous PQRS... terms.</span></span>


### <a name="nextfermionicterm--int"></a><span data-ttu-id="3c066-110">nextFermionicTerm: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="3c066-110">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="3c066-111">다음 PQRS에 대 한 인덱스 목록 ... 표현을.</span><span class="sxs-lookup"><span data-stu-id="3c066-111">List of indices to next PQRS... terms.</span></span>


### <a name="aux--qubit"></a><span data-ttu-id="3c066-112">aux: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3c066-112">aux : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3c066-113">패리티 계산 결과가 저장 되는 보조 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="3c066-113">Auxiliary qubit onto which parity computation results are stored.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="3c066-114">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3c066-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3c066-115">모든 PQRS에서 처리 되는 고 비트 표현을.</span><span class="sxs-lookup"><span data-stu-id="3c066-115">Qubit acted on by all PQRS... terms.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3c066-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3c066-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3c066-117">설명</span><span class="sxs-lookup"><span data-stu-id="3c066-117">Remarks</span></span>

<span data-ttu-id="3c066-118">여기서는 P < Q < R < S 인덱스를 < 하는 것으로 가정 합니다. prevPQ 및 nextPQ 모두에 대해입니다.</span><span class="sxs-lookup"><span data-stu-id="3c066-118">This assumes that indices of P < Q < R < S < ... for both prevPQ and nextPQ.</span></span>