---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubits
title: ApplyToFirstThreeQubits 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubits
qsharp.summary: Applies an operation to the first three qubits in the register.
ms.openlocfilehash: 61330f9e9b1f6b9f3965c9240505814b295aaefe
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717382"
---
# <a name="applytofirstthreequbits-operation"></a><span data-ttu-id="4f568-102">ApplyToFirstThreeQubits 작업</span><span class="sxs-lookup"><span data-stu-id="4f568-102">ApplyToFirstThreeQubits operation</span></span>

<span data-ttu-id="4f568-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4f568-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4f568-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4f568-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4f568-105">레지스터의 처음 3 개 비트에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f568-105">Applies an operation to the first three qubits in the register.</span></span>

```qsharp
operation ApplyToFirstThreeQubits (op : ((Qubit, Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="4f568-106">입력</span><span class="sxs-lookup"><span data-stu-id="4f568-106">Input</span></span>

### <a name="op--qubitqubitqubit--unit"></a><span data-ttu-id="4f568-107">op[: (이상 비트, 고](xref:microsoft.quantum.lang-ref.qubit)[비트, 고](xref:microsoft.quantum.lang-ref.qubit)[비트](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4f568-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="4f568-108">처음 세 개의에 적용 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="4f568-108">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="4f568-109">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="4f568-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="4f568-110">연산이 적용 되는 처음 세 개의 비트에 대 한 기본 비트 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="4f568-110">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4f568-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4f568-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="4f568-112">설명</span><span class="sxs-lookup"><span data-stu-id="4f568-112">Remarks</span></span>

<span data-ttu-id="4f568-113">다음 코드와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="4f568-113">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="4f568-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4f568-114">See Also</span></span>

- [<span data-ttu-id="4f568-115">ApplyToFirstThreeQubitsC입니다.</span><span class="sxs-lookup"><span data-stu-id="4f568-115">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsC)
- [<span data-ttu-id="4f568-116">ApplyToFirstThreeQubitsA입니다.</span><span class="sxs-lookup"><span data-stu-id="4f568-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA)
- [<span data-ttu-id="4f568-117">ApplyToFirstThreeQubitsCA입니다.</span><span class="sxs-lookup"><span data-stu-id="4f568-117">Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA)