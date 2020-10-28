---
uid: Microsoft.Quantum.Convert.BigIntAsBoolArray
title: BigIntAsBoolArray 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BigIntAsBoolArray
qsharp.summary: Converts a given big integer to an array of Booleans. The 0 element of the array is the least significant bit of the big integer.
ms.openlocfilehash: 13ba5b6dbf477dd1a02f24da5b7aca9bdb30ad2b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713623"
---
# <a name="bigintasboolarray-function"></a><span data-ttu-id="f390c-102">BigIntAsBoolArray 함수</span><span class="sxs-lookup"><span data-stu-id="f390c-102">BigIntAsBoolArray function</span></span>

<span data-ttu-id="f390c-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="f390c-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="f390c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f390c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f390c-105">지정 된 큰 정수를 부울 배열로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f390c-105">Converts a given big integer to an array of Booleans.</span></span>
<span data-ttu-id="f390c-106">배열의 0 요소는 큰 정수의 최하위 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="f390c-106">The 0 element of the array is the least significant bit of the big integer.</span></span>

```qsharp
function BigIntAsBoolArray (a : BigInt) : Bool[]
```


## <a name="input"></a><span data-ttu-id="f390c-107">입력</span><span class="sxs-lookup"><span data-stu-id="f390c-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="f390c-108">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="f390c-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bool"></a><span data-ttu-id="f390c-109">Output: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="f390c-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="f390c-110">설명</span><span class="sxs-lookup"><span data-stu-id="f390c-110">Remarks</span></span>

<span data-ttu-id="f390c-111">자세한 내용은 [c # BigInteger 생성자](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f390c-111">See [C# BigInteger constructor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) for more details.</span></span>