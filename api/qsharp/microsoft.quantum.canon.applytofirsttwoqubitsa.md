---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA
title: ApplyToFirstTwoQubitsA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsA
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 911e9bc3d02bf6c0395c30fa167a6cb730dc666e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717305"
---
# <a name="applytofirsttwoqubitsa-operation"></a><span data-ttu-id="c4056-102">ApplyToFirstTwoQubitsA 작업</span><span class="sxs-lookup"><span data-stu-id="c4056-102">ApplyToFirstTwoQubitsA operation</span></span>

<span data-ttu-id="c4056-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c4056-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c4056-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c4056-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c4056-105">레지스터의 처음 두 비트에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4056-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="c4056-106">한정자는 `A` 작업이 adjointable를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c4056-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsA (op : ((Qubit, Qubit) => Unit is Adj), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c4056-107">입력</span><span class="sxs-lookup"><span data-stu-id="c4056-107">Input</span></span>

### <a name="op--qubitqubit--unit-adj"></a><span data-ttu-id="c4056-108">op: (Adj[비트](xref:microsoft.quantum.lang-ref.qubit))[=](xref:microsoft.quantum.lang-ref.qubit)> [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c4056-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="c4056-109">처음 두 개의 작업에 적용 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c4056-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="c4056-110">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c4056-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c4056-111">연산이 적용 되는 처음 두 개의 비트에 대 한 기본 비트 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="c4056-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c4056-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c4056-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c4056-113">설명</span><span class="sxs-lookup"><span data-stu-id="c4056-113">Remarks</span></span>

<span data-ttu-id="c4056-114">다음 코드와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="c4056-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="c4056-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c4056-115">See Also</span></span>

- [<span data-ttu-id="c4056-116">ApplyToFirstTwoQubits입니다.</span><span class="sxs-lookup"><span data-stu-id="c4056-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)