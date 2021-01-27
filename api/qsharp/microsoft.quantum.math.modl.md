---
uid: Microsoft.Quantum.Math.ModL
title: ModL 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModL
qsharp.summary: Returns the modulus of a number with respect to another number.
ms.openlocfilehash: f044ae16d93d31d0f28f5fcf076cff2bfef62eb8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846833"
---
# <a name="modl-function"></a><span data-ttu-id="8677b-102">ModL 함수</span><span class="sxs-lookup"><span data-stu-id="8677b-102">ModL function</span></span>

<span data-ttu-id="8677b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="8677b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="8677b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8677b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8677b-105">다른 숫자와 관련 된 숫자의 모듈러스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8677b-105">Returns the modulus of a number with respect to another number.</span></span>

```qsharp
function ModL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="8677b-106">입력</span><span class="sxs-lookup"><span data-stu-id="8677b-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="8677b-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="8677b-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="8677b-108">모듈러스가 반환 될 입력 $a $입니다.</span><span class="sxs-lookup"><span data-stu-id="8677b-108">The input $a$ whose modulus is to be returned.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="8677b-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="8677b-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="8677b-110">$A $의 모듈러스가 반환 되는 대상에 대 한 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="8677b-110">The number with respect to which the modulus of $a$ is to be returned.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="8677b-111">출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="8677b-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="8677b-112">모듈러스 $a \bmod b $입니다.</span><span class="sxs-lookup"><span data-stu-id="8677b-112">The modulus $a \bmod b$.</span></span>