---
uid: Microsoft.Quantum.Math.PowC
title: PowC 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PowC
qsharp.summary: Returns a number raised to a given power.
ms.openlocfilehash: 57a0f4c8176a7f87835c7d096136e288c4875eea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194715"
---
# <a name="powc-function"></a><span data-ttu-id="2d765-102">PowC 함수</span><span class="sxs-lookup"><span data-stu-id="2d765-102">PowC function</span></span>

<span data-ttu-id="2d765-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="2d765-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="2d765-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2d765-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2d765-105">지정 된 지 수 만큼 거듭제곱 한 숫자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d765-105">Returns a number raised to a given power.</span></span>

```qsharp
function PowC (a : Microsoft.Quantum.Math.Complex, power : Microsoft.Quantum.Math.Complex) : Microsoft.Quantum.Math.Complex
```


## <a name="input"></a><span data-ttu-id="2d765-106">입력</span><span class="sxs-lookup"><span data-stu-id="2d765-106">Input</span></span>

### <a name="a--complex"></a><span data-ttu-id="2d765-107">a: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="2d765-107">a : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="2d765-108">발생 시킬 $ $a 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="2d765-108">The number $a$ that is to be raised.</span></span>


### <a name="power--complex"></a><span data-ttu-id="2d765-109">전원: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="2d765-109">power : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="2d765-110">$A $가 발생 해야 하는 power $b $입니다.</span><span class="sxs-lookup"><span data-stu-id="2d765-110">The power $b$ to which $a$ should be raised.</span></span>



## <a name="output--complex"></a><span data-ttu-id="2d765-111">출력: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="2d765-111">Output : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="2d765-112">Power $a ^ b $</span><span class="sxs-lookup"><span data-stu-id="2d765-112">The power $a^b$</span></span>