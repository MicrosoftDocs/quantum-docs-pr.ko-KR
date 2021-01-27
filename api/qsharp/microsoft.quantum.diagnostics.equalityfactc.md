---
uid: Microsoft.Quantum.Diagnostics.EqualityFactC
title: EqualityFactC 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactC
qsharp.summary: Asserts that a complex number has the expected value.
ms.openlocfilehash: 0fcfe553d7a0050a9ab35a43ac5fe2b1958514db
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853373"
---
# <a name="equalityfactc-function"></a><span data-ttu-id="07e44-102">EqualityFactC 함수</span><span class="sxs-lookup"><span data-stu-id="07e44-102">EqualityFactC function</span></span>

<span data-ttu-id="07e44-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="07e44-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="07e44-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="07e44-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="07e44-105">복소수에 필요한 값이 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="07e44-105">Asserts that a complex number has the expected value.</span></span>

```qsharp
function EqualityFactC (actual : Microsoft.Quantum.Math.Complex, expected : Microsoft.Quantum.Math.Complex, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="07e44-106">입력</span><span class="sxs-lookup"><span data-stu-id="07e44-106">Input</span></span>

### <a name="actual--complex"></a><span data-ttu-id="07e44-107">실제: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="07e44-107">actual : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="07e44-108">확인할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="07e44-108">The value to be checked.</span></span>


### <a name="expected--complex"></a><span data-ttu-id="07e44-109">예상: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="07e44-109">expected : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="07e44-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="07e44-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="07e44-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="07e44-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="07e44-112">어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="07e44-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="07e44-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="07e44-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

