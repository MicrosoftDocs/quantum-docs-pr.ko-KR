---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitCA
title: Applytofirst Bitca 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitCA
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: bc2b1275b4258b9cc2db45c9e5cfe14f7eee0c67
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208808"
---
# <a name="applytofirstqubitca-operation"></a><span data-ttu-id="0cec5-102">Applytofirst Bitca 작업</span><span class="sxs-lookup"><span data-stu-id="0cec5-102">ApplyToFirstQubitCA operation</span></span>

<span data-ttu-id="0cec5-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0cec5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0cec5-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0cec5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0cec5-105">레지스터의 첫 번째 비트에 작업 op를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cec5-105">Applies operation op to the first qubit in the register.</span></span>
<span data-ttu-id="0cec5-106">한정자는 `CA` 작업을 제어 하 고 adjointable 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0cec5-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstQubitCA (op : (Qubit => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="0cec5-107">입력</span><span class="sxs-lookup"><span data-stu-id="0cec5-107">Input</span></span>

### <a name="op--qubit--unit--is-adj--ctl"></a><span data-ttu-id="0cec5-108">op: 고 [비트](xref:microsoft.quantum.lang-ref.qubit) => [단위](xref:microsoft.quantum.lang-ref.unit)  는 Adj + Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="0cec5-108">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="0cec5-109">첫 번째 비트에 적용 되는 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="0cec5-109">An operation to be applied to the first qubit</span></span>


### <a name="register--qubit"></a><span data-ttu-id="0cec5-110">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0cec5-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="0cec5-111">연산이 적용 되는 첫 번째 작업에 대 한 기본 비트 배열</span><span class="sxs-lookup"><span data-stu-id="0cec5-111">Qubit array to the first qubit of which the operation is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="0cec5-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0cec5-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="0cec5-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0cec5-113">See Also</span></span>

- [<span data-ttu-id="0cec5-114">Microsoft. 양자. Applytofirstbit</span><span class="sxs-lookup"><span data-stu-id="0cec5-114">Microsoft.Quantum.Canon.ApplyToFirstQubit</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)