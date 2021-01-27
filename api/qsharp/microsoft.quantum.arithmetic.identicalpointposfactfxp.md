---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: IdenticalPointPosFactFxP 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 7212f918e1d0ee86b12b85caa6e0c27bc2cebe58
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846614"
---
# <a name="identicalpointposfactfxp-function"></a><span data-ttu-id="9f880-102">IdenticalPointPosFactFxP 함수</span><span class="sxs-lookup"><span data-stu-id="9f880-102">IdenticalPointPosFactFxP function</span></span>

<span data-ttu-id="9f880-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9f880-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9f880-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="9f880-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="9f880-105">제공 된 배열의 모든 고정 소수점 숫자가 최하위 비트에서 계산 될 때 동일한 점 위치를 갖도록 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f880-105">Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit.</span></span> <span data-ttu-id="9f880-106">즉, 비트 수 빼기 point position은 배열의 모든 고정 소수점 숫자에 대해 상수 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f880-106">I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.</span></span>

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a><span data-ttu-id="9f880-107">입력</span><span class="sxs-lookup"><span data-stu-id="9f880-107">Input</span></span>

### <a name="fixedpoints--fixedpoint"></a><span data-ttu-id="9f880-108">fixedPoints: [Fixedpoints](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span><span class="sxs-lookup"><span data-stu-id="9f880-108">fixedPoints : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]</span></span>

<span data-ttu-id="9f880-109">호환성을 검사 하는 퀀텀 고정 소수점 숫자 (어설션 사용)의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9f880-109">Array of quantum fixed-point numbers that will be checked for compatibility (using assertions).</span></span>



## <a name="output--unit"></a><span data-ttu-id="9f880-110">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9f880-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

