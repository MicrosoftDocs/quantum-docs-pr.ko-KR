---
uid: Microsoft.Quantum.Arrays.SequenceI
title: SequenceI 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5dc4377c696e14b505c63701c2f5ca0dadca672
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718897"
---
# <a name="sequencei-function"></a><span data-ttu-id="12612-102">SequenceI 함수</span><span class="sxs-lookup"><span data-stu-id="12612-102">SequenceI function</span></span>

<span data-ttu-id="12612-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="12612-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="12612-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="12612-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="12612-105">지정 된 간격의 정수 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12612-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceI (from : Int, to : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="12612-106">입력</span><span class="sxs-lookup"><span data-stu-id="12612-106">Input</span></span>

### <a name="from--int"></a><span data-ttu-id="12612-107">시작: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="12612-107">from : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="12612-108">간격의 포함 시작 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="12612-108">An inclusive start index of the interval.</span></span>


### <a name="to--int"></a><span data-ttu-id="12612-109">대상: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="12612-109">to : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="12612-110">보다 작은 간격의 포함 끝 인덱스입니다 `from` .</span><span class="sxs-lookup"><span data-stu-id="12612-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--int"></a><span data-ttu-id="12612-111">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="12612-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="12612-112">숫자 시퀀스 (, ...,)를 포함 하는 배열입니다. `from` `from + 1` `to`</span><span class="sxs-lookup"><span data-stu-id="12612-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>