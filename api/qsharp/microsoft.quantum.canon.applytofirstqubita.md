---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitA
title: Applytofirst Bita 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitA
qsharp.summary: Applies an operation to the first qubit in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 00dbff0b562f90653c8569589e838f11e6c938e8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717403"
---
# <a name="applytofirstqubita-operation"></a><span data-ttu-id="bc28c-102">Applytofirst Bita 작업</span><span class="sxs-lookup"><span data-stu-id="bc28c-102">ApplyToFirstQubitA operation</span></span>

<span data-ttu-id="bc28c-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bc28c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bc28c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bc28c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bc28c-105">레지스터의 첫 번째 비트에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc28c-105">Applies an operation to the first qubit in the register.</span></span>
<span data-ttu-id="bc28c-106">한정자는 `A` 작업이 adjointable를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bc28c-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitA (op : (Qubit => Unit is Adj), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="bc28c-107">입력</span><span class="sxs-lookup"><span data-stu-id="bc28c-107">Input</span></span>

### <a name="op--qubit--unit-adj"></a><span data-ttu-id="bc28c-108">op: Adj [비트](xref:microsoft.quantum.lang-ref.qubit) => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bc28c-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="bc28c-109">첫 번째 비트에 적용 되는 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="bc28c-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="bc28c-110">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="bc28c-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bc28c-111">연산이 적용 되는 첫 번째 작업에 대 한 기본 비트 배열</span><span class="sxs-lookup"><span data-stu-id="bc28c-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="bc28c-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bc28c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="bc28c-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="bc28c-113">See Also</span></span>

- [<span data-ttu-id="bc28c-114">Microsoft. 양자. Applytofirstbit</span><span class="sxs-lookup"><span data-stu-id="bc28c-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)