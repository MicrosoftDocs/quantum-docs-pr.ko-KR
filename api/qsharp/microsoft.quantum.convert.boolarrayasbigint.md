---
uid: Microsoft.Quantum.Convert.BoolArrayAsBigInt
title: BoolArrayAsBigInt 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsBigInt
qsharp.summary: Converts a given array of Booleans to an equivalent big integer. The 0 element of the array is the least significant bit of the big integer.
ms.openlocfilehash: 75656ba188a1b822eb42e98412365bf5873bf46e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713616"
---
# <a name="boolarrayasbigint-function"></a><span data-ttu-id="755db-102">BoolArrayAsBigInt 함수</span><span class="sxs-lookup"><span data-stu-id="755db-102">BoolArrayAsBigInt function</span></span>

<span data-ttu-id="755db-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="755db-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="755db-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="755db-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="755db-105">지정 된 부울 배열을 해당 하는 큰 정수로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="755db-105">Converts a given array of Booleans to an equivalent big integer.</span></span>
<span data-ttu-id="755db-106">배열의 0 요소는 큰 정수의 최하위 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="755db-106">The 0 element of the array is the least significant bit of the big integer.</span></span>

```qsharp
function BoolArrayAsBigInt (a : Bool[]) : BigInt
```


## <a name="input"></a><span data-ttu-id="755db-107">입력</span><span class="sxs-lookup"><span data-stu-id="755db-107">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="755db-108">a: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="755db-108">a : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>





## <a name="output--bigint"></a><span data-ttu-id="755db-109">출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="755db-109">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>



## <a name="remarks"></a><span data-ttu-id="755db-110">설명</span><span class="sxs-lookup"><span data-stu-id="755db-110">Remarks</span></span>

<span data-ttu-id="755db-111">자세한 내용은 [c # BigInteger 생성자](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="755db-111">See [C# BigInteger constructor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) for more details.</span></span>