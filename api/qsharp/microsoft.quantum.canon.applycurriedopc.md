---
uid: Microsoft.Quantum.Canon.ApplyCurriedOpC
title: ApplyCurriedOpC 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOpC
qsharp.summary: ''
ms.openlocfilehash: faca9b3f6d9a132b591a532c9e2ce54af1f0b182
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218940"
---
# <a name="applycurriedopc-operation"></a><span data-ttu-id="e2746-102">ApplyCurriedOpC 작업</span><span class="sxs-lookup"><span data-stu-id="e2746-102">ApplyCurriedOpC operation</span></span>

<span data-ttu-id="e2746-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e2746-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e2746-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e2746-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyCurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl)), first : 'T, second : 'U) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="e2746-105">입력</span><span class="sxs-lookup"><span data-stu-id="e2746-105">Input</span></span>

### <a name="curriedop--t---u--unit--is-ctl"></a><span data-ttu-id="e2746-106">curriedOp: ' t > ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="e2746-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="first--t"></a><span data-ttu-id="e2746-107">첫 번째: ' t</span><span class="sxs-lookup"><span data-stu-id="e2746-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="e2746-108">second: ' U</span><span class="sxs-lookup"><span data-stu-id="e2746-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="e2746-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e2746-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e2746-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e2746-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e2746-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="e2746-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="e2746-112">' U</span><span class="sxs-lookup"><span data-stu-id="e2746-112">'U</span></span>

