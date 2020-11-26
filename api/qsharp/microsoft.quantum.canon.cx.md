---
uid: Microsoft.Quantum.Canon.CX
title: CX 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CX
qsharp.summary: >-
  Applies the controlled-X (CX) gate to a pair of qubits.

  $$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: 4eaecf372f3054de4886b1e42c6b4ce386a22f73
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207244"
---
# <a name="cx-operation"></a><span data-ttu-id="63ed5-102">CX 작업</span><span class="sxs-lookup"><span data-stu-id="63ed5-102">CX operation</span></span>

<span data-ttu-id="63ed5-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="63ed5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="63ed5-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="63ed5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="63ed5-105">제어 된 X (CX) 게이트를 한 쌍의 비트에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="63ed5-105">Applies the controlled-X (CX) gate to a pair of qubits.</span></span>

<span data-ttu-id="63ed5-106">$ $ \begin{align} \left (\begin{matrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 0 & 0 & 0 & 1 0 & 0 & 1 \\ \\ \\ \\ & 0 \end{matrix}\right) \end{align}, $ $ 여기서 행과 열은 퀀텀 개념 가이드에서와 같이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63ed5-106">$$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CX (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="63ed5-107">입력</span><span class="sxs-lookup"><span data-stu-id="63ed5-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="63ed5-108">제어: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="63ed5-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="63ed5-109">CX gate의 비트를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="63ed5-109">Control qubit for the CX gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="63ed5-110">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="63ed5-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="63ed5-111">CX gate의 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="63ed5-111">Target qubit for the CX gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="63ed5-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="63ed5-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="63ed5-113">설명</span><span class="sxs-lookup"><span data-stu-id="63ed5-113">Remarks</span></span>

<span data-ttu-id="63ed5-114">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="63ed5-114">Equivalent to:</span></span>

```qsharp
Controlled X([control], target);
```

<span data-ttu-id="63ed5-115">그리고 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="63ed5-115">and to:</span></span>

```qsharp
CNOT(control, target);
```