---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactCP
title: NearEqualityFactCP 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactCP
qsharp.summary: Asserts that a classical complex number has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 477449913732950ad26adc0cdabaaaab803a20c3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853277"
---
# <a name="nearequalityfactcp-function"></a><span data-ttu-id="cb035-102">NearEqualityFactCP 함수</span><span class="sxs-lookup"><span data-stu-id="cb035-102">NearEqualityFactCP function</span></span>

<span data-ttu-id="cb035-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="cb035-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="cb035-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cb035-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cb035-105">기존 복소수에 필요한 값이 1e-10의 작은 허용 오차 보다 많은 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb035-105">Asserts that a classical complex number has the expected value up to a small tolerance of 1e-10.</span></span>

```qsharp
function NearEqualityFactCP (actual : Microsoft.Quantum.Math.ComplexPolar, expected : Microsoft.Quantum.Math.ComplexPolar) : Unit
```


## <a name="input"></a><span data-ttu-id="cb035-106">입력</span><span class="sxs-lookup"><span data-stu-id="cb035-106">Input</span></span>

### <a name="actual--complexpolar"></a><span data-ttu-id="cb035-107">실제: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="cb035-107">actual : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="cb035-108">확인할 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="cb035-108">The number to be checked.</span></span>


### <a name="expected--complexpolar"></a><span data-ttu-id="cb035-109">예상: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="cb035-109">expected : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="cb035-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="cb035-110">The expected value.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cb035-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cb035-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

