---
uid: Microsoft.Quantum.Intrinsic.Z
title: Z 연산
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Z
qsharp.summary: >-
  Applies the Pauli $Z$ gate.

  \begin{align} \sigma_z \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix}. \end{align}
ms.openlocfilehash: 5bfb435a1e7a7b90da807e7c6edb8358fb006e34
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198438"
---
# <a name="z-operation"></a><span data-ttu-id="9ab5d-102">Z 연산</span><span class="sxs-lookup"><span data-stu-id="9ab5d-102">Z operation</span></span>

<span data-ttu-id="9ab5d-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="9ab5d-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="9ab5d-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9ab5d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9ab5d-105">Pauli $Z $ gate에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-105">Applies the Pauli $Z$ gate.</span></span>

<span data-ttu-id="9ab5d-106">\begin{align} \ sigma_z \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ 0 &-1 \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-106">\begin{align} \sigma_z \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix}.</span></span>
<span data-ttu-id="9ab5d-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="9ab5d-107">\end{align}</span></span>

```qsharp
operation Z (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9ab5d-108">입력</span><span class="sxs-lookup"><span data-stu-id="9ab5d-108">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="9ab5d-109">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9ab5d-109">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9ab5d-110">게이트가 적용 되어야 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-110">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9ab5d-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9ab5d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

