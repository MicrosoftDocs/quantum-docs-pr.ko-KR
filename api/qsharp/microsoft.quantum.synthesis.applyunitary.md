---
uid: Microsoft.Quantum.Synthesis.ApplyUnitary
title: ApplyUnitary 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyUnitary
qsharp.summary: >-
  Applies gate defined by 2^n x 2^n unitary matrix.

  Fails if matrix is not unitary, or has wrong size.
ms.openlocfilehash: 58215d3b05b8c6974e979d21a13869f27b436310
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859218"
---
# <a name="applyunitary-operation"></a><span data-ttu-id="7455a-102">ApplyUnitary 작업</span><span class="sxs-lookup"><span data-stu-id="7455a-102">ApplyUnitary operation</span></span>

<span data-ttu-id="7455a-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="7455a-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="7455a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7455a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7455a-105">2 ^ n x 2 ^ n 단일 행렬로 정의 된 게이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7455a-105">Applies gate defined by 2^n x 2^n unitary matrix.</span></span>

<span data-ttu-id="7455a-106">Matrix가 단일 요소가 아니거나 크기가 잘못 된 경우 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="7455a-106">Fails if matrix is not unitary, or has wrong size.</span></span>

```qsharp
operation ApplyUnitary (unitary : Microsoft.Quantum.Math.Complex[][], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7455a-107">입력</span><span class="sxs-lookup"><span data-stu-id="7455a-107">Input</span></span>

### <a name="unitary--complex"></a><span data-ttu-id="7455a-108">단일: [복합](xref:Microsoft.Quantum.Math.Complex)[] []</span><span class="sxs-lookup"><span data-stu-id="7455a-108">unitary : [Complex](xref:Microsoft.Quantum.Math.Complex)[][]</span></span>

<span data-ttu-id="7455a-109">2 ^ n x 2 ^ n 단일 행렬 작업을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7455a-109">2^n x 2^n unitary matrix describing the operation.</span></span>
<span data-ttu-id="7455a-110">Matrix가 단일 크기가 아니거나 적절 한 크기가 아닌 경우는 예외를 throw 합니다.</span><span class="sxs-lookup"><span data-stu-id="7455a-110">If matrix is not unitary or not of suitable size, throws an exception.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="7455a-111">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7455a-111">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7455a-112">작업 (길이 n의 레지스터)을 적용 하는 이상 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="7455a-112">Qubits to which apply the operation - register of length n.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7455a-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7455a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

