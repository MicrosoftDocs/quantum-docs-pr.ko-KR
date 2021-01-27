---
uid: Microsoft.Quantum.Arrays.SequenceL
title: SequenceL 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 7e3c5c31428f9be152e28afbe478a3d15eb0a56c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850979"
---
# <a name="sequencel-function"></a><span data-ttu-id="75603-102">SequenceL 함수</span><span class="sxs-lookup"><span data-stu-id="75603-102">SequenceL function</span></span>

<span data-ttu-id="75603-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="75603-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="75603-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="75603-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="75603-105">지정 된 간격의 정수 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75603-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a><span data-ttu-id="75603-106">입력</span><span class="sxs-lookup"><span data-stu-id="75603-106">Input</span></span>

### <a name="from--bigint"></a><span data-ttu-id="75603-107">시작: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="75603-107">from : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="75603-108">간격의 포함 시작 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="75603-108">An inclusive start index of the interval.</span></span>


### <a name="to--bigint"></a><span data-ttu-id="75603-109">대상: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="75603-109">to : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="75603-110">보다 작은 간격의 포함 끝 인덱스입니다 `from` .</span><span class="sxs-lookup"><span data-stu-id="75603-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="75603-111">출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span><span class="sxs-lookup"><span data-stu-id="75603-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span></span>

<span data-ttu-id="75603-112">숫자 시퀀스 (, ...,)를 포함 하는 배열입니다. `from` `from + 1` `to`</span><span class="sxs-lookup"><span data-stu-id="75603-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>

## <a name="example"></a><span data-ttu-id="75603-113">예</span><span class="sxs-lookup"><span data-stu-id="75603-113">Example</span></span>

```qsharp
let arr1 = SequenceL(0L, 3L); // [0L, 1L, 2L, 3L]
let arr2 = SequenceL(23L, 29L); // [23L, 24L, 25L, 26L, 27L, 28L, 29L]
let arr3 = SequenceL(-5L, -2L); // [-5L, -4L, -3L, -2L]
```

## <a name="remarks"></a><span data-ttu-id="75603-114">설명</span><span class="sxs-lookup"><span data-stu-id="75603-114">Remarks</span></span>

<span data-ttu-id="75603-115">과 사이의 차이 `from` 는 `to` 값에 맞아야 합니다 `Int` .</span><span class="sxs-lookup"><span data-stu-id="75603-115">The difference between `from` and `to` must fit into an `Int` value.</span></span>