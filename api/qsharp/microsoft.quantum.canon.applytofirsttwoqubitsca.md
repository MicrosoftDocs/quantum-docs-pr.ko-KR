---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA
title: ApplyToFirstTwoQubitsCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsCA
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 0c5e29fbca8449f8122f2a9f988797e94e27da60
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717263"
---
# <a name="applytofirsttwoqubitsca-operation"></a><span data-ttu-id="caae0-102">ApplyToFirstTwoQubitsCA 작업</span><span class="sxs-lookup"><span data-stu-id="caae0-102">ApplyToFirstTwoQubitsCA operation</span></span>

<span data-ttu-id="caae0-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="caae0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="caae0-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="caae0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="caae0-105">레지스터의 처음 두 비트에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="caae0-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="caae0-106">한정자는 `CA` 작업을 제어 하 고 adjointable 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="caae0-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsCA (op : ((Qubit, Qubit) => Unit is Adj + Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="caae0-107">입력</span><span class="sxs-lookup"><span data-stu-id="caae0-107">Input</span></span>

### <a name="op--qubitqubit--unit-adj--ctl"></a><span data-ttu-id="caae0-108">op: (Adj[비트](xref:microsoft.quantum.lang-ref.qubit))[=](xref:microsoft.quantum.lang-ref.qubit)> [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="caae0-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="caae0-109">처음 두 개의 작업에 적용 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="caae0-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="caae0-110">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="caae0-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="caae0-111">연산이 적용 되는 처음 두 개의 비트에 대 한 기본 비트 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="caae0-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="caae0-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="caae0-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="caae0-113">설명</span><span class="sxs-lookup"><span data-stu-id="caae0-113">Remarks</span></span>

<span data-ttu-id="caae0-114">다음 코드와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="caae0-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="caae0-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="caae0-115">See Also</span></span>

- [<span data-ttu-id="caae0-116">ApplyToFirstTwoQubits입니다.</span><span class="sxs-lookup"><span data-stu-id="caae0-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)