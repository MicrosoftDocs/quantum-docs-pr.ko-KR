---
uid: Microsoft.Quantum.Math.DivRemL
title: DivRemL 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: DivRemL
qsharp.summary: Divides one BigInteger value by another, returns the result and the remainder as a tuple.
ms.openlocfilehash: 329f4d0bc21e74ab6c138af39c88cdcd964e63cf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857082"
---
# <a name="divreml-function"></a><span data-ttu-id="00276-102">DivRemL 함수</span><span class="sxs-lookup"><span data-stu-id="00276-102">DivRemL function</span></span>

<span data-ttu-id="00276-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="00276-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="00276-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="00276-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="00276-105">하나의 BigInteger 값을 다른 값으로 나누고 결과와 나머지를 튜플로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="00276-105">Divides one BigInteger value by another, returns the result and the remainder as a tuple.</span></span>

```qsharp
function DivRemL (dividend : BigInt, divisor : BigInt) : (BigInt, BigInt)
```


## <a name="input"></a><span data-ttu-id="00276-106">입력</span><span class="sxs-lookup"><span data-stu-id="00276-106">Input</span></span>

### <a name="dividend--bigint"></a><span data-ttu-id="00276-107">피제수: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="00276-107">dividend : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="divisor--bigint"></a><span data-ttu-id="00276-108">제 제: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="00276-108">divisor : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigintbigint"></a><span data-ttu-id="00276-109">출력: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="00276-109">Output : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>



## <a name="remarks"></a><span data-ttu-id="00276-110">설명</span><span class="sxs-lookup"><span data-stu-id="00276-110">Remarks</span></span>

<span data-ttu-id="00276-111">자세한 내용은 [BigInteger](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.divrem) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="00276-111">See [System.Numerics.BigInteger.DivRem](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.divrem) for more details.</span></span>