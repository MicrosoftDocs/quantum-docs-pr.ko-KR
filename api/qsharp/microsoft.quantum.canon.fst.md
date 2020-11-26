---
uid: Microsoft.Quantum.Canon.Fst
title: Fst 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 634f11881a054df7fe79d889832ea6bd80a7394f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206938"
---
# <a name="fst-function"></a><span data-ttu-id="b74ff-102">Fst 함수</span><span class="sxs-lookup"><span data-stu-id="b74ff-102">Fst function</span></span>

<span data-ttu-id="b74ff-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b74ff-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b74ff-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b74ff-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b74ff-105">쌍이 지정 된 경우 첫 번째 요소를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b74ff-105">Given a pair, returns its first element.</span></span>

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a><span data-ttu-id="b74ff-106">입력</span><span class="sxs-lookup"><span data-stu-id="b74ff-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="b74ff-107">pair: (' t ', ' U)</span><span class="sxs-lookup"><span data-stu-id="b74ff-107">pair : ('T,'U)</span></span>

<span data-ttu-id="b74ff-108">두 개의 요소가 포함 된 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="b74ff-108">A tuple with two elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="b74ff-109">출력: ' '</span><span class="sxs-lookup"><span data-stu-id="b74ff-109">Output : 'T</span></span>

<span data-ttu-id="b74ff-110">`pair`의 첫 번째 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b74ff-110">The first element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b74ff-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b74ff-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b74ff-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="b74ff-112">'T</span></span>

<span data-ttu-id="b74ff-113">쌍의 첫 번째 멤버의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b74ff-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="b74ff-114">' U</span><span class="sxs-lookup"><span data-stu-id="b74ff-114">'U</span></span>

<span data-ttu-id="b74ff-115">쌍의 두 번째 멤버의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b74ff-115">The type of the pair's second member.</span></span>