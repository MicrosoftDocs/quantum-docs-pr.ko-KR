---
uid: Microsoft.Quantum.Intrinsic.M
title: M 연산
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: M
qsharp.summary: >-
  Performs a measurement of a single qubit in the Pauli $Z$ basis.

  The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}. \end{align}
ms.openlocfilehash: 8d4b120385bfc7086a7cb0e3f77034c760d78d92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720937"
---
# <a name="m-operation"></a><span data-ttu-id="41214-102">M 연산</span><span class="sxs-lookup"><span data-stu-id="41214-102">M operation</span></span>

<span data-ttu-id="41214-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="41214-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="41214-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="41214-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="41214-105">Pauli $Z $ 기준에서 단일 고 비트를 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41214-105">Performs a measurement of a single qubit in the Pauli $Z$ basis.</span></span>

<span data-ttu-id="41214-106">출력 결과는 배포 \begin{align} \Pr (\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.에 의해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="41214-106">The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span></span>
<span data-ttu-id="41214-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="41214-107">\end{align}</span></span>

```qsharp
operation M (qubit : Qubit) : Result
```


## <a name="input"></a><span data-ttu-id="41214-108">입력</span><span class="sxs-lookup"><span data-stu-id="41214-108">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="41214-109">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="41214-109">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="41214-110">측정할 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="41214-110">Qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="41214-111">출력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="41214-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="41214-112">`Zero` $ + $1 eigenvalue가 관찰 되 면이 고, `One` $-$1 eigenvalue가 관찰 되 면입니다.</span><span class="sxs-lookup"><span data-stu-id="41214-112">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="41214-113">설명</span><span class="sxs-lookup"><span data-stu-id="41214-113">Remarks</span></span>

<span data-ttu-id="41214-114">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="41214-114">Equivalent to:</span></span>

```qsharp
Measure([PauliZ], [qubit]);
```