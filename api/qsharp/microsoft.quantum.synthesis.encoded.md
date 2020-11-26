---
uid: Microsoft.Quantum.Synthesis.Encoded
title: 인코딩된 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 803f35b9e7af547bc34f21de74684fba885bfda9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203181"
---
# <a name="encoded-function"></a><span data-ttu-id="ad9b1-102">인코딩된 함수</span><span class="sxs-lookup"><span data-stu-id="ad9b1-102">Encoded function</span></span>

<span data-ttu-id="ad9b1-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="ad9b1-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="ad9b1-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ad9b1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ad9b1-105">코딩에서 참 테이블 인코딩 {1,-1}</span><span class="sxs-lookup"><span data-stu-id="ad9b1-105">Encode truth table in {1,-1} coding</span></span>

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="ad9b1-106">입력</span><span class="sxs-lookup"><span data-stu-id="ad9b1-106">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="ad9b1-107">테이블: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="ad9b1-107">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="ad9b1-108">참 테이블을 실제 값 배열로</span><span class="sxs-lookup"><span data-stu-id="ad9b1-108">Truth table as array of truth values</span></span>



## <a name="output--int"></a><span data-ttu-id="ad9b1-109">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ad9b1-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ad9b1-110">정수 배열로 서의 참 테이블 {1,-1}</span><span class="sxs-lookup"><span data-stu-id="ad9b1-110">Truth table as array of {1,-1} integers</span></span>