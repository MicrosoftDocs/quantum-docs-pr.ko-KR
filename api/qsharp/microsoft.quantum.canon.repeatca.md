---
uid: Microsoft.Quantum.Canon.RepeatCA
title: RepeatCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: b68c3aa4298fffa76f7c43ac4c6d27cdf3b72fbf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715548"
---
# <a name="repeatca-operation"></a><span data-ttu-id="6639f-102">RepeatCA 작업</span><span class="sxs-lookup"><span data-stu-id="6639f-102">RepeatCA operation</span></span>

<span data-ttu-id="6639f-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6639f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6639f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6639f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6639f-105">지정 된 횟수 만큼 작업을 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="6639f-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="6639f-106">입력</span><span class="sxs-lookup"><span data-stu-id="6639f-106">Input</span></span>

### <a name="op--tinput--unit-adj--ctl"></a><span data-ttu-id="6639f-107">op: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="6639f-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="6639f-108">반복적으로 호출 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="6639f-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="6639f-109">nTimes: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6639f-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6639f-110">호출 하는 횟수 `op` 입니다.</span><span class="sxs-lookup"><span data-stu-id="6639f-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="6639f-111">입력: ' TInput</span><span class="sxs-lookup"><span data-stu-id="6639f-111">input : 'TInput</span></span>

<span data-ttu-id="6639f-112">에 전달 되는 입력 `op` 입니다.</span><span class="sxs-lookup"><span data-stu-id="6639f-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6639f-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6639f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6639f-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6639f-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="6639f-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="6639f-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="6639f-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6639f-116">See Also</span></span>

- [<span data-ttu-id="6639f-117">Microsoft 양자 Many</span><span class="sxs-lookup"><span data-stu-id="6639f-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="6639f-118">Microsoft. 양자 반복</span><span class="sxs-lookup"><span data-stu-id="6639f-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="6639f-119">RepeatA입니다.</span><span class="sxs-lookup"><span data-stu-id="6639f-119">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="6639f-120">Microsoft 양자.</span><span class="sxs-lookup"><span data-stu-id="6639f-120">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)