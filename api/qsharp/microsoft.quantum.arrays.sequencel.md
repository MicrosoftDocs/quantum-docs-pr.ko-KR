---
uid: Microsoft.Quantum.Arrays.SequenceL
title: SequenceL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5ce63575e703341fce42c0be393765c342bbd89
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718880"
---
# <a name="sequencel-function"></a><span data-ttu-id="9490a-102">SequenceL 함수</span><span class="sxs-lookup"><span data-stu-id="9490a-102">SequenceL function</span></span>

<span data-ttu-id="9490a-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9490a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9490a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9490a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9490a-105">지정 된 간격의 정수 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9490a-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a><span data-ttu-id="9490a-106">입력</span><span class="sxs-lookup"><span data-stu-id="9490a-106">Input</span></span>

### <a name="from--bigint"></a><span data-ttu-id="9490a-107">시작: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9490a-107">from : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9490a-108">간격의 포함 시작 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="9490a-108">An inclusive start index of the interval.</span></span>


### <a name="to--bigint"></a><span data-ttu-id="9490a-109">대상: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9490a-109">to : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9490a-110">보다 작은 간격의 포함 끝 인덱스입니다 `from` .</span><span class="sxs-lookup"><span data-stu-id="9490a-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="9490a-111">출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span><span class="sxs-lookup"><span data-stu-id="9490a-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span></span>

<span data-ttu-id="9490a-112">숫자 시퀀스 (, ...,)를 포함 하는 배열입니다. `from` `from + 1` `to`</span><span class="sxs-lookup"><span data-stu-id="9490a-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>

## <a name="remarks"></a><span data-ttu-id="9490a-113">설명</span><span class="sxs-lookup"><span data-stu-id="9490a-113">Remarks</span></span>

<span data-ttu-id="9490a-114">과 사이의 차이 `from` 는 `to` 값에 맞아야 합니다 `Int` .</span><span class="sxs-lookup"><span data-stu-id="9490a-114">The difference between `from` and `to` must fit into an `Int` value.</span></span>