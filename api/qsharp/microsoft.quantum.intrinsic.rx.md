---
uid: Microsoft.Quantum.Intrinsic.Rx
title: Rx 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rx
qsharp.summary: >-
  Applies a rotation about the $x$-axis by a given angle.

  \begin{align} R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -i\sin \frac{\theta}{2}  \\\\ -i\sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 6d11c8fa3c3fb2c07a88fdf2cba0ff2a7f51bf6b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723504"
---
# <a name="rx-operation"></a><span data-ttu-id="364af-102">Rx 작업</span><span class="sxs-lookup"><span data-stu-id="364af-102">Rx operation</span></span>

<span data-ttu-id="364af-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="364af-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="364af-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="364af-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="364af-105">지정 된 각도 만큼 $x $ 축에 대 한 회전을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="364af-105">Applies a rotation about the $x$-axis by a given angle.</span></span>

<span data-ttu-id="364af-106">\begin{align} R_x (\theta) \mathrel{: =} e ^ {-i \om\ sigma_x/2} = \begin{bmatrix} \theta \frac{\theta} {2} &-i\sin \frac{\theta} {2} \\ \\ -i\sin \frac{\theta} {2} & \theta \frac{\theta} {2} \end{bmatrix}.  </span><span class="sxs-lookup"><span data-stu-id="364af-106">\begin{align} R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -i\sin \frac{\theta}{2}  \\\\ -i\sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}.</span></span>
<span data-ttu-id="364af-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="364af-107">\end{align}</span></span>

```qsharp
operation Rx (theta : Double, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="364af-108">입력</span><span class="sxs-lookup"><span data-stu-id="364af-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="364af-109">테타: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="364af-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="364af-110">해당 하는 비트를 회전할 각도입니다.</span><span class="sxs-lookup"><span data-stu-id="364af-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="364af-111">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="364af-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="364af-112">게이트가 적용 되어야 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="364af-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="364af-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="364af-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="364af-114">설명</span><span class="sxs-lookup"><span data-stu-id="364af-114">Remarks</span></span>

<span data-ttu-id="364af-115">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="364af-115">Equivalent to:</span></span>

```qsharp
R(PauliX, theta, qubit);
```