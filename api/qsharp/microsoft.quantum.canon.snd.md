---
uid: Microsoft.Quantum.Canon.Snd
title: Snd 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Snd
qsharp.summary: Given a pair, returns its second element.
ms.openlocfilehash: c935a2bc9e3f5ab32669feae2bfc0f2ebf57e744
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205323"
---
# <a name="snd-function"></a><span data-ttu-id="9cf0d-102">Snd 함수</span><span class="sxs-lookup"><span data-stu-id="9cf0d-102">Snd function</span></span>

<span data-ttu-id="9cf0d-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9cf0d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9cf0d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9cf0d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9cf0d-105">쌍이 지정 된 경우 두 번째 요소를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf0d-105">Given a pair, returns its second element.</span></span>

```qsharp
function Snd<'T, 'U> (pair : ('T, 'U)) : 'U
```


## <a name="input"></a><span data-ttu-id="9cf0d-106">입력</span><span class="sxs-lookup"><span data-stu-id="9cf0d-106">Input</span></span>

### <a name="pair--tu"></a><span data-ttu-id="9cf0d-107">pair: (' t ', ' U)</span><span class="sxs-lookup"><span data-stu-id="9cf0d-107">pair : ('T,'U)</span></span>

<span data-ttu-id="9cf0d-108">두 개의 요소가 포함 된 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="9cf0d-108">A tuple with two elements.</span></span>



## <a name="output--u"></a><span data-ttu-id="9cf0d-109">출력: ' U</span><span class="sxs-lookup"><span data-stu-id="9cf0d-109">Output : 'U</span></span>

<span data-ttu-id="9cf0d-110">의 두 번째 요소 `pair` 입니다.</span><span class="sxs-lookup"><span data-stu-id="9cf0d-110">The second element of `pair`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9cf0d-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9cf0d-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9cf0d-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="9cf0d-112">'T</span></span>

<span data-ttu-id="9cf0d-113">쌍의 첫 번째 멤버의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9cf0d-113">The type of the pair's first member.</span></span>
### <a name="u"></a><span data-ttu-id="9cf0d-114">' U</span><span class="sxs-lookup"><span data-stu-id="9cf0d-114">'U</span></span>

<span data-ttu-id="9cf0d-115">쌍의 두 번째 멤버의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9cf0d-115">The type of the pair's second member.</span></span>