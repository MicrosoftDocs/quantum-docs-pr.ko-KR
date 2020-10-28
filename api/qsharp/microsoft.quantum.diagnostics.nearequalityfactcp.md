---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactCP
title: NearEqualityFactCP 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactCP
qsharp.summary: Asserts that a classical complex number has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 1d62d25a3d04c431440cf8fc1eb585cac2c73f2e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712657"
---
# <a name="nearequalityfactcp-function"></a><span data-ttu-id="2b9db-102">NearEqualityFactCP 함수</span><span class="sxs-lookup"><span data-stu-id="2b9db-102">NearEqualityFactCP function</span></span>

<span data-ttu-id="2b9db-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="2b9db-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="2b9db-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2b9db-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2b9db-105">기존 복소수에 필요한 값이 1e-10의 작은 허용 오차 보다 많은 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b9db-105">Asserts that a classical complex number has the expected value up to a small tolerance of 1e-10.</span></span>

```qsharp
function NearEqualityFactCP (actual : Microsoft.Quantum.Math.ComplexPolar, expected : Microsoft.Quantum.Math.ComplexPolar) : Unit
```


## <a name="input"></a><span data-ttu-id="2b9db-106">입력</span><span class="sxs-lookup"><span data-stu-id="2b9db-106">Input</span></span>

### <a name="actual--complexpolar"></a><span data-ttu-id="2b9db-107">실제: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="2b9db-107">actual : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="2b9db-108">확인할 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="2b9db-108">The number to be checked.</span></span>


### <a name="expected--complexpolar"></a><span data-ttu-id="2b9db-109">예상: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="2b9db-109">expected : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="2b9db-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2b9db-110">The expected value.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2b9db-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2b9db-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

