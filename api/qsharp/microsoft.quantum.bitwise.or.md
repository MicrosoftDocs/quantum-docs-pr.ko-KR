---
uid: Microsoft.Quantum.Bitwise.Or
title: Or 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Or
qsharp.summary: Returns the bitwise OR of two integers. This performs the same computation as the built-in `|||` operator.
ms.openlocfilehash: 811e7cf64424e8302c5745c4c71d76de50ab8c08
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845275"
---
# <a name="or-function"></a><span data-ttu-id="39b60-102">Or 함수</span><span class="sxs-lookup"><span data-stu-id="39b60-102">Or function</span></span>

<span data-ttu-id="39b60-103">네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="39b60-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="39b60-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="39b60-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="39b60-105">두 정수의 비트 OR을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="39b60-105">Returns the bitwise OR of two integers.</span></span>
<span data-ttu-id="39b60-106">이는 기본 제공 연산자와 동일한 계산을 수행 합니다 `|||` .</span><span class="sxs-lookup"><span data-stu-id="39b60-106">This performs the same computation as the built-in `|||` operator.</span></span>

```qsharp
function Or (a : Int, b : Int) : Int
```


## <a name="input"></a><span data-ttu-id="39b60-107">입력</span><span class="sxs-lookup"><span data-stu-id="39b60-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="39b60-108">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="39b60-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="b--int"></a><span data-ttu-id="39b60-109">b: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="39b60-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="39b60-110">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="39b60-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="example"></a><span data-ttu-id="39b60-111">예</span><span class="sxs-lookup"><span data-stu-id="39b60-111">Example</span></span>

```qsharp
let a = 248;      //                 11111000₂
let b = 63;       //                 00111111₂
let x = Or(a, b); // x : Int = 255 = 11111111₂.
```

## <a name="remarks"></a><span data-ttu-id="39b60-112">설명</span><span class="sxs-lookup"><span data-stu-id="39b60-112">Remarks</span></span>

<span data-ttu-id="39b60-113">[C # | 참조 추가 정보를 확인](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/or-operator) 합니다.</span><span class="sxs-lookup"><span data-stu-id="39b60-113">See the [C# | Operator](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/or-operator) for more details.</span></span>