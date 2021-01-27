---
uid: Microsoft.Quantum.Intrinsic.M
title: M 연산
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: M
qsharp.summary: >-
  Performs a measurement of a single qubit in the Pauli $Z$ basis.

  The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}. \end{align}
ms.openlocfilehash: 0037d7f5ad060857c6ca2c863b1d24aca3e338cf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818866"
---
# <a name="m-operation"></a><span data-ttu-id="12fcc-102">M 연산</span><span class="sxs-lookup"><span data-stu-id="12fcc-102">M operation</span></span>

<span data-ttu-id="12fcc-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="12fcc-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="12fcc-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="12fcc-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="12fcc-105">Pauli $Z $ 기준에서 단일 고 비트를 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12fcc-105">Performs a measurement of a single qubit in the Pauli $Z$ basis.</span></span>

<span data-ttu-id="12fcc-106">출력 결과는 배포 \begin{align} \Pr (\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.에 의해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="12fcc-106">The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.</span></span>
<span data-ttu-id="12fcc-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="12fcc-107">\end{align}</span></span>

```qsharp
operation M (qubit : Qubit) : Result
```


## <a name="input"></a><span data-ttu-id="12fcc-108">입력</span><span class="sxs-lookup"><span data-stu-id="12fcc-108">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="12fcc-109">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="12fcc-109">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="12fcc-110">측정할 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="12fcc-110">Qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="12fcc-111">출력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="12fcc-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="12fcc-112">`Zero` $ + $1 eigenvalue가 관찰 되 면이 고, `One` $-$1 eigenvalue가 관찰 되 면입니다.</span><span class="sxs-lookup"><span data-stu-id="12fcc-112">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="12fcc-113">설명</span><span class="sxs-lookup"><span data-stu-id="12fcc-113">Remarks</span></span>

<span data-ttu-id="12fcc-114">다음에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="12fcc-114">Equivalent to:</span></span>

```qsharp
Measure([PauliZ], [qubit]);
```