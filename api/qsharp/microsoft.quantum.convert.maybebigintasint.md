---
uid: Microsoft.Quantum.Convert.MaybeBigIntAsInt
title: MaybeBigIntAsInt 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: MaybeBigIntAsInt
qsharp.summary: Converts a given big integer to an equivalent integer, if possible. The function returns a pair of the resulting integer and a Boolean flag which is true, if and only if the conversion was possible.
ms.openlocfilehash: d0a598497e8a8f019bbd8da7db1c6cc4d7bde017
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224278"
---
# <a name="maybebigintasint-function"></a><span data-ttu-id="65dd3-102">MaybeBigIntAsInt 함수</span><span class="sxs-lookup"><span data-stu-id="65dd3-102">MaybeBigIntAsInt function</span></span>

<span data-ttu-id="65dd3-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="65dd3-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="65dd3-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="65dd3-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="65dd3-105">가능 하면 지정 된 큰 정수를 해당 하는 정수로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="65dd3-105">Converts a given big integer to an equivalent integer, if possible.</span></span>
<span data-ttu-id="65dd3-106">함수는 변환 가능한 경우에만 결과 정수 및 부울 플래그 (true)의 쌍을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="65dd3-106">The function returns a pair of the resulting integer and a Boolean flag which is true, if and only if the conversion was possible.</span></span>

```qsharp
function MaybeBigIntAsInt (a : BigInt) : (Int, Bool)
```


## <a name="input"></a><span data-ttu-id="65dd3-107">입력</span><span class="sxs-lookup"><span data-stu-id="65dd3-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="65dd3-108">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="65dd3-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--intbool"></a><span data-ttu-id="65dd3-109">Output: ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool))</span><span class="sxs-lookup"><span data-stu-id="65dd3-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool))</span></span>



## <a name="remarks"></a><span data-ttu-id="65dd3-110">설명</span><span class="sxs-lookup"><span data-stu-id="65dd3-110">Remarks</span></span>

<span data-ttu-id="65dd3-111">자세한 내용은 [c # BigInteger 생성자](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) 를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="65dd3-111">See [C# BigInteger constructor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) for more details.</span></span>