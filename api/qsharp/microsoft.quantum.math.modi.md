---
uid: Microsoft.Quantum.Math.ModI
title: ModI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModI
qsharp.summary: Returns the modulus of a number with respect to another number.
ms.openlocfilehash: 8f4ff37767e5120b99834a63ed19055ba1806907
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848053"
---
# <a name="modi-function"></a><span data-ttu-id="eb87e-102">ModI 함수</span><span class="sxs-lookup"><span data-stu-id="eb87e-102">ModI function</span></span>

<span data-ttu-id="eb87e-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="eb87e-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="eb87e-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="eb87e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="eb87e-105">다른 숫자와 관련 된 숫자의 모듈러스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb87e-105">Returns the modulus of a number with respect to another number.</span></span>

```qsharp
function ModI (a : Int, b : Int) : Int
```


## <a name="input"></a><span data-ttu-id="eb87e-106">입력</span><span class="sxs-lookup"><span data-stu-id="eb87e-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="eb87e-107">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eb87e-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eb87e-108">모듈러스가 반환 될 입력 $a $입니다.</span><span class="sxs-lookup"><span data-stu-id="eb87e-108">The input $a$ whose modulus is to be returned.</span></span>


### <a name="b--int"></a><span data-ttu-id="eb87e-109">b: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eb87e-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eb87e-110">$A $의 모듈러스가 반환 되는 대상에 대 한 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="eb87e-110">The number with respect to which the modulus of $a$ is to be returned.</span></span>



## <a name="output--int"></a><span data-ttu-id="eb87e-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eb87e-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eb87e-112">모듈러스 $a \bmod b $입니다.</span><span class="sxs-lookup"><span data-stu-id="eb87e-112">The modulus $a \bmod b$.</span></span>