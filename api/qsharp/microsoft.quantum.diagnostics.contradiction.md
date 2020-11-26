---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: 모순 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: f9ad9a7d67bda8e50c76f679f535ad55ba07698e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202144"
---
# <a name="contradiction-function"></a><span data-ttu-id="fb389-102">모순 함수</span><span class="sxs-lookup"><span data-stu-id="fb389-102">Contradiction function</span></span>

<span data-ttu-id="fb389-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="fb389-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="fb389-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="fb389-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="fb389-105">는 기존 조건이 false 임을 선언 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb389-105">Declares that a classical condition is false.</span></span>

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="fb389-106">입력</span><span class="sxs-lookup"><span data-stu-id="fb389-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="fb389-107">actual: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fb389-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fb389-108">선언 될 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="fb389-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="fb389-109">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="fb389-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="fb389-110">고전 조건이 true 인 경우 인쇄 될 실패 메시지 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="fb389-110">Failure message string to be printed in the case that the classical condition is true.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fb389-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fb389-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="fb389-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="fb389-112">See Also</span></span>

- [<span data-ttu-id="fb389-113">Microsoft 양자 진단 팩트</span><span class="sxs-lookup"><span data-stu-id="fb389-113">Microsoft.Quantum.Diagnostics.Fact</span></span>](xref:Microsoft.Quantum.Diagnostics.Fact)