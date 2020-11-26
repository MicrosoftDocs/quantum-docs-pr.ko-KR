---
uid: Microsoft.Quantum.Math.ModL
title: ModL 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModL
qsharp.summary: Returns the modulus of a number with respect to another number.
ms.openlocfilehash: 0b1ac69cc1474e9cfa6a3489b2b2fdf497e812e0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227797"
---
# <a name="modl-function"></a><span data-ttu-id="9c1a2-102">ModL 함수</span><span class="sxs-lookup"><span data-stu-id="9c1a2-102">ModL function</span></span>

<span data-ttu-id="9c1a2-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="9c1a2-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="9c1a2-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9c1a2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9c1a2-105">다른 숫자와 관련 된 숫자의 모듈러스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a2-105">Returns the modulus of a number with respect to another number.</span></span>

```qsharp
function ModL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="9c1a2-106">입력</span><span class="sxs-lookup"><span data-stu-id="9c1a2-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="9c1a2-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9c1a2-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9c1a2-108">모듈러스가 반환 될 입력 $a $입니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a2-108">The input $a$ whose modulus is to be returned.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="9c1a2-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9c1a2-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9c1a2-110">$A $의 모듈러스가 반환 되는 대상에 대 한 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a2-110">The number with respect to which the modulus of $a$ is to be returned.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="9c1a2-111">출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9c1a2-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9c1a2-112">모듈러스 $a \bmod b $입니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a2-112">The modulus $a \bmod b$.</span></span>