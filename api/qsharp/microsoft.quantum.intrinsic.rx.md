---
uid: Microsoft.Quantum.Intrinsic.Rx
title: Rx 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rx
qsharp.summary: >-
  Applies a rotation about the $x$-axis by a given angle.

  \begin{align} R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -i\sin \frac{\theta}{2}  \\\\ -i\sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 49638c00967ff2f47dad41acfed05868d65a24a0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198591"
---
# <a name="rx-operation"></a><span data-ttu-id="c7ab9-102">Rx 작업</span><span class="sxs-lookup"><span data-stu-id="c7ab9-102">Rx operation</span></span>

<span data-ttu-id="c7ab9-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="c7ab9-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="c7ab9-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c7ab9-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c7ab9-105">지정 된 각도 만큼 $x $ 축에 대 한 회전을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ab9-105">Applies a rotation about the $x$-axis by a given angle.</span></span>

<span data-ttu-id="c7ab9-106">\begin{align} R_x (\theta) \mathrel{: =} e ^ {-i \om\ sigma_x/2} = \begin{bmatrix} \theta \frac{\theta} {2} &-i\sin \frac{\theta} {2} \\ \\ -i\sin \frac{\theta} {2} & \theta \frac{\theta} {2} \end{bmatrix}.  </span><span class="sxs-lookup"><span data-stu-id="c7ab9-106">\begin{align} R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -i\sin \frac{\theta}{2}  \\\\ -i\sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}.</span></span>
<span data-ttu-id="c7ab9-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="c7ab9-107">\end{align}</span></span>

```qsharp
operation Rx (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c7ab9-108">입력</span><span class="sxs-lookup"><span data-stu-id="c7ab9-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="c7ab9-109">테타: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c7ab9-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c7ab9-110">해당 하는 비트를 회전할 각도입니다.</span><span class="sxs-lookup"><span data-stu-id="c7ab9-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="c7ab9-111">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c7ab9-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c7ab9-112">게이트가 적용 되어야 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="c7ab9-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c7ab9-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c7ab9-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c7ab9-114">설명</span><span class="sxs-lookup"><span data-stu-id="c7ab9-114">Remarks</span></span>

<span data-ttu-id="c7ab9-115">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ab9-115">Equivalent to:</span></span>

```qsharp
R(PauliX, theta, qubit);
```