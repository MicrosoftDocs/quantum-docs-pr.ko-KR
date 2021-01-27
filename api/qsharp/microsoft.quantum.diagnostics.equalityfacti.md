---
uid: Microsoft.Quantum.Diagnostics.EqualityFactI
title: EqualityFactI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityFactI
qsharp.summary: Asserts that a classical Int variable has the expected value.
ms.openlocfilehash: c41cb5548e8dfebb4d1c1a1c052306878c85e821
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853344"
---
# <a name="equalityfacti-function"></a><span data-ttu-id="03acc-102">EqualityFactI 함수</span><span class="sxs-lookup"><span data-stu-id="03acc-102">EqualityFactI function</span></span>

<span data-ttu-id="03acc-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="03acc-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="03acc-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="03acc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="03acc-105">기존 Int 변수에 예상 값이 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="03acc-105">Asserts that a classical Int variable has the expected value.</span></span>

```qsharp
function EqualityFactI (actual : Int, expected : Int, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="03acc-106">입력</span><span class="sxs-lookup"><span data-stu-id="03acc-106">Input</span></span>

### <a name="actual--int"></a><span data-ttu-id="03acc-107">실제: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="03acc-107">actual : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="03acc-108">확인할 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="03acc-108">The number to be checked.</span></span>


### <a name="expected--int"></a><span data-ttu-id="03acc-109">예상: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="03acc-109">expected : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="03acc-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="03acc-110">The expected value.</span></span>


### <a name="message--string"></a><span data-ttu-id="03acc-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="03acc-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="03acc-112">어설션이 트리거될 때 사용할 오류 메시지 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="03acc-112">Failure message string to be used when the assertion is triggered.</span></span>



## <a name="output--unit"></a><span data-ttu-id="03acc-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="03acc-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

