---
uid: Microsoft.Quantum.Synthesis.Encoded
title: 인코딩된 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 6b9d21969ee90f3928b65a1c97a5b0f15157e381
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725205"
---
# <a name="encoded-function"></a><span data-ttu-id="c2686-102">인코딩된 함수</span><span class="sxs-lookup"><span data-stu-id="c2686-102">Encoded function</span></span>

<span data-ttu-id="c2686-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="c2686-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="c2686-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c2686-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c2686-105">코딩에서 참 테이블 인코딩 {1,-1}</span><span class="sxs-lookup"><span data-stu-id="c2686-105">Encode truth table in {1,-1} coding</span></span>

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="c2686-106">입력</span><span class="sxs-lookup"><span data-stu-id="c2686-106">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="c2686-107">테이블: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="c2686-107">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="c2686-108">참 테이블을 실제 값 배열로</span><span class="sxs-lookup"><span data-stu-id="c2686-108">Truth table as array of truth values</span></span>



## <a name="output--int"></a><span data-ttu-id="c2686-109">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c2686-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c2686-110">정수 배열로 서의 참 테이블 {1,-1}</span><span class="sxs-lookup"><span data-stu-id="c2686-110">Truth table as array of {1,-1} integers</span></span>