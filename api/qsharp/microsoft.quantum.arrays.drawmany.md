---
uid: Microsoft.Quantum.Arrays.DrawMany
title: DrawMany 연산
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: bf63ce308679cef97c776d3383ff732ed4d4e500
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846215"
---
# <a name="drawmany-operation"></a><span data-ttu-id="a20b4-102">DrawMany 연산</span><span class="sxs-lookup"><span data-stu-id="a20b4-102">DrawMany operation</span></span>

<span data-ttu-id="a20b4-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a20b4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a20b4-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a20b4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a20b4-105">지정 된 수의 샘플에 대해 작업을 반복 하 여 배열에서 해당 출력을 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="a20b4-105">Repeats an operation for a given number of samples, collecting its outputs in an array.</span></span>

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a><span data-ttu-id="a20b4-106">입력</span><span class="sxs-lookup"><span data-stu-id="a20b4-106">Input</span></span>

### <a name="op--tinput--toutput"></a><span data-ttu-id="a20b4-107">op: ' TInput => ' TOutput</span><span class="sxs-lookup"><span data-stu-id="a20b4-107">op : 'TInput => 'TOutput</span></span> 

<span data-ttu-id="a20b4-108">반복적으로 호출 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a20b4-108">The operation to be called repeatedly.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="a20b4-109">nSamples: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a20b4-109">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a20b4-110">`op`을 (를) 수집 하기 위해 호출 하는 샘플의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a20b4-110">The number of samples of calling `op` to collect.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="a20b4-111">입력: ' TInput</span><span class="sxs-lookup"><span data-stu-id="a20b4-111">input : 'TInput</span></span>

<span data-ttu-id="a20b4-112">에 전달 되는 입력 `op` 입니다.</span><span class="sxs-lookup"><span data-stu-id="a20b4-112">The input to be passed to `op`.</span></span>



## <a name="output--toutput"></a><span data-ttu-id="a20b4-113">출력: ' TOutput []</span><span class="sxs-lookup"><span data-stu-id="a20b4-113">Output : 'TOutput[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a20b4-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a20b4-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="a20b4-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="a20b4-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="a20b4-116">' TOutput</span><span class="sxs-lookup"><span data-stu-id="a20b4-116">'TOutput</span></span>



## <a name="example"></a><span data-ttu-id="a20b4-117">예</span><span class="sxs-lookup"><span data-stu-id="a20b4-117">Example</span></span>

<span data-ttu-id="a20b4-118">다음은 한 번에 단일 비트를 샘플링 하는 연산이 주어진 경우 정수를 샘플링 합니다.</span><span class="sxs-lookup"><span data-stu-id="a20b4-118">The following samples an integer, given an operation that samples a single bit at a time.</span></span>

```qsharp
let randomInteger = BoolArrayAsInt(DrawMany(SampleRandomBit, 16, ()));
```

## <a name="see-also"></a><span data-ttu-id="a20b4-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a20b4-119">See Also</span></span>

- [<span data-ttu-id="a20b4-120">Microsoft. 양자 반복</span><span class="sxs-lookup"><span data-stu-id="a20b4-120">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)