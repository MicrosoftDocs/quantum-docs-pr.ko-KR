---
uid: Microsoft.Quantum.Math.DivRemL
title: DivRemL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: DivRemL
qsharp.summary: Divides one BigInteger value by another, returns the result and the remainder as a tuple.
ms.openlocfilehash: d2ca91e0c3e8d69902234689359da7b73a8f7d1b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723742"
---
# <a name="divreml-function"></a><span data-ttu-id="a5739-102">DivRemL 함수</span><span class="sxs-lookup"><span data-stu-id="a5739-102">DivRemL function</span></span>

<span data-ttu-id="a5739-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="a5739-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="a5739-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a5739-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a5739-105">하나의 BigInteger 값을 다른 값으로 나누고 결과와 나머지를 튜플로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5739-105">Divides one BigInteger value by another, returns the result and the remainder as a tuple.</span></span>

```qsharp
function DivRemL (dividend : BigInt, divisor : BigInt) : (BigInt, BigInt)
```


## <a name="input"></a><span data-ttu-id="a5739-106">입력</span><span class="sxs-lookup"><span data-stu-id="a5739-106">Input</span></span>

### <a name="dividend--bigint"></a><span data-ttu-id="a5739-107">피제수: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a5739-107">dividend : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="divisor--bigint"></a><span data-ttu-id="a5739-108">제 제: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a5739-108">divisor : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigintbigint"></a><span data-ttu-id="a5739-109">출력: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="a5739-109">Output : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>



## <a name="remarks"></a><span data-ttu-id="a5739-110">설명</span><span class="sxs-lookup"><span data-stu-id="a5739-110">Remarks</span></span>

<span data-ttu-id="a5739-111">자세한 내용은 [BigInteger](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.divrem) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5739-111">See [System.Numerics.BigInteger.DivRem](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.divrem) for more details.</span></span>