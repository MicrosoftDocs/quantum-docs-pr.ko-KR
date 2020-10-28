---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: CCNOT 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: bf20ff1e9d25d72e7e8e0207ab947a57dc394cf4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711537"
---
# <a name="ccnot-operation"></a><span data-ttu-id="07406-102">CCNOT 작업</span><span class="sxs-lookup"><span data-stu-id="07406-102">CCNOT operation</span></span>

<span data-ttu-id="07406-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="07406-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="07406-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="07406-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="07406-105">3 가지 비트에 이중 제어 – (CCNOT) 게이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07406-105">Applies the doubly controlled–NOT (CCNOT) gate to three qubits.</span></span>

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="07406-106">입력</span><span class="sxs-lookup"><span data-stu-id="07406-106">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="07406-107">control1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="07406-107">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="07406-108">먼저 CCNOT gate의 비트를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="07406-108">First control qubit for the CCNOT gate.</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="07406-109">control2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="07406-109">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="07406-110">CCNOT gate의 두 번째 제어 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="07406-110">Second control qubit for the CCNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="07406-111">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="07406-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="07406-112">CCNOT gate의 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="07406-112">Target qubit for the CCNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="07406-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="07406-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="07406-114">설명</span><span class="sxs-lookup"><span data-stu-id="07406-114">Remarks</span></span>

<span data-ttu-id="07406-115">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="07406-115">Equivalent to:</span></span>

```qsharp
Controlled X([control1, control2], target);
```