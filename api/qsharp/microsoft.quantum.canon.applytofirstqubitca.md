---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitCA
title: Applytofirst Bitca 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitCA
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 2e1db23ad819a85df99a826f406d9b0fbcc7a175
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717396"
---
# <a name="applytofirstqubitca-operation"></a><span data-ttu-id="35585-102">Applytofirst Bitca 작업</span><span class="sxs-lookup"><span data-stu-id="35585-102">ApplyToFirstQubitCA operation</span></span>

<span data-ttu-id="35585-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="35585-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="35585-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="35585-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="35585-105">레지스터의 첫 번째 비트에 작업 op를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="35585-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="35585-106">한정자는 `CA` 작업을 제어 하 고 adjointable 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="35585-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitCA (op : (Qubit => Unit is Adj + Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="35585-107">입력</span><span class="sxs-lookup"><span data-stu-id="35585-107">Input</span></span>

### <a name="op--qubit--unit-adj--ctl"></a><span data-ttu-id="35585-108">op: 이상 [비트](xref:microsoft.quantum.lang-ref.qubit) => [단위](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="35585-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="35585-109">첫 번째 비트에 적용 되는 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="35585-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="35585-110">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="35585-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="35585-111">연산이 적용 되는 첫 번째 작업에 대 한 기본 비트 배열</span><span class="sxs-lookup"><span data-stu-id="35585-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="35585-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="35585-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="35585-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="35585-113">See Also</span></span>

- [<span data-ttu-id="35585-114">Microsoft. 양자. Applytofirstbit</span><span class="sxs-lookup"><span data-stu-id="35585-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)