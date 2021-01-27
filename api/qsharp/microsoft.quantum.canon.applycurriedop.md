---
uid: Microsoft.Quantum.Canon.ApplyCurriedOp
title: ApplyCurriedOp 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOp
qsharp.summary: ''
ms.openlocfilehash: c252eceb6a307ea9514aaa8aa3a3de1f9fa1b698
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841926"
---
# <a name="applycurriedop-operation"></a><span data-ttu-id="734ef-102">ApplyCurriedOp 작업</span><span class="sxs-lookup"><span data-stu-id="734ef-102">ApplyCurriedOp operation</span></span>

<span data-ttu-id="734ef-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="734ef-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="734ef-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="734ef-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyCurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit)), first : 'T, second : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="734ef-105">입력</span><span class="sxs-lookup"><span data-stu-id="734ef-105">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="734ef-106">curriedOp: ' t-> ' U => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="734ef-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="first--t"></a><span data-ttu-id="734ef-107">첫 번째: ' t</span><span class="sxs-lookup"><span data-stu-id="734ef-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="734ef-108">second: ' U</span><span class="sxs-lookup"><span data-stu-id="734ef-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="734ef-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="734ef-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="734ef-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="734ef-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="734ef-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="734ef-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="734ef-112">' U</span><span class="sxs-lookup"><span data-stu-id="734ef-112">'U</span></span>

