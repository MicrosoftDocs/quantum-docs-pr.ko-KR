---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC
title: ApplyToFirstTwoQubitsC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsC
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 97706ffcc8700a0055ff37bbbaccc6fb4f8854b6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717284"
---
# <a name="applytofirsttwoqubitsc-operation"></a><span data-ttu-id="cd477-102">ApplyToFirstTwoQubitsC 작업</span><span class="sxs-lookup"><span data-stu-id="cd477-102">ApplyToFirstTwoQubitsC operation</span></span>

<span data-ttu-id="cd477-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cd477-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cd477-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cd477-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cd477-105">레지스터의 처음 두 비트에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd477-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="cd477-106">한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cd477-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsC (op : ((Qubit, Qubit) => Unit is Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="cd477-107">입력</span><span class="sxs-lookup"><span data-stu-id="cd477-107">Input</span></span>

### <a name="op--qubitqubit--unit-ctl"></a><span data-ttu-id="cd477-108">op: ([(고](xref:microsoft.quantum.lang-ref.qubit)[비트](xref:microsoft.quantum.lang-ref.qubit)) => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="cd477-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="cd477-109">처음 두 개의 작업에 적용 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="cd477-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="cd477-110">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="cd477-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="cd477-111">연산이 적용 되는 처음 두 개의 비트에 대 한 기본 비트 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="cd477-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cd477-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cd477-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="cd477-113">설명</span><span class="sxs-lookup"><span data-stu-id="cd477-113">Remarks</span></span>

<span data-ttu-id="cd477-114">다음 코드와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="cd477-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="cd477-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cd477-115">See Also</span></span>

- [<span data-ttu-id="cd477-116">ApplyToFirstTwoQubits입니다.</span><span class="sxs-lookup"><span data-stu-id="cd477-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)