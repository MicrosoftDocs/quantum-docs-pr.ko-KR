---
uid: Microsoft.Quantum.Canon.CY
title: CY 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CY
qsharp.summary: >-
  Applies the controlled-Y (CY) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 291891457ff39cf7092d17aa1d900dd0d35d9cf8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716360"
---
# <a name="cy-operation"></a><span data-ttu-id="ba3ab-102">CY 작업</span><span class="sxs-lookup"><span data-stu-id="ba3ab-102">CY operation</span></span>

<span data-ttu-id="ba3ab-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ba3ab-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ba3ab-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ba3ab-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ba3ab-105">제어 된-Y (CY) 게이트를 한 쌍의 비트에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba3ab-105">Applies the controlled-Y (CY) gate to a pair of qubits.</span></span>

<span data-ttu-id="ba3ab-106">$ $ \begin{align} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 0 & 0 & 0 & \\ \\ -i 0 & 0 \\ \\ & i & 0 \end{align}, $ $ 여기서 행과 열은 퀀텀 개념 가이드에서와 같이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba3ab-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -i \\\\ 0 & 0 & i & 0 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CY (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="ba3ab-107">입력</span><span class="sxs-lookup"><span data-stu-id="ba3ab-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="ba3ab-108">제어: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ba3ab-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ba3ab-109">CY 게이트의 비트를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba3ab-109">Control qubit for the CY gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="ba3ab-110">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ba3ab-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ba3ab-111">CY 게이트의 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="ba3ab-111">Target qubit for the CY gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ba3ab-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ba3ab-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ba3ab-113">설명</span><span class="sxs-lookup"><span data-stu-id="ba3ab-113">Remarks</span></span>

<span data-ttu-id="ba3ab-114">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba3ab-114">Equivalent to:</span></span>

```qsharp
Controlled Y([control], target);
```