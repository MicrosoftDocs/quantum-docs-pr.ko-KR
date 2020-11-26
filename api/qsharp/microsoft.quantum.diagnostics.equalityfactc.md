---
uid: Microsoft.Quantum.Diagnostics.EqualityFactC
title: EqualityFactC 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactC
qsharp.summary: Asserts that a complex number has the expected value.
ms.openlocfilehash: e33d25899580a127171fb45a92d77cfdb5003a21
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201906"
---
# <a name="equalityfactc-function"></a><span data-ttu-id="2b7b0-102">EqualityFactC 함수</span><span class="sxs-lookup"><span data-stu-id="2b7b0-102">EqualityFactC function</span></span>

<span data-ttu-id="2b7b0-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="2b7b0-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="2b7b0-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2b7b0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2b7b0-105">복소수에 필요한 값이 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b7b0-105">Asserts that a complex number has the expected value.</span></span>

```qsharp
function EqualityFactC (actual : Microsoft.Quantum.Math.Complex, expected : Microsoft.Quantum.Math.Complex, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="2b7b0-106">입력</span><span class="sxs-lookup"><span data-stu-id="2b7b0-106">Input</span></span>

### <a name="actual--complex"></a><span data-ttu-id="2b7b0-107">실제: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="2b7b0-107">actual : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="2b7b0-108">확인할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2b7b0-108">The value to be checked.</span></span>


### <a name="expected--complex"></a><span data-ttu-id="2b7b0-109">예상: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="2b7b0-109">expected : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="2b7b0-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2b7b0-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="2b7b0-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="2b7b0-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="2b7b0-112">어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="2b7b0-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2b7b0-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2b7b0-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

