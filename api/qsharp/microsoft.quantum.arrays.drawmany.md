---
uid: Microsoft.Quantum.Arrays.DrawMany
title: DrawMany 연산
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: 3185f2ec01a2b9d01cff82a0c4667f12483801a7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209998"
---
# <a name="drawmany-operation"></a><span data-ttu-id="822cf-102">DrawMany 연산</span><span class="sxs-lookup"><span data-stu-id="822cf-102">DrawMany operation</span></span>

<span data-ttu-id="822cf-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="822cf-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="822cf-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="822cf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="822cf-105">지정 된 수의 샘플에 대해 작업을 반복 하 여 배열에서 해당 출력을 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="822cf-105">Repeats an operation for a given number of samples, collecting its outputs in an array.</span></span>

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a><span data-ttu-id="822cf-106">입력</span><span class="sxs-lookup"><span data-stu-id="822cf-106">Input</span></span>

### <a name="op--tinput--toutput"></a><span data-ttu-id="822cf-107">op: ' TInput => ' TOutput</span><span class="sxs-lookup"><span data-stu-id="822cf-107">op : 'TInput => 'TOutput</span></span> 

<span data-ttu-id="822cf-108">반복적으로 호출 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="822cf-108">The operation to be called repeatedly.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="822cf-109">nSamples: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="822cf-109">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="822cf-110">`op`을 (를) 수집 하기 위해 호출 하는 샘플의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="822cf-110">The number of samples of calling `op` to collect.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="822cf-111">입력: ' TInput</span><span class="sxs-lookup"><span data-stu-id="822cf-111">input : 'TInput</span></span>

<span data-ttu-id="822cf-112">에 전달 되는 입력 `op` 입니다.</span><span class="sxs-lookup"><span data-stu-id="822cf-112">The input to be passed to `op`.</span></span>



## <a name="output--toutput"></a><span data-ttu-id="822cf-113">출력: ' TOutput []</span><span class="sxs-lookup"><span data-stu-id="822cf-113">Output : 'TOutput[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="822cf-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="822cf-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="822cf-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="822cf-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="822cf-116">' TOutput</span><span class="sxs-lookup"><span data-stu-id="822cf-116">'TOutput</span></span>



## <a name="see-also"></a><span data-ttu-id="822cf-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="822cf-117">See Also</span></span>

- [<span data-ttu-id="822cf-118">Microsoft. 양자 반복</span><span class="sxs-lookup"><span data-stu-id="822cf-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)