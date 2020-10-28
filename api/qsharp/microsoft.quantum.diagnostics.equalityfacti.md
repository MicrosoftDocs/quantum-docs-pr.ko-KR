---
uid: Microsoft.Quantum.Diagnostics.EqualityFactI
title: EqualityFactI 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactI
qsharp.summary: Asserts that a classical Int variable has the expected value.
ms.openlocfilehash: 34bb38a9447f71372ec0b234731f31a5818d3af1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712762"
---
# <a name="equalityfacti-function"></a><span data-ttu-id="3cae3-102">EqualityFactI 함수</span><span class="sxs-lookup"><span data-stu-id="3cae3-102">EqualityFactI function</span></span>

<span data-ttu-id="3cae3-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="3cae3-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="3cae3-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3cae3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3cae3-105">기존 Int 변수에 예상 값이 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cae3-105">Asserts that a classical Int variable has the expected value.</span></span>

```qsharp
function EqualityFactI (actual : Int, expected : Int, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="3cae3-106">입력</span><span class="sxs-lookup"><span data-stu-id="3cae3-106">Input</span></span>

### <a name="actual--int"></a><span data-ttu-id="3cae3-107">실제: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3cae3-107">actual : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3cae3-108">확인할 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="3cae3-108">The number to be checked.</span></span>


### <a name="expected--int"></a><span data-ttu-id="3cae3-109">예상: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3cae3-109">expected : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3cae3-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3cae3-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="3cae3-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="3cae3-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="3cae3-112">어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="3cae3-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3cae3-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3cae3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

