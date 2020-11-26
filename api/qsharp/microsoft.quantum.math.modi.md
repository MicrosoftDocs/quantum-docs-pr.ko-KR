---
uid: Microsoft.Quantum.Math.ModI
title: ModI 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModI
qsharp.summary: Returns the modulus of a number with respect to another number.
ms.openlocfilehash: e0d735096ce00b97ac42b336ac226e8e25879c94
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195021"
---
# <a name="modi-function"></a><span data-ttu-id="4b9b7-102">ModI 함수</span><span class="sxs-lookup"><span data-stu-id="4b9b7-102">ModI function</span></span>

<span data-ttu-id="4b9b7-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="4b9b7-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="4b9b7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4b9b7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4b9b7-105">다른 숫자와 관련 된 숫자의 모듈러스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-105">Returns the modulus of a number with respect to another number.</span></span>

```qsharp
function ModI (a : Int, b : Int) : Int
```


## <a name="input"></a><span data-ttu-id="4b9b7-106">입력</span><span class="sxs-lookup"><span data-stu-id="4b9b7-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="4b9b7-107">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4b9b7-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4b9b7-108">모듈러스가 반환 될 입력 $a $입니다.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-108">The input $a$ whose modulus is to be returned.</span></span>


### <a name="b--int"></a><span data-ttu-id="4b9b7-109">b: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4b9b7-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4b9b7-110">$A $의 모듈러스가 반환 되는 대상에 대 한 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-110">The number with respect to which the modulus of $a$ is to be returned.</span></span>



## <a name="output--int"></a><span data-ttu-id="4b9b7-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4b9b7-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4b9b7-112">모듈러스 $a \bmod b $입니다.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-112">The modulus $a \bmod b$.</span></span>