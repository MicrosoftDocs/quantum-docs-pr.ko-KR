---
uid: Microsoft.Quantum.Diagnostics.EqualityFactCP
title: EqualityFactCP 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactCP
qsharp.summary: Asserts that a complex number has the expected value.
ms.openlocfilehash: 1ea790debb5a9123fb8bee3a5f8a1fde0a050b37
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712769"
---
# <a name="equalityfactcp-function"></a><span data-ttu-id="22e6a-102">EqualityFactCP 함수</span><span class="sxs-lookup"><span data-stu-id="22e6a-102">EqualityFactCP function</span></span>

<span data-ttu-id="22e6a-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="22e6a-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="22e6a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="22e6a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="22e6a-105">복소수에 필요한 값이 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="22e6a-105">Asserts that a complex number has the expected value.</span></span>

```qsharp
function EqualityFactCP (actual : Microsoft.Quantum.Math.ComplexPolar, expected : Microsoft.Quantum.Math.ComplexPolar, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="22e6a-106">입력</span><span class="sxs-lookup"><span data-stu-id="22e6a-106">Input</span></span>

### <a name="actual--complexpolar"></a><span data-ttu-id="22e6a-107">실제: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="22e6a-107">actual : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="22e6a-108">확인할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="22e6a-108">The value to be checked.</span></span>


### <a name="expected--complexpolar"></a><span data-ttu-id="22e6a-109">예상: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="22e6a-109">expected : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="22e6a-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="22e6a-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="22e6a-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="22e6a-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="22e6a-112">어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="22e6a-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="22e6a-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="22e6a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

