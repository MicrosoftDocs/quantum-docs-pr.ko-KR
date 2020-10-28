---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: 모순 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: a5f3f26c5ada2eea9206699a2cc77575a9b5eebd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712867"
---
# <a name="contradiction-function"></a><span data-ttu-id="16457-102">모순 함수</span><span class="sxs-lookup"><span data-stu-id="16457-102">Contradiction function</span></span>

<span data-ttu-id="16457-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="16457-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="16457-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="16457-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="16457-105">는 기존 조건이 false 임을 선언 합니다.</span><span class="sxs-lookup"><span data-stu-id="16457-105">Declares that a classical condition is false.</span></span>

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="16457-106">입력</span><span class="sxs-lookup"><span data-stu-id="16457-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="16457-107">actual: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="16457-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="16457-108">선언 될 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="16457-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="16457-109">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="16457-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="16457-110">고전 조건이 true 인 경우 인쇄 될 실패 메시지 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="16457-110">Failure message string to be printed in the case that the classical condition is true.</span></span>



## <a name="output--unit"></a><span data-ttu-id="16457-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="16457-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="16457-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="16457-112">See Also</span></span>

- [<span data-ttu-id="16457-113">Microsoft 양자 진단 팩트</span><span class="sxs-lookup"><span data-stu-id="16457-113">Microsoft.Quantum.Diagnostics.Fact</span></span>](xref:Microsoft.Quantum.Diagnostics.Fact)