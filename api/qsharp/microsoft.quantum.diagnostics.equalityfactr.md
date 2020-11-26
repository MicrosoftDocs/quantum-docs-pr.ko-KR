---
uid: Microsoft.Quantum.Diagnostics.EqualityFactR
title: EqualityFactR 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactR
qsharp.summary: Asserts that a classical Result variable has the expected value.
ms.openlocfilehash: 166dff211d6db9da5d39c607af1924ffd6d276dd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201770"
---
# <a name="equalityfactr-function"></a><span data-ttu-id="7d30a-102">EqualityFactR 함수</span><span class="sxs-lookup"><span data-stu-id="7d30a-102">EqualityFactR function</span></span>

<span data-ttu-id="7d30a-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="7d30a-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="7d30a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7d30a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7d30a-105">기존 결과 변수가 예상 값을 가지는 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d30a-105">Asserts that a classical Result variable has the expected value.</span></span>

```qsharp
function EqualityFactR (actual : Result, expected : Result, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="7d30a-106">입력</span><span class="sxs-lookup"><span data-stu-id="7d30a-106">Input</span></span>

### <a name="actual--__invalidresult__"></a><span data-ttu-id="7d30a-107">실제: __유효 <Result> 하지 않음__</span><span class="sxs-lookup"><span data-stu-id="7d30a-107">actual : __invalid<Result>__</span></span>

<span data-ttu-id="7d30a-108">검사할 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="7d30a-108">The variable to be checked.</span></span>


### <a name="expected--__invalidresult__"></a><span data-ttu-id="7d30a-109">예상: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="7d30a-109">expected : __invalid<Result>__</span></span>

<span data-ttu-id="7d30a-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="7d30a-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="7d30a-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="7d30a-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="7d30a-112">어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="7d30a-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7d30a-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7d30a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

