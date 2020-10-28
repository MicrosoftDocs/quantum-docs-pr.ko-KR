---
uid: Microsoft.Quantum.Canon.ApplyCurriedOp
title: ApplyCurriedOp 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOp
qsharp.summary: ''
ms.openlocfilehash: 22e2ace51175ed9df1c70bf75ce2b497f8449020
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718340"
---
# <a name="applycurriedop-operation"></a><span data-ttu-id="8b844-102">ApplyCurriedOp 작업</span><span class="sxs-lookup"><span data-stu-id="8b844-102">ApplyCurriedOp operation</span></span>

<span data-ttu-id="8b844-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8b844-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8b844-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8b844-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyCurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit)), first : 'T, second : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="8b844-105">입력</span><span class="sxs-lookup"><span data-stu-id="8b844-105">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="8b844-106">curriedOp: ' t-> ' U => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8b844-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="first--t"></a><span data-ttu-id="8b844-107">첫 번째: ' t</span><span class="sxs-lookup"><span data-stu-id="8b844-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="8b844-108">second: ' U</span><span class="sxs-lookup"><span data-stu-id="8b844-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="8b844-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8b844-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8b844-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8b844-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8b844-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="8b844-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="8b844-112">' U</span><span class="sxs-lookup"><span data-stu-id="8b844-112">'U</span></span>

