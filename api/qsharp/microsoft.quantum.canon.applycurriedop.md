---
uid: Microsoft.Quantum.Canon.ApplyCurriedOp
title: ApplyCurriedOp 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOp
qsharp.summary: ''
ms.openlocfilehash: ab652159fa64a95401d07998ed4aaae5c4dbb92e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219025"
---
# <a name="applycurriedop-operation"></a><span data-ttu-id="9480f-102">ApplyCurriedOp 작업</span><span class="sxs-lookup"><span data-stu-id="9480f-102">ApplyCurriedOp operation</span></span>

<span data-ttu-id="9480f-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9480f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9480f-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9480f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyCurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit)), first : 'T, second : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="9480f-105">입력</span><span class="sxs-lookup"><span data-stu-id="9480f-105">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="9480f-106">curriedOp: ' t-> ' U => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9480f-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="first--t"></a><span data-ttu-id="9480f-107">첫 번째: ' t</span><span class="sxs-lookup"><span data-stu-id="9480f-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="9480f-108">second: ' U</span><span class="sxs-lookup"><span data-stu-id="9480f-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="9480f-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9480f-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9480f-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9480f-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9480f-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="9480f-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="9480f-112">' U</span><span class="sxs-lookup"><span data-stu-id="9480f-112">'U</span></span>

