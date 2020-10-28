---
uid: Microsoft.Quantum.Canon.ApplyCurriedOpC
title: ApplyCurriedOpC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOpC
qsharp.summary: ''
ms.openlocfilehash: 1a00fe91889e3100e4d3272d258877b4ec88618f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718321"
---
# <a name="applycurriedopc-operation"></a><span data-ttu-id="97ff2-102">ApplyCurriedOpC 작업</span><span class="sxs-lookup"><span data-stu-id="97ff2-102">ApplyCurriedOpC operation</span></span>

<span data-ttu-id="97ff2-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="97ff2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="97ff2-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="97ff2-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyCurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl)), first : 'T, second : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="97ff2-105">입력</span><span class="sxs-lookup"><span data-stu-id="97ff2-105">Input</span></span>

### <a name="curriedop--t---u--unit-ctl"></a><span data-ttu-id="97ff2-106">curriedOp: ' t-> ' U => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="97ff2-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>




### <a name="first--t"></a><span data-ttu-id="97ff2-107">첫 번째: ' t</span><span class="sxs-lookup"><span data-stu-id="97ff2-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="97ff2-108">second: ' U</span><span class="sxs-lookup"><span data-stu-id="97ff2-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="97ff2-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="97ff2-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="97ff2-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="97ff2-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="97ff2-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="97ff2-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="97ff2-112">' U</span><span class="sxs-lookup"><span data-stu-id="97ff2-112">'U</span></span>

