---
uid: Microsoft.Quantum.Canon.ComposedOutput
title: ComposedOutput 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ComposedOutput
qsharp.summary: Returns the output of the composition of `inner` and `outer` for a given input.
ms.openlocfilehash: d39fcd6b2987b3a4f69df13fa83b69a199d6eddb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840882"
---
# <a name="composedoutput-function"></a><span data-ttu-id="76ed3-102">ComposedOutput 함수</span><span class="sxs-lookup"><span data-stu-id="76ed3-102">ComposedOutput function</span></span>

<span data-ttu-id="76ed3-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="76ed3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="76ed3-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="76ed3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="76ed3-105">`inner`지정 된 입력에 대해 및의 컴퍼지션 출력을 반환 합니다 `outer` .</span><span class="sxs-lookup"><span data-stu-id="76ed3-105">Returns the output of the composition of `inner` and `outer` for a given input.</span></span>

```qsharp
function ComposedOutput<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U), target : 'T) : 'V
```


## <a name="input"></a><span data-ttu-id="76ed3-106">입력</span><span class="sxs-lookup"><span data-stu-id="76ed3-106">Input</span></span>

### <a name="outer--u---v"></a><span data-ttu-id="76ed3-107">외부: ' U-> ' V</span><span class="sxs-lookup"><span data-stu-id="76ed3-107">outer : 'U -> 'V</span></span>




### <a name="inner--t---u"></a><span data-ttu-id="76ed3-108">inner: ' t-> ' U</span><span class="sxs-lookup"><span data-stu-id="76ed3-108">inner : 'T -> 'U</span></span>




### <a name="target--t"></a><span data-ttu-id="76ed3-109">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="76ed3-109">target : 'T</span></span>





## <a name="output--v"></a><span data-ttu-id="76ed3-110">출력: ' V</span><span class="sxs-lookup"><span data-stu-id="76ed3-110">Output : 'V</span></span>



## <a name="type-parameters"></a><span data-ttu-id="76ed3-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="76ed3-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="76ed3-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="76ed3-112">'T</span></span>


### <a name="u"></a><span data-ttu-id="76ed3-113">' U</span><span class="sxs-lookup"><span data-stu-id="76ed3-113">'U</span></span>


### <a name="v"></a><span data-ttu-id="76ed3-114">' V</span><span class="sxs-lookup"><span data-stu-id="76ed3-114">'V</span></span>

