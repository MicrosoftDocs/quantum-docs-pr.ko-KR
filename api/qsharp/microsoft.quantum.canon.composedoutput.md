---
uid: Microsoft.Quantum.Canon.ComposedOutput
title: ComposedOutput 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ComposedOutput
qsharp.summary: Returns the output of the composition of `inner` and `outer` for a given input.
ms.openlocfilehash: 7e361a62679ab93e9a0ebc04fa52be193805c78d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207465"
---
# <a name="composedoutput-function"></a><span data-ttu-id="99724-102">ComposedOutput 함수</span><span class="sxs-lookup"><span data-stu-id="99724-102">ComposedOutput function</span></span>

<span data-ttu-id="99724-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="99724-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="99724-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="99724-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="99724-105">`inner`지정 된 입력에 대해 및의 컴퍼지션 출력을 반환 합니다 `outer` .</span><span class="sxs-lookup"><span data-stu-id="99724-105">Returns the output of the composition of `inner` and `outer` for a given input.</span></span>

```qsharp
function ComposedOutput<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U), target : 'T) : 'V
```


## <a name="input"></a><span data-ttu-id="99724-106">입력</span><span class="sxs-lookup"><span data-stu-id="99724-106">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="99724-107">외부: ' U-> ' V</span><span class="sxs-lookup"><span data-stu-id="99724-107">outer : 'U -> 'V</span></span>




### <a name="inner--t---u"></a><span data-ttu-id="99724-108">inner: ' t-> ' U</span><span class="sxs-lookup"><span data-stu-id="99724-108">inner : 'T -> 'U</span></span>




### <a name="target--t"></a><span data-ttu-id="99724-109">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="99724-109">target : 'T</span></span>





## <a name="output--v"></a><span data-ttu-id="99724-110">출력: ' V</span><span class="sxs-lookup"><span data-stu-id="99724-110">Output : 'V</span></span>



## <a name="type-parameters"></a><span data-ttu-id="99724-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="99724-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="99724-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="99724-112">'T</span></span>


### <a name="u"></a><span data-ttu-id="99724-113">' U</span><span class="sxs-lookup"><span data-stu-id="99724-113">'U</span></span>


### <a name="v"></a><span data-ttu-id="99724-114">' V</span><span class="sxs-lookup"><span data-stu-id="99724-114">'V</span></span>

