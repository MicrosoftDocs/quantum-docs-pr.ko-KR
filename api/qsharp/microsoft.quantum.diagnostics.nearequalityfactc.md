---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactC
title: NearEqualityFactC 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactC
qsharp.summary: Asserts that a classical complex number has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 410ec8eb23501c80852b6d5a105ba5fb177110e4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98828264"
---
# <a name="nearequalityfactc-function"></a><span data-ttu-id="63d3f-102">NearEqualityFactC 함수</span><span class="sxs-lookup"><span data-stu-id="63d3f-102">NearEqualityFactC function</span></span>

<span data-ttu-id="63d3f-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="63d3f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="63d3f-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="63d3f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="63d3f-105">기존 복소수에 필요한 값이 1e-10의 작은 허용 오차 보다 많은 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="63d3f-105">Asserts that a classical complex number has the expected value up to a small tolerance of 1e-10.</span></span>

```qsharp
function NearEqualityFactC (actual : Microsoft.Quantum.Math.Complex, expected : Microsoft.Quantum.Math.Complex) : Unit
```


## <a name="input"></a><span data-ttu-id="63d3f-106">입력</span><span class="sxs-lookup"><span data-stu-id="63d3f-106">Input</span></span>

### <a name="actual--complex"></a><span data-ttu-id="63d3f-107">실제: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="63d3f-107">actual : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="63d3f-108">확인할 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="63d3f-108">The number to be checked.</span></span>


### <a name="expected--complex"></a><span data-ttu-id="63d3f-109">예상: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="63d3f-109">expected : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="63d3f-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="63d3f-110">The expected value.</span></span>



## <a name="output--unit"></a><span data-ttu-id="63d3f-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="63d3f-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

