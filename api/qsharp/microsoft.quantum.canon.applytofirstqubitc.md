---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitC
title: Applytofirst Bitc 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitC
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: e2c137ad4a8252731acf94d6f2343f8fd386b8e3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717410"
---
# <a name="applytofirstqubitc-operation"></a><span data-ttu-id="f496b-102">Applytofirst Bitc 작업</span><span class="sxs-lookup"><span data-stu-id="f496b-102">ApplyToFirstQubitC operation</span></span>

<span data-ttu-id="f496b-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f496b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f496b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f496b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f496b-105">레지스터의 첫 번째 비트에 작업 op를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f496b-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="f496b-106">한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f496b-106">The modifier `C` indicates that the operation is controllable.</span></span>

```qsharp
operation ApplyToFirstQubitC (op : (Qubit => Unit is Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="f496b-107">입력</span><span class="sxs-lookup"><span data-stu-id="f496b-107">Input</span></span>

### <a name="op--qubit--unit-ctl"></a><span data-ttu-id="f496b-108">op: 이상 [비트](xref:microsoft.quantum.lang-ref.qubit) => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="f496b-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="f496b-109">첫 번째 비트에 적용 되는 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="f496b-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="f496b-110">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f496b-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f496b-111">연산이 적용 되는 첫 번째 작업에 대 한 기본 비트 배열</span><span class="sxs-lookup"><span data-stu-id="f496b-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="f496b-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f496b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="f496b-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f496b-113">See Also</span></span>

- [<span data-ttu-id="f496b-114">Microsoft. 양자. Applytofirstbit</span><span class="sxs-lookup"><span data-stu-id="f496b-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)