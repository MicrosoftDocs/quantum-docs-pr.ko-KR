---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubit
title: Applytofirst의 비트 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubit
qsharp.summary: Applies an operation to the first qubit in the register.
ms.openlocfilehash: 99439229e2c3d5a10073669cf1e742f6de3d7618
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717424"
---
# <a name="applytofirstqubit-operation"></a><span data-ttu-id="27b45-102">Applytofirst의 비트 작업</span><span class="sxs-lookup"><span data-stu-id="27b45-102">ApplyToFirstQubit operation</span></span>

<span data-ttu-id="27b45-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="27b45-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="27b45-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="27b45-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="27b45-105">레지스터의 첫 번째 비트에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b45-105">Applies an operation to the first qubit in the register.</span></span>

```qsharp
operation ApplyToFirstQubit (op : (Qubit => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="27b45-106">입력</span><span class="sxs-lookup"><span data-stu-id="27b45-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="27b45-107">op:의 [비트](xref:microsoft.quantum.lang-ref.qubit) => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="27b45-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="27b45-108">첫 번째 비트에 적용 되는 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="27b45-108">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="27b45-109">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="27b45-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="27b45-110">연산이 적용 되는 첫 번째 작업에 대 한 기본 비트 배열</span><span class="sxs-lookup"><span data-stu-id="27b45-110">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="27b45-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="27b45-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="27b45-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="27b45-112">See Also</span></span>

- [<span data-ttu-id="27b45-113">Microsoft. 양자. ApplyToFirstQubitA</span><span class="sxs-lookup"><span data-stu-id="27b45-113">Microsoft.Quantum.Canon.ApplyToFirstQubitA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubitA)
- [<span data-ttu-id="27b45-114">Microsoft. 양자. ApplyToFirstQubitC</span><span class="sxs-lookup"><span data-stu-id="27b45-114">Microsoft.Quantum.Canon.ApplyToFirstQubitC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubitC)
- [<span data-ttu-id="27b45-115">Microsoft. 양자. ApplyToFirstQubitCA</span><span class="sxs-lookup"><span data-stu-id="27b45-115">Microsoft.Quantum.Canon.ApplyToFirstQubitCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubitCA)