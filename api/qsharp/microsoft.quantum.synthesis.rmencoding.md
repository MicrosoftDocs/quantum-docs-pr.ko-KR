---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: R 코딩 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: a506ccb637b331a392ea75383c8bd605114af059
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202943"
---
# <a name="rmencoding-function"></a><span data-ttu-id="3bc0f-102">R 코딩 함수</span><span class="sxs-lookup"><span data-stu-id="3bc0f-102">RMEncoding function</span></span>

<span data-ttu-id="3bc0f-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="3bc0f-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="3bc0f-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3bc0f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3bc0f-105">{-1,1} 부울 값 코딩</span><span class="sxs-lookup"><span data-stu-id="3bc0f-105">{-1,1} coding of a Boolean truth value</span></span>

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a><span data-ttu-id="3bc0f-106">입력</span><span class="sxs-lookup"><span data-stu-id="3bc0f-106">Input</span></span>

### <a name="b--bool"></a><span data-ttu-id="3bc0f-107">b: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3bc0f-107">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3bc0f-108">부울 값</span><span class="sxs-lookup"><span data-stu-id="3bc0f-108">Boolean value</span></span>



## <a name="output--int"></a><span data-ttu-id="3bc0f-109">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3bc0f-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3bc0f-110">가 false 이면 1이 고, `b` 그렇지 않으면-1입니다.</span><span class="sxs-lookup"><span data-stu-id="3bc0f-110">1, if `b` is false, otherwise -1</span></span>