---
uid: Microsoft.Quantum.Intrinsic.Rz
title: Rz 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rz
qsharp.summary: >-
  Applies a rotation about the $z$-axis by a given angle.

  \begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 4282fcc216173234ec742991b8f0fa1be203da0d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849285"
---
# <a name="rz-operation"></a><span data-ttu-id="47235-102">Rz 작업</span><span class="sxs-lookup"><span data-stu-id="47235-102">Rz operation</span></span>

<span data-ttu-id="47235-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="47235-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="47235-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="47235-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="47235-105">지정 된 각도 만큼 $z $ 축에 대 한 회전을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="47235-105">Applies a rotation about the $z$-axis by a given angle.</span></span>

<span data-ttu-id="47235-106">\begin{align} R_z (\theta) \mathrel{: =} e ^ {-i \theta \ sigma_z/2} = \begin{bmatrix} e ^ {-i \theta/2} & 0 \\ \\ 0 & e ^ {i \theta/2} \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="47235-106">\begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}.</span></span>
<span data-ttu-id="47235-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="47235-107">\end{align}</span></span>

```qsharp
operation Rz (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="47235-108">입력</span><span class="sxs-lookup"><span data-stu-id="47235-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="47235-109">테타: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="47235-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="47235-110">해당 하는 비트를 회전할 각도입니다.</span><span class="sxs-lookup"><span data-stu-id="47235-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="47235-111">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="47235-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="47235-112">게이트가 적용 되어야 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="47235-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="47235-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="47235-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="47235-114">설명</span><span class="sxs-lookup"><span data-stu-id="47235-114">Remarks</span></span>

<span data-ttu-id="47235-115">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="47235-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
```