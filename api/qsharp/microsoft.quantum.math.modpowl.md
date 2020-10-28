---
uid: Microsoft.Quantum.Math.ModPowL
title: ModPowL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModPowL
qsharp.summary: Performs modular division on a number raised to the power of another number.
ms.openlocfilehash: 7d3e1de8c7d0eb5f35392bec373e7f16b152ca3c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723084"
---
# <a name="modpowl-function"></a><span data-ttu-id="17047-102">ModPowL 함수</span><span class="sxs-lookup"><span data-stu-id="17047-102">ModPowL function</span></span>

<span data-ttu-id="17047-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="17047-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="17047-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="17047-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="17047-105">다른 숫자의 승수로 거듭제곱 한 숫자에 대해 모듈식 나누기를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="17047-105">Performs modular division on a number raised to the power of another number.</span></span>

```qsharp
function ModPowL (value : BigInt, exponent : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="17047-106">입력</span><span class="sxs-lookup"><span data-stu-id="17047-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="17047-107">값: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="17047-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="exponent--bigint"></a><span data-ttu-id="17047-108">지 수: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="17047-108">exponent : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="modulus--bigint"></a><span data-ttu-id="17047-109">모듈러스: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="17047-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigint"></a><span data-ttu-id="17047-110">출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="17047-110">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>



## <a name="remarks"></a><span data-ttu-id="17047-111">설명</span><span class="sxs-lookup"><span data-stu-id="17047-111">Remarks</span></span>

<span data-ttu-id="17047-112">자세한 내용은 [BigInteger](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.modpow) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="17047-112">See [System.Numerics.BigInteger.ModPow](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.modpow) for more details.</span></span>