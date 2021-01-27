---
uid: Microsoft.Quantum.Arrays.SequenceI
title: SequenceI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 3cf09e48cce1aeb1aac837465ee3a5e06adf5169
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851001"
---
# <a name="sequencei-function"></a><span data-ttu-id="e7c3d-102">SequenceI 함수</span><span class="sxs-lookup"><span data-stu-id="e7c3d-102">SequenceI function</span></span>

<span data-ttu-id="e7c3d-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e7c3d-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e7c3d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e7c3d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e7c3d-105">지정 된 간격의 정수 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7c3d-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceI (from : Int, to : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="e7c3d-106">입력</span><span class="sxs-lookup"><span data-stu-id="e7c3d-106">Input</span></span>

### <a name="from--int"></a><span data-ttu-id="e7c3d-107">시작: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e7c3d-107">from : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e7c3d-108">간격의 포함 시작 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c3d-108">An inclusive start index of the interval.</span></span>


### <a name="to--int"></a><span data-ttu-id="e7c3d-109">대상: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e7c3d-109">to : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e7c3d-110">보다 작은 간격의 포함 끝 인덱스입니다 `from` .</span><span class="sxs-lookup"><span data-stu-id="e7c3d-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--int"></a><span data-ttu-id="e7c3d-111">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="e7c3d-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="e7c3d-112">숫자 시퀀스 (, ...,)를 포함 하는 배열입니다. `from` `from + 1` `to`</span><span class="sxs-lookup"><span data-stu-id="e7c3d-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>

## <a name="example"></a><span data-ttu-id="e7c3d-113">예제</span><span class="sxs-lookup"><span data-stu-id="e7c3d-113">Example</span></span>

```qsharp
let arr1 = SequenceI(0, 3); // [0, 1, 2, 3]
let arr2 = SequenceI(23, 29); // [23, 24, 25, 26, 27, 28, 29]
let arr3 = SequenceI(-5, -2); // [-5, -4, -3, -2]

let numbers = SequenceI(0, _); // function to create sequence from 0 to `to`
let naturals = SequenceI(1, _); // function to create sequence from 1 to `to`
```