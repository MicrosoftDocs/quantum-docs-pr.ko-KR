---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactB
title: AllEqualityFactB 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactB
qsharp.summary: Asserts that two arrays of boolean values are equal.
ms.openlocfilehash: 79dcf65956ba9436fb6fdd452f22f35d4852d6f8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213704"
---
# <a name="allequalityfactb-function"></a><span data-ttu-id="f9943-102">AllEqualityFactB 함수</span><span class="sxs-lookup"><span data-stu-id="f9943-102">AllEqualityFactB function</span></span>

<span data-ttu-id="f9943-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="f9943-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="f9943-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f9943-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f9943-105">부울 값의 두 배열이 동일한 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9943-105">Asserts that two arrays of boolean values are equal.</span></span>

```qsharp
function AllEqualityFactB (actual : Bool[], expected : Bool[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="f9943-106">입력</span><span class="sxs-lookup"><span data-stu-id="f9943-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="f9943-107">actual: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="f9943-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="f9943-108">관련 테스트 사례에 의해 생성 되는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f9943-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--bool"></a><span data-ttu-id="f9943-109">예상: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="f9943-109">expected : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="f9943-110">관련 테스트 사례에서 예상 되는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f9943-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="f9943-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="f9943-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="f9943-112">배열이 같지 않으면 인쇄할 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="f9943-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f9943-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f9943-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

