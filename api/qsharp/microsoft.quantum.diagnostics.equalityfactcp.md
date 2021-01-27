---
uid: Microsoft.Quantum.Diagnostics.EqualityFactCP
title: EqualityFactCP 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactCP
qsharp.summary: Asserts that a complex number has the expected value.
ms.openlocfilehash: a207ba1c4d08ec58095f5db34ee32c7341002920
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829184"
---
# <a name="equalityfactcp-function"></a><span data-ttu-id="91635-102">EqualityFactCP 함수</span><span class="sxs-lookup"><span data-stu-id="91635-102">EqualityFactCP function</span></span>

<span data-ttu-id="91635-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="91635-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="91635-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="91635-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="91635-105">복소수에 필요한 값이 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="91635-105">Asserts that a complex number has the expected value.</span></span>

```qsharp
function EqualityFactCP (actual : Microsoft.Quantum.Math.ComplexPolar, expected : Microsoft.Quantum.Math.ComplexPolar, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="91635-106">입력</span><span class="sxs-lookup"><span data-stu-id="91635-106">Input</span></span>

### <a name="actual--complexpolar"></a><span data-ttu-id="91635-107">실제: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="91635-107">actual : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="91635-108">확인할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="91635-108">The value to be checked.</span></span>


### <a name="expected--complexpolar"></a><span data-ttu-id="91635-109">예상: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="91635-109">expected : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="91635-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="91635-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="91635-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="91635-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="91635-112">어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="91635-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="91635-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="91635-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

