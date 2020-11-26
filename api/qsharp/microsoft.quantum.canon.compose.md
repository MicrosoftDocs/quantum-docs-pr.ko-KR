---
uid: Microsoft.Quantum.Canon.Compose
title: 작성 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: f8c6ad36220b48be1723c2d91cbf7c0a4947af14
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216764"
---
# <a name="compose-function"></a><span data-ttu-id="7397c-102">작성 함수</span><span class="sxs-lookup"><span data-stu-id="7397c-102">Compose function</span></span>

<span data-ttu-id="7397c-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7397c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7397c-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7397c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7397c-105">두 함수의 컴퍼지션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7397c-105">Returns the composition of two functions.</span></span>

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a><span data-ttu-id="7397c-106">Description</span><span class="sxs-lookup"><span data-stu-id="7397c-106">Description</span></span>

<span data-ttu-id="7397c-107">$ 및 $g $ $f 두 개의 함수가 지정 된 경우 $f \circ g $를 나타내는 새 함수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7397c-107">Given two functions $f$ and $g$, returns a new function representing $f \circ g$.</span></span>

## <a name="input"></a><span data-ttu-id="7397c-108">입력</span><span class="sxs-lookup"><span data-stu-id="7397c-108">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="7397c-109">외부: ' U-> ' V</span><span class="sxs-lookup"><span data-stu-id="7397c-109">outer : 'U -> 'V</span></span>

<span data-ttu-id="7397c-110">적용할 두 번째 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="7397c-110">The second function to be applied.</span></span>


### <a name="inner--t---u"></a><span data-ttu-id="7397c-111">inner: ' t-> ' U</span><span class="sxs-lookup"><span data-stu-id="7397c-111">inner : 'T -> 'U</span></span>

<span data-ttu-id="7397c-112">적용할 첫 번째 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="7397c-112">The first function to be applied.</span></span>



## <a name="output--t---v"></a><span data-ttu-id="7397c-113">출력: ' t ' > ' V</span><span class="sxs-lookup"><span data-stu-id="7397c-113">Output : 'T -> 'V</span></span>

<span data-ttu-id="7397c-114">$, $F (g (x)) = h (x) $ $x 모든 입력에 대 한 새 함수는 $를 $h 합니다.</span><span class="sxs-lookup"><span data-stu-id="7397c-114">A new function $h$ such that for all inputs $x$, $f(g(x)) = h(x)$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7397c-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7397c-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7397c-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="7397c-116">'T</span></span>

<span data-ttu-id="7397c-117">적용할 첫 번째 함수의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7397c-117">The input type of the first function to be applied.</span></span>
### <a name="u"></a><span data-ttu-id="7397c-118">' U</span><span class="sxs-lookup"><span data-stu-id="7397c-118">'U</span></span>

<span data-ttu-id="7397c-119">적용할 첫 번째 함수의 출력 형식과 적용할 두 번째 함수의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7397c-119">The output type of the first function to be applied and the input type of the second function to be applied.</span></span>
### <a name="v"></a><span data-ttu-id="7397c-120">' V</span><span class="sxs-lookup"><span data-stu-id="7397c-120">'V</span></span>

<span data-ttu-id="7397c-121">적용할 두 번째 함수의 출력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7397c-121">The output type of the second function to be applied.</span></span>