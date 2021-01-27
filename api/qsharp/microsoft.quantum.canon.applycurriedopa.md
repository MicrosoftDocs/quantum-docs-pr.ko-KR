---
uid: Microsoft.Quantum.Canon.ApplyCurriedOpA
title: ApplyCurriedOpA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOpA
qsharp.summary: ''
ms.openlocfilehash: 100d8a42d6475d3cdda349a2e685a6fbfff23cdc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845081"
---
# <a name="applycurriedopa-operation"></a><span data-ttu-id="ce985-102">ApplyCurriedOpA 작업</span><span class="sxs-lookup"><span data-stu-id="ce985-102">ApplyCurriedOpA operation</span></span>

<span data-ttu-id="ce985-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ce985-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ce985-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ce985-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyCurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj)), first : 'T, second : 'U) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="ce985-105">입력</span><span class="sxs-lookup"><span data-stu-id="ce985-105">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj"></a><span data-ttu-id="ce985-106">curriedOp: ' t > ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="ce985-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="first--t"></a><span data-ttu-id="ce985-107">첫 번째: ' t</span><span class="sxs-lookup"><span data-stu-id="ce985-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="ce985-108">second: ' U</span><span class="sxs-lookup"><span data-stu-id="ce985-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="ce985-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ce985-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ce985-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ce985-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ce985-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="ce985-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="ce985-112">' U</span><span class="sxs-lookup"><span data-stu-id="ce985-112">'U</span></span>

