---
uid: Microsoft.Quantum.Bitwise.Xor
title: Xor 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Xor
qsharp.summary: Returns the bitwise exclusive-OR (XOR) of two integers. This performs the same computation as the built-in `^^^` operator.
ms.openlocfilehash: ac31ba973ff06424dbd16168dac14a79b2691b3f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842075"
---
# <a name="xor-function"></a><span data-ttu-id="c3da3-102">Xor 함수</span><span class="sxs-lookup"><span data-stu-id="c3da3-102">Xor function</span></span>

<span data-ttu-id="c3da3-103">네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="c3da3-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="c3da3-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c3da3-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c3da3-105">두 정수의 배타적 비트 or (XOR)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3da3-105">Returns the bitwise exclusive-OR (XOR) of two integers.</span></span>
<span data-ttu-id="c3da3-106">이는 기본 제공 연산자와 동일한 계산을 수행 합니다 `^^^` .</span><span class="sxs-lookup"><span data-stu-id="c3da3-106">This performs the same computation as the built-in `^^^` operator.</span></span>

```qsharp
function Xor (a : Int, b : Int) : Int
```


## <a name="input"></a><span data-ttu-id="c3da3-107">입력</span><span class="sxs-lookup"><span data-stu-id="c3da3-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="c3da3-108">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c3da3-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="b--int"></a><span data-ttu-id="c3da3-109">b: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c3da3-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="c3da3-110">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c3da3-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="example"></a><span data-ttu-id="c3da3-111">예</span><span class="sxs-lookup"><span data-stu-id="c3da3-111">Example</span></span>

```qsharp
let a = 248;       //                 11111000₂
let b = 63;        //                 00111111₂
let x = Xor(a, b); // x : Int = 199 = 11000111₂.
```

## <a name="remarks"></a><span data-ttu-id="c3da3-112">설명</span><span class="sxs-lookup"><span data-stu-id="c3da3-112">Remarks</span></span>

<span data-ttu-id="c3da3-113">자세한 내용은 [c # ^ 연산자](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/xor-operator) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3da3-113">See the [C# ^ Operator](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/xor-operator) for more details.</span></span>