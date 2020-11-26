---
uid: Microsoft.Quantum.Intrinsic.S
title: S 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: S
qsharp.summary: Applies the S gate to a single qubit.
ms.openlocfilehash: c697408c4efe1963787b5aee8f0d3bb6b9e64dd5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198455"
---
# <a name="s-operation"></a><span data-ttu-id="43132-102">S 작업</span><span class="sxs-lookup"><span data-stu-id="43132-102">S operation</span></span>

<span data-ttu-id="43132-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="43132-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="43132-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="43132-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="43132-105">단일의 단일 비트에 게이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="43132-105">Applies the S gate to a single qubit.</span></span>

```qsharp
operation S (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="43132-106">Description</span><span class="sxs-lookup"><span data-stu-id="43132-106">Description</span></span>

<span data-ttu-id="43132-107">단일 행렬 \begin{align} S \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ 0 & i \end{bmatrix}.에서이 작업을 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43132-107">This operation can be simulated by the unitary matrix \begin{align} S \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & i \end{bmatrix}.</span></span>
<span data-ttu-id="43132-108">\end{align}</span><span class="sxs-lookup"><span data-stu-id="43132-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="43132-109">입력</span><span class="sxs-lookup"><span data-stu-id="43132-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="43132-110">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="43132-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="43132-111">게이트가 적용 되어야 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="43132-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="43132-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="43132-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

