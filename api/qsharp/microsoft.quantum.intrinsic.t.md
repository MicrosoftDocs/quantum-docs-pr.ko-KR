---
uid: Microsoft.Quantum.Intrinsic.T
title: T 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: T
qsharp.summary: Applies the T gate to a single qubit.
ms.openlocfilehash: 352ef2c1b15a46dea85c420fc6f1cfab0382e73a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198404"
---
# <a name="t-operation"></a><span data-ttu-id="f7c9b-102">T 작업</span><span class="sxs-lookup"><span data-stu-id="f7c9b-102">T operation</span></span>

<span data-ttu-id="f7c9b-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="f7c9b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="f7c9b-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="f7c9b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="f7c9b-105">T 게이트를 단일의 비트에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7c9b-105">Applies the T gate to a single qubit.</span></span>

```qsharp
operation T (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="f7c9b-106">Description</span><span class="sxs-lookup"><span data-stu-id="f7c9b-106">Description</span></span>

<span data-ttu-id="f7c9b-107">단일 행렬 \begin{align} T \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ 0 & e ^ {i \pi/4} \end{bmatrix}.이 작업을 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f7c9b-107">This operation can be simulated by the unitary matrix \begin{align} T \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & e^{i \pi / 4} \end{bmatrix}.</span></span>
<span data-ttu-id="f7c9b-108">\end{align}</span><span class="sxs-lookup"><span data-stu-id="f7c9b-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="f7c9b-109">입력</span><span class="sxs-lookup"><span data-stu-id="f7c9b-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="f7c9b-110">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f7c9b-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f7c9b-111">게이트가 적용 되어야 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="f7c9b-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f7c9b-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f7c9b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

