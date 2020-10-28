---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: R 코딩 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: ef9be0f0628c8ba8c5f131cc558bdcda6bb6ea55
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725478"
---
# <a name="rmencoding-function"></a><span data-ttu-id="b34aa-102">R 코딩 함수</span><span class="sxs-lookup"><span data-stu-id="b34aa-102">RMEncoding function</span></span>

<span data-ttu-id="b34aa-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="b34aa-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="b34aa-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b34aa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b34aa-105">{-1,1} 부울 값 코딩</span><span class="sxs-lookup"><span data-stu-id="b34aa-105">{-1,1} coding of a Boolean truth value</span></span>

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a><span data-ttu-id="b34aa-106">입력</span><span class="sxs-lookup"><span data-stu-id="b34aa-106">Input</span></span>

### <a name="b--bool"></a><span data-ttu-id="b34aa-107">b: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b34aa-107">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b34aa-108">부울 값</span><span class="sxs-lookup"><span data-stu-id="b34aa-108">Boolean value</span></span>



## <a name="output--int"></a><span data-ttu-id="b34aa-109">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b34aa-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b34aa-110">가 false 이면 1이 고, `b` 그렇지 않으면-1입니다.</span><span class="sxs-lookup"><span data-stu-id="b34aa-110">1, if `b` is false, otherwise -1</span></span>