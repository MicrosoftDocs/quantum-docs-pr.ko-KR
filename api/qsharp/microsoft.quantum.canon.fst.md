---
uid: Microsoft.Quantum.Canon.Fst
title: Fst 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: cd5746358c8323f8d2dbca44965fa5dbac0a84c1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840510"
---
# <a name="fst-function"></a><span data-ttu-id="7cf5f-102">Fst 함수</span><span class="sxs-lookup"><span data-stu-id="7cf5f-102">Fst function</span></span>

<span data-ttu-id="7cf5f-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7cf5f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7cf5f-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7cf5f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7cf5f-105">쌍이 지정 된 경우 첫 번째 요소를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cf5f-105">Given a pair, returns its first element.</span></span>

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a><span data-ttu-id="7cf5f-106">입력</span><span class="sxs-lookup"><span data-stu-id="7cf5f-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="7cf5f-107">pair: (' t ', ' U)</span><span class="sxs-lookup"><span data-stu-id="7cf5f-107">pair : ('T,'U)</span></span>

<span data-ttu-id="7cf5f-108">두 개의 요소가 포함 된 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="7cf5f-108">A tuple with two elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="7cf5f-109">출력: ' '</span><span class="sxs-lookup"><span data-stu-id="7cf5f-109">Output : 'T</span></span>

<span data-ttu-id="7cf5f-110">`pair`의 첫 번째 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="7cf5f-110">The first element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7cf5f-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7cf5f-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7cf5f-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="7cf5f-112">'T</span></span>

<span data-ttu-id="7cf5f-113">쌍의 첫 번째 멤버의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7cf5f-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="7cf5f-114">' U</span><span class="sxs-lookup"><span data-stu-id="7cf5f-114">'U</span></span>

<span data-ttu-id="7cf5f-115">쌍의 두 번째 멤버의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7cf5f-115">The type of the pair's second member.</span></span>