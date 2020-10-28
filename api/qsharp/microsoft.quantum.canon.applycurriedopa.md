---
uid: Microsoft.Quantum.Canon.ApplyCurriedOpA
title: ApplyCurriedOpA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOpA
qsharp.summary: ''
ms.openlocfilehash: 2b0f86efe79654e1f886f0ccd0287e07225cbf83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718333"
---
# <a name="applycurriedopa-operation"></a><span data-ttu-id="2a56d-102">ApplyCurriedOpA 작업</span><span class="sxs-lookup"><span data-stu-id="2a56d-102">ApplyCurriedOpA operation</span></span>

<span data-ttu-id="2a56d-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2a56d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2a56d-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2a56d-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyCurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj)), first : 'T, second : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="2a56d-105">입력</span><span class="sxs-lookup"><span data-stu-id="2a56d-105">Input</span></span>

### <a name="curriedop--t---u--unit-adj"></a><span data-ttu-id="2a56d-106">curriedOp: ' t-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="2a56d-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>




### <a name="first--t"></a><span data-ttu-id="2a56d-107">첫 번째: ' t</span><span class="sxs-lookup"><span data-stu-id="2a56d-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="2a56d-108">second: ' U</span><span class="sxs-lookup"><span data-stu-id="2a56d-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="2a56d-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2a56d-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2a56d-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2a56d-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2a56d-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="2a56d-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="2a56d-112">' U</span><span class="sxs-lookup"><span data-stu-id="2a56d-112">'U</span></span>

