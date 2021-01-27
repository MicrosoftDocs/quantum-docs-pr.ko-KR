---
uid: Microsoft.Quantum.Intrinsic.Ry
title: R) 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Ry
qsharp.summary: >-
  Applies a rotation about the $y$-axis by a given angle.

  \begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}. \end{align}
ms.openlocfilehash: b50225b67701c6b17475445d5ed54400240e0b69
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818276"
---
# <a name="ry-operation"></a><span data-ttu-id="a5f40-102">R) 작업</span><span class="sxs-lookup"><span data-stu-id="a5f40-102">Ry operation</span></span>

<span data-ttu-id="a5f40-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="a5f40-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="a5f40-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a5f40-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a5f40-105">지정 된 각도 만큼 $y $ 축에 대 한 회전을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5f40-105">Applies a rotation about the $y$-axis by a given angle.</span></span>

<span data-ttu-id="a5f40-106">\begin{align} R_y (\theta) \mathrel{: =} e ^ {-i \om\ sigma_y/2} = \begin{bmatrix} \theta \frac{\theta} {2} &-\theta \frac{\theta} {2} \\ \\ \theta \frac{\theta} {2} & \theta \frac{\theta} {2} \end{bmatrix}.  </span><span class="sxs-lookup"><span data-stu-id="a5f40-106">\begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}.</span></span>
<span data-ttu-id="a5f40-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="a5f40-107">\end{align}</span></span>

```qsharp
operation Ry (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a5f40-108">입력</span><span class="sxs-lookup"><span data-stu-id="a5f40-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="a5f40-109">테타: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a5f40-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a5f40-110">해당 하는 비트를 회전할 각도입니다.</span><span class="sxs-lookup"><span data-stu-id="a5f40-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="a5f40-111">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a5f40-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a5f40-112">게이트가 적용 되어야 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="a5f40-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a5f40-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a5f40-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a5f40-114">설명</span><span class="sxs-lookup"><span data-stu-id="a5f40-114">Remarks</span></span>

<span data-ttu-id="a5f40-115">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5f40-115">Equivalent to:</span></span>

```qsharp
R(PauliY, theta, qubit);
```