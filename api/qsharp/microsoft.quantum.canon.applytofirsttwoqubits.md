---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubits
title: ApplyToFirstTwoQubits 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubits
qsharp.summary: Applies an operation to the first two qubits in the register.
ms.openlocfilehash: aad07889c0dbf2329304c98b06dbd0c225df8a81
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717312"
---
# <a name="applytofirsttwoqubits-operation"></a><span data-ttu-id="7d698-102">ApplyToFirstTwoQubits 작업</span><span class="sxs-lookup"><span data-stu-id="7d698-102">ApplyToFirstTwoQubits operation</span></span>

<span data-ttu-id="7d698-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7d698-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7d698-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7d698-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7d698-105">레지스터의 처음 두 비트에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d698-105">Applies an operation to the first two qubits in the register.</span></span>

```qsharp
operation ApplyToFirstTwoQubits (op : ((Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="7d698-106">입력</span><span class="sxs-lookup"><span data-stu-id="7d698-106">Input</span></span>

### <a name="op--qubitqubit--unit"></a><span data-ttu-id="7d698-107">op: ([(고](xref:microsoft.quantum.lang-ref.qubit)[비트](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7d698-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="7d698-108">처음 두 개의 작업에 적용 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="7d698-108">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="7d698-109">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7d698-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7d698-110">연산이 적용 되는 처음 두 개의 비트에 대 한 기본 비트 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="7d698-110">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7d698-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7d698-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7d698-112">설명</span><span class="sxs-lookup"><span data-stu-id="7d698-112">Remarks</span></span>

<span data-ttu-id="7d698-113">다음 코드와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="7d698-113">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="7d698-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="7d698-114">See Also</span></span>

- [<span data-ttu-id="7d698-115">ApplyToFirstTwoQubitsA입니다.</span><span class="sxs-lookup"><span data-stu-id="7d698-115">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA)
- [<span data-ttu-id="7d698-116">ApplyToFirstTwoQubitsC입니다.</span><span class="sxs-lookup"><span data-stu-id="7d698-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC)
- [<span data-ttu-id="7d698-117">ApplyToFirstTwoQubitsCA입니다.</span><span class="sxs-lookup"><span data-stu-id="7d698-117">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA)