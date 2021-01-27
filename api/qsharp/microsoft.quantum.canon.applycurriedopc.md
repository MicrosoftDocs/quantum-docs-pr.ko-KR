---
uid: Microsoft.Quantum.Canon.ApplyCurriedOpC
title: ApplyCurriedOpC 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOpC
qsharp.summary: ''
ms.openlocfilehash: 65e861914b57cf8a32f2321f881248830b72c54e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841903"
---
# <a name="applycurriedopc-operation"></a><span data-ttu-id="54ee0-102">ApplyCurriedOpC 작업</span><span class="sxs-lookup"><span data-stu-id="54ee0-102">ApplyCurriedOpC operation</span></span>

<span data-ttu-id="54ee0-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="54ee0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="54ee0-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="54ee0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyCurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl)), first : 'T, second : 'U) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="54ee0-105">입력</span><span class="sxs-lookup"><span data-stu-id="54ee0-105">Input</span></span>

### <a name="curriedop--t---u--unit--is-ctl"></a><span data-ttu-id="54ee0-106">curriedOp: ' t > ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="54ee0-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="first--t"></a><span data-ttu-id="54ee0-107">첫 번째: ' t</span><span class="sxs-lookup"><span data-stu-id="54ee0-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="54ee0-108">second: ' U</span><span class="sxs-lookup"><span data-stu-id="54ee0-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="54ee0-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="54ee0-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="54ee0-110">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="54ee0-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="54ee0-111">없습니다</span><span class="sxs-lookup"><span data-stu-id="54ee0-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="54ee0-112">' U</span><span class="sxs-lookup"><span data-stu-id="54ee0-112">'U</span></span>

