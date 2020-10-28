---
uid: Microsoft.Quantum.Canon.Fst
title: Fst 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 88ff5e29de9eeefcc1e207f277c37c63cb0faade
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716185"
---
# <a name="fst-function"></a><span data-ttu-id="e89ba-102">Fst 함수</span><span class="sxs-lookup"><span data-stu-id="e89ba-102">Fst function</span></span>

<span data-ttu-id="e89ba-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e89ba-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e89ba-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e89ba-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e89ba-105">쌍이 지정 된 경우 첫 번째 요소를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e89ba-105">Given a pair, returns its first element.</span></span>

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a><span data-ttu-id="e89ba-106">입력</span><span class="sxs-lookup"><span data-stu-id="e89ba-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="e89ba-107">pair: (' t ', ' U)</span><span class="sxs-lookup"><span data-stu-id="e89ba-107">pair : ('T,'U)</span></span>

<span data-ttu-id="e89ba-108">두 개의 요소가 포함 된 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="e89ba-108">A tuple with two elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="e89ba-109">출력: ' '</span><span class="sxs-lookup"><span data-stu-id="e89ba-109">Output : 'T</span></span>

<span data-ttu-id="e89ba-110">`pair`의 첫 번째 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="e89ba-110">The first element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e89ba-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e89ba-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e89ba-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="e89ba-112">'T</span></span>

<span data-ttu-id="e89ba-113">쌍의 첫 번째 멤버의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e89ba-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="e89ba-114">' U</span><span class="sxs-lookup"><span data-stu-id="e89ba-114">'U</span></span>

<span data-ttu-id="e89ba-115">쌍의 두 번째 멤버의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e89ba-115">The type of the pair's second member.</span></span>