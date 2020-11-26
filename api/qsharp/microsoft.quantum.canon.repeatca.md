---
uid: Microsoft.Quantum.Canon.RepeatCA
title: RepeatCA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 24606486b3d5703065a7c7f62d3bbc7e3d07615f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205408"
---
# <a name="repeatca-operation"></a><span data-ttu-id="2ae59-102">RepeatCA 작업</span><span class="sxs-lookup"><span data-stu-id="2ae59-102">RepeatCA operation</span></span>

<span data-ttu-id="2ae59-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2ae59-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2ae59-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2ae59-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2ae59-105">지정 된 횟수 만큼 작업을 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ae59-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="2ae59-106">입력</span><span class="sxs-lookup"><span data-stu-id="2ae59-106">Input</span></span>

### <a name="op--tinput--unit--is-adj--ctl"></a><span data-ttu-id="2ae59-107">op: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="2ae59-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="2ae59-108">반복적으로 호출 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="2ae59-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="2ae59-109">nTimes: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2ae59-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2ae59-110">호출 하는 횟수 `op` 입니다.</span><span class="sxs-lookup"><span data-stu-id="2ae59-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="2ae59-111">입력: ' TInput</span><span class="sxs-lookup"><span data-stu-id="2ae59-111">input : 'TInput</span></span>

<span data-ttu-id="2ae59-112">에 전달 되는 입력 `op` 입니다.</span><span class="sxs-lookup"><span data-stu-id="2ae59-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2ae59-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2ae59-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2ae59-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2ae59-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="2ae59-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="2ae59-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="2ae59-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2ae59-116">See Also</span></span>

- [<span data-ttu-id="2ae59-117">Microsoft 양자 Many</span><span class="sxs-lookup"><span data-stu-id="2ae59-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="2ae59-118">Microsoft. 양자 반복</span><span class="sxs-lookup"><span data-stu-id="2ae59-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="2ae59-119">RepeatA입니다.</span><span class="sxs-lookup"><span data-stu-id="2ae59-119">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="2ae59-120">Microsoft 양자.</span><span class="sxs-lookup"><span data-stu-id="2ae59-120">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)