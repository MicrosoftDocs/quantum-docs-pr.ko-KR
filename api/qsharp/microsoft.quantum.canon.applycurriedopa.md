---
uid: Microsoft.Quantum.Canon.ApplyCurriedOpA
title: ApplyCurriedOpA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOpA
qsharp.summary: ''
ms.openlocfilehash: db3f63cbe2ee5ef048c7e378864d68696f55331f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218957"
---
# <a name="applycurriedopa-operation"></a><span data-ttu-id="6f393-102">ApplyCurriedOpA 작업</span><span class="sxs-lookup"><span data-stu-id="6f393-102">ApplyCurriedOpA operation</span></span>

<span data-ttu-id="6f393-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6f393-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6f393-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6f393-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyCurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj)), first : 'T, second : 'U) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="6f393-105">입력</span><span class="sxs-lookup"><span data-stu-id="6f393-105">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj"></a><span data-ttu-id="6f393-106">curriedOp: ' t > ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="6f393-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="first--t"></a><span data-ttu-id="6f393-107">첫 번째: ' t</span><span class="sxs-lookup"><span data-stu-id="6f393-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="6f393-108">second: ' U</span><span class="sxs-lookup"><span data-stu-id="6f393-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="6f393-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6f393-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6f393-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6f393-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6f393-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="6f393-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="6f393-112">' U</span><span class="sxs-lookup"><span data-stu-id="6f393-112">'U</span></span>

