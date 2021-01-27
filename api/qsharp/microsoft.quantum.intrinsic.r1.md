---
uid: Microsoft.Quantum.Intrinsic.R1
title: R1 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by a given angle.

  \begin{align} R_1(\theta) \mathrel{:=} \operatorname{diag}(1, e^{i\theta}). \end{align}
ms.openlocfilehash: 07cce580b50fef5664fdac32bb4fae0ba22d25e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849359"
---
# <a name="r1-operation"></a><span data-ttu-id="3cfb6-102">R1 작업</span><span class="sxs-lookup"><span data-stu-id="3cfb6-102">R1 operation</span></span>

<span data-ttu-id="3cfb6-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="3cfb6-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="3cfb6-105">지정 된 각도로 $ \ket $ 상태에 대 한 회전을 적용 {1} 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-105">Applies a rotation about the $\ket{1}$ state by a given angle.</span></span>

<span data-ttu-id="3cfb6-106">\begin{align} R_1 (\theta) \mathrel{: =} \operatorname{diag} (1, e ^ {i\theta}).</span><span class="sxs-lookup"><span data-stu-id="3cfb6-106">\begin{align} R_1(\theta) \mathrel{:=} \operatorname{diag}(1, e^{i\theta}).</span></span>
<span data-ttu-id="3cfb6-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="3cfb6-107">\end{align}</span></span>

```qsharp
operation R1 (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3cfb6-108">입력</span><span class="sxs-lookup"><span data-stu-id="3cfb6-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="3cfb6-109">테타: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="3cfb6-110">해당 하는 비트를 회전할 각도입니다.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="3cfb6-111">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3cfb6-112">게이트가 적용 되어야 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3cfb6-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3cfb6-114">설명</span><span class="sxs-lookup"><span data-stu-id="3cfb6-114">Remarks</span></span>

<span data-ttu-id="3cfb6-115">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
R(PauliI, -theta, qubit);
```