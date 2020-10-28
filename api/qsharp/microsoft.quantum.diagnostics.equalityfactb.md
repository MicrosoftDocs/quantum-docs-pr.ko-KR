---
uid: Microsoft.Quantum.Diagnostics.EqualityFactB
title: EqualityFactB 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactB
qsharp.summary: Asserts that a classical Bool variable has the expected value.
ms.openlocfilehash: d3163281772bda392fbdd61ad58543e22022a600
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712776"
---
# <a name="equalityfactb-function"></a><span data-ttu-id="77b0f-102">EqualityFactB 함수</span><span class="sxs-lookup"><span data-stu-id="77b0f-102">EqualityFactB function</span></span>

<span data-ttu-id="77b0f-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="77b0f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="77b0f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="77b0f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="77b0f-105">기존 Bool 변수에 예상 값이 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="77b0f-105">Asserts that a classical Bool variable has the expected value.</span></span>

```qsharp
function EqualityFactB (actual : Bool, expected : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="77b0f-106">입력</span><span class="sxs-lookup"><span data-stu-id="77b0f-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="77b0f-107">actual: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="77b0f-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="77b0f-108">검사할 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="77b0f-108">The variable to be checked.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="77b0f-109">예상: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="77b0f-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="77b0f-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="77b0f-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="77b0f-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="77b0f-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="77b0f-112">어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="77b0f-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="77b0f-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="77b0f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

