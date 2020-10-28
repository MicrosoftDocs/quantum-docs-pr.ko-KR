---
uid: Microsoft.Quantum.Canon.RepeatC
title: RepeatC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatC
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 8dc178374bdc9f8bf9f8aed57b9ae9a56995dec6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715555"
---
# <a name="repeatc-operation"></a><span data-ttu-id="c2fc3-102">RepeatC 작업</span><span class="sxs-lookup"><span data-stu-id="c2fc3-102">RepeatC operation</span></span>

<span data-ttu-id="c2fc3-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c2fc3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c2fc3-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c2fc3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c2fc3-105">지정 된 횟수 만큼 작업을 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatC<'TInput> (op : ('TInput => Unit is Ctl), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="c2fc3-106">입력</span><span class="sxs-lookup"><span data-stu-id="c2fc3-106">Input</span></span>

### <a name="op--tinput--unit-ctl"></a><span data-ttu-id="c2fc3-107">op: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="c2fc3-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="c2fc3-108">반복적으로 호출 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="c2fc3-109">nTimes: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c2fc3-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c2fc3-110">호출 하는 횟수 `op` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="c2fc3-111">입력: ' TInput</span><span class="sxs-lookup"><span data-stu-id="c2fc3-111">input : 'TInput</span></span>

<span data-ttu-id="c2fc3-112">에 전달 되는 입력 `op` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c2fc3-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c2fc3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c2fc3-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c2fc3-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="c2fc3-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="c2fc3-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="c2fc3-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c2fc3-116">See Also</span></span>

- [<span data-ttu-id="c2fc3-117">Microsoft 양자 Many</span><span class="sxs-lookup"><span data-stu-id="c2fc3-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="c2fc3-118">Microsoft. 양자 반복</span><span class="sxs-lookup"><span data-stu-id="c2fc3-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="c2fc3-119">RepeatA입니다.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-119">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="c2fc3-120">Microsoft 양자.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)