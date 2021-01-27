---
uid: Microsoft.Quantum.Canon.Compose
title: 작성 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 73eab66e2e9a9af56d01db927eb7af38bb56a23e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840900"
---
# <a name="compose-function"></a><span data-ttu-id="8bcee-102">작성 함수</span><span class="sxs-lookup"><span data-stu-id="8bcee-102">Compose function</span></span>

<span data-ttu-id="8bcee-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8bcee-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8bcee-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8bcee-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8bcee-105">두 함수의 컴퍼지션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcee-105">Returns the composition of two functions.</span></span>

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a><span data-ttu-id="8bcee-106">설명</span><span class="sxs-lookup"><span data-stu-id="8bcee-106">Description</span></span>

<span data-ttu-id="8bcee-107">$ 및 $g $ $f 두 개의 함수가 지정 된 경우 $f \circ g $를 나타내는 새 함수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcee-107">Given two functions $f$ and $g$, returns a new function representing $f \circ g$.</span></span>

## <a name="input"></a><span data-ttu-id="8bcee-108">입력</span><span class="sxs-lookup"><span data-stu-id="8bcee-108">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="8bcee-109">외부: ' U-> ' V</span><span class="sxs-lookup"><span data-stu-id="8bcee-109">outer : 'U -> 'V</span></span>

<span data-ttu-id="8bcee-110">적용할 두 번째 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="8bcee-110">The second function to be applied.</span></span>


### <a name="inner--t---u"></a><span data-ttu-id="8bcee-111">inner: ' t-> ' U</span><span class="sxs-lookup"><span data-stu-id="8bcee-111">inner : 'T -> 'U</span></span>

<span data-ttu-id="8bcee-112">적용할 첫 번째 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="8bcee-112">The first function to be applied.</span></span>



## <a name="output--t---v"></a><span data-ttu-id="8bcee-113">출력: ' t ' > ' V</span><span class="sxs-lookup"><span data-stu-id="8bcee-113">Output : 'T -> 'V</span></span>

<span data-ttu-id="8bcee-114">$, $F (g (x)) = h (x) $ $x 모든 입력에 대 한 새 함수는 $를 $h 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcee-114">A new function $h$ such that for all inputs $x$, $f(g(x)) = h(x)$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8bcee-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8bcee-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8bcee-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="8bcee-116">'T</span></span>

<span data-ttu-id="8bcee-117">적용할 첫 번째 함수의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8bcee-117">The input type of the first function to be applied.</span></span>
### <a name="u"></a><span data-ttu-id="8bcee-118">' U</span><span class="sxs-lookup"><span data-stu-id="8bcee-118">'U</span></span>

<span data-ttu-id="8bcee-119">적용할 첫 번째 함수의 출력 형식과 적용할 두 번째 함수의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8bcee-119">The output type of the first function to be applied and the input type of the second function to be applied.</span></span>
### <a name="v"></a><span data-ttu-id="8bcee-120">' V</span><span class="sxs-lookup"><span data-stu-id="8bcee-120">'V</span></span>

<span data-ttu-id="8bcee-121">적용할 두 번째 함수의 출력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8bcee-121">The output type of the second function to be applied.</span></span>