---
uid: Microsoft.Quantum.Synthesis.Encoded
title: 인코딩된 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 44f6b247e6bfab7b55c46146cb63f8b6d219955b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855492"
---
# <a name="encoded-function"></a><span data-ttu-id="07528-102">인코딩된 함수</span><span class="sxs-lookup"><span data-stu-id="07528-102">Encoded function</span></span>

<span data-ttu-id="07528-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="07528-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="07528-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="07528-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="07528-105">코딩에서 참 테이블 인코딩 {1,-1}</span><span class="sxs-lookup"><span data-stu-id="07528-105">Encode truth table in {1,-1} coding</span></span>

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="07528-106">입력</span><span class="sxs-lookup"><span data-stu-id="07528-106">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="07528-107">테이블: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="07528-107">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="07528-108">참 테이블을 실제 값 배열로</span><span class="sxs-lookup"><span data-stu-id="07528-108">Truth table as array of truth values</span></span>



## <a name="output--int"></a><span data-ttu-id="07528-109">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="07528-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="07528-110">정수 배열로 서의 참 테이블 {1,-1}</span><span class="sxs-lookup"><span data-stu-id="07528-110">Truth table as array of {1,-1} integers</span></span>

## <a name="example"></a><span data-ttu-id="07528-111">예제</span><span class="sxs-lookup"><span data-stu-id="07528-111">Example</span></span>

```qsharp
Encoded([false, false, false, true]); // [1, 1, 1, -1]
```