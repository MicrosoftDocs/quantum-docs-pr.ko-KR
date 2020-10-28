---
uid: Microsoft.Quantum.Canon.ComposedOutput
title: ComposedOutput 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ComposedOutput
qsharp.summary: Returns the output of the composition of `inner` and `outer` for a given input.
ms.openlocfilehash: 4da66616692055a7d60abbf1fac6e6799806675d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716486"
---
# <a name="composedoutput-function"></a><span data-ttu-id="25225-102">ComposedOutput 함수</span><span class="sxs-lookup"><span data-stu-id="25225-102">ComposedOutput function</span></span>

<span data-ttu-id="25225-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="25225-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="25225-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="25225-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="25225-105">`inner`지정 된 입력에 대해 및의 컴퍼지션 출력을 반환 합니다 `outer` .</span><span class="sxs-lookup"><span data-stu-id="25225-105">Returns the output of the composition of `inner` and `outer` for a given input.</span></span>

```qsharp
function ComposedOutput<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U), target : 'T) : 'V
```


## <a name="input"></a><span data-ttu-id="25225-106">입력</span><span class="sxs-lookup"><span data-stu-id="25225-106">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="25225-107">외부: ' U-> ' V</span><span class="sxs-lookup"><span data-stu-id="25225-107">outer : 'U -> 'V</span></span>




### <a name="inner--t---u"></a><span data-ttu-id="25225-108">inner: ' t-> ' U</span><span class="sxs-lookup"><span data-stu-id="25225-108">inner : 'T -> 'U</span></span>




### <a name="target--t"></a><span data-ttu-id="25225-109">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="25225-109">target : 'T</span></span>





## <a name="output--v"></a><span data-ttu-id="25225-110">출력: ' V</span><span class="sxs-lookup"><span data-stu-id="25225-110">Output : 'V</span></span>



## <a name="type-parameters"></a><span data-ttu-id="25225-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="25225-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="25225-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="25225-112">'T</span></span>


### <a name="u"></a><span data-ttu-id="25225-113">' U</span><span class="sxs-lookup"><span data-stu-id="25225-113">'U</span></span>


### <a name="v"></a><span data-ttu-id="25225-114">' V</span><span class="sxs-lookup"><span data-stu-id="25225-114">'V</span></span>

