---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA
title: ApplyToFirstThreeQubitsA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsA
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: c3374ceba9f442f9315d4b5fc54b158327124926
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208774"
---
# <a name="applytofirstthreequbitsa-operation"></a><span data-ttu-id="34cd2-102">ApplyToFirstThreeQubitsA 작업</span><span class="sxs-lookup"><span data-stu-id="34cd2-102">ApplyToFirstThreeQubitsA operation</span></span>

<span data-ttu-id="34cd2-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="34cd2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="34cd2-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="34cd2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="34cd2-105">레지스터의 처음 3 개 비트에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="34cd2-105">Applies an operation to the first three qubits in the register.</span></span>
<span data-ttu-id="34cd2-106">한정자는 `A` 작업이 adjointable를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="34cd2-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstThreeQubitsA (op : ((Qubit, Qubit, Qubit) => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="34cd2-107">입력</span><span class="sxs-lookup"><span data-stu-id="34cd2-107">Input</span></span>

### <a name="op--qubitqubitqubit--unit--is-adj"></a><span data-ttu-id="34cd2-108">op[: (Adj bit,](xref:microsoft.quantum.lang-ref.qubit) [bit](xref:microsoft.quantum.lang-ref.qubit), [bit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is</span><span class="sxs-lookup"><span data-stu-id="34cd2-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="34cd2-109">처음 세 개의에 적용 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="34cd2-109">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="34cd2-110">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="34cd2-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="34cd2-111">연산이 적용 되는 처음 세 개의 비트에 대 한 기본 비트 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="34cd2-111">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="34cd2-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="34cd2-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="34cd2-113">설명</span><span class="sxs-lookup"><span data-stu-id="34cd2-113">Remarks</span></span>

<span data-ttu-id="34cd2-114">다음 코드와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="34cd2-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="34cd2-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="34cd2-115">See Also</span></span>

- [<span data-ttu-id="34cd2-116">ApplyToFirstThreeQubits입니다.</span><span class="sxs-lookup"><span data-stu-id="34cd2-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)