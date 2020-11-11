---
uid: Microsoft.Quantum.Canon.Angle
title: Angle 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: da3ecdaf1b2c88180bd2a660fac0b6e87b2cafa1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718489"
---
# <a name="angle-function"></a><span data-ttu-id="5e165-102">Angle 함수</span><span class="sxs-lookup"><span data-stu-id="5e165-102">Angle function</span></span>

<span data-ttu-id="5e165-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5e165-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5e165-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5e165-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5e165-105">에 짝수 1과-1이 있으면 1을 반환 `index` `index` 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e165-105">Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.</span></span>

```qsharp
function Angle (index : Int) : Int
```


## <a name="description"></a><span data-ttu-id="5e165-106">Description</span><span class="sxs-lookup"><span data-stu-id="5e165-106">Description</span></span>

<span data-ttu-id="5e165-107">값은 회전 각도를 결정 하는 지정 된 할당에 대 한 n 변수 및 함수의 Rademacher-Walsh 스펙트럼 계수의 부호에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e165-107">Value corresponds to the sign of the coefficient of the Rademacher-Walsh spectrum of the n-variable AND function for a given assignment that decides the angle of the rotation.</span></span>

## <a name="input"></a><span data-ttu-id="5e165-108">입력</span><span class="sxs-lookup"><span data-stu-id="5e165-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="5e165-109">인덱스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5e165-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5e165-110">입력 할당을 정수로 (0에서 2 ^ n-1)</span><span class="sxs-lookup"><span data-stu-id="5e165-110">Input assignment as integer (from 0 to 2^n - 1)</span></span>



## <a name="output--int"></a><span data-ttu-id="5e165-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5e165-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>
