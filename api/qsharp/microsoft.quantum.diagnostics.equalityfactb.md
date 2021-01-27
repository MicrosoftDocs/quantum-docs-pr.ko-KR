---
uid: Microsoft.Quantum.Diagnostics.EqualityFactB
title: EqualityFactB 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactB
qsharp.summary: Asserts that a classical Bool variable has the expected value.
ms.openlocfilehash: cb1d4c471c528d2d3c08c92619fafd532a88c8f0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829218"
---
# <a name="equalityfactb-function"></a><span data-ttu-id="852d4-102">EqualityFactB 함수</span><span class="sxs-lookup"><span data-stu-id="852d4-102">EqualityFactB function</span></span>

<span data-ttu-id="852d4-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="852d4-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="852d4-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="852d4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="852d4-105">기존 Bool 변수에 예상 값이 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="852d4-105">Asserts that a classical Bool variable has the expected value.</span></span>

```qsharp
function EqualityFactB (actual : Bool, expected : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="852d4-106">입력</span><span class="sxs-lookup"><span data-stu-id="852d4-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="852d4-107">actual: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="852d4-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="852d4-108">검사할 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="852d4-108">The variable to be checked.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="852d4-109">예상: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="852d4-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="852d4-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="852d4-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="852d4-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="852d4-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="852d4-112">어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="852d4-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="852d4-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="852d4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

