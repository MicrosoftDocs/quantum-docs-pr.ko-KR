---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: 모순 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: 7d62c9341b768dfdfbfbf8e73e64748f04317595
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829355"
---
# <a name="contradiction-function"></a><span data-ttu-id="c3549-102">모순 함수</span><span class="sxs-lookup"><span data-stu-id="c3549-102">Contradiction function</span></span>

<span data-ttu-id="c3549-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="c3549-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="c3549-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c3549-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c3549-105">는 기존 조건이 false 임을 선언 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3549-105">Declares that a classical condition is false.</span></span>

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="c3549-106">입력</span><span class="sxs-lookup"><span data-stu-id="c3549-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="c3549-107">actual: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c3549-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c3549-108">선언 될 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="c3549-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="c3549-109">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="c3549-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="c3549-110">고전 조건이 true 인 경우 인쇄 될 실패 메시지 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="c3549-110">Failure message string to be printed in the case that the classical condition is true.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c3549-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c3549-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="c3549-112">예</span><span class="sxs-lookup"><span data-stu-id="c3549-112">Example</span></span>

<span data-ttu-id="c3549-113">다음 Q # 코드는 "Hello, 세계"를 인쇄 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3549-113">The following Q# code will print "Hello, world":</span></span>

```qsharp
Contradiction(2 == 3, "2 is not equal to 3.");
Message("Hello, world.");
```

## <a name="see-also"></a><span data-ttu-id="c3549-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c3549-114">See Also</span></span>

- [<span data-ttu-id="c3549-115">Microsoft 양자 진단 팩트</span><span class="sxs-lookup"><span data-stu-id="c3549-115">Microsoft.Quantum.Diagnostics.Fact</span></span>](xref:Microsoft.Quantum.Diagnostics.Fact)