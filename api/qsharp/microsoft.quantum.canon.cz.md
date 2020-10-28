---
uid: Microsoft.Quantum.Canon.CZ
title: CZ 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CZ
qsharp.summary: >-
  Applies the controlled-Z (CZ) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 0 & 0 & -1 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: bc38cd43a0dcaf7aea735ef6468a394e91c85593
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716346"
---
# <a name="cz-operation"></a><span data-ttu-id="829bd-102">CZ 작업</span><span class="sxs-lookup"><span data-stu-id="829bd-102">CZ operation</span></span>

<span data-ttu-id="829bd-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="829bd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="829bd-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="829bd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="829bd-105">CZ (제어-Z) 게이트를 다양 한 쌍에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="829bd-105">Applies the controlled-Z (CZ) gate to a pair of qubits.</span></span>

<span data-ttu-id="829bd-106">$ $ \begin{align} 1 & 0 & 0 & 0 0 & 1 & 0 & 0 0 & 0 & 1 & 0 0 & 0 & 0 & \\ \\ \\ \\ \\ \\ -1 \end{align}, $ $ 여기서 행과 열은 퀀텀 개념 가이드에서와 같이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="829bd-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 0 & 0 & -1 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CZ (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="829bd-107">입력</span><span class="sxs-lookup"><span data-stu-id="829bd-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="829bd-108">제어: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="829bd-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="829bd-109">CZ 게이트의 비트를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="829bd-109">Control qubit for the CZ gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="829bd-110">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="829bd-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="829bd-111">CZ 게이트의 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="829bd-111">Target qubit for the CZ gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="829bd-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="829bd-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="829bd-113">설명</span><span class="sxs-lookup"><span data-stu-id="829bd-113">Remarks</span></span>

<span data-ttu-id="829bd-114">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="829bd-114">Equivalent to:</span></span>

```qsharp
Controlled Z([control], target);
```