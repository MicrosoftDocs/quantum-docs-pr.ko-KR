---
uid: Microsoft.Quantum.Math.PowCP
title: PowCP 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PowCP
qsharp.summary: Returns a number raised to a given power.
ms.openlocfilehash: 185d40acff6027a775130faaff64582c58384a90
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194647"
---
# <a name="powcp-function"></a><span data-ttu-id="f9675-102">PowCP 함수</span><span class="sxs-lookup"><span data-stu-id="f9675-102">PowCP function</span></span>

<span data-ttu-id="f9675-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="f9675-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="f9675-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f9675-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f9675-105">지정 된 지 수 만큼 거듭제곱 한 숫자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9675-105">Returns a number raised to a given power.</span></span>

```qsharp
function PowCP (a : Microsoft.Quantum.Math.ComplexPolar, power : Microsoft.Quantum.Math.ComplexPolar) : Microsoft.Quantum.Math.ComplexPolar
```


## <a name="input"></a><span data-ttu-id="f9675-106">입력</span><span class="sxs-lookup"><span data-stu-id="f9675-106">Input</span></span>

### <a name="a--complexpolar"></a><span data-ttu-id="f9675-107">a: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="f9675-107">a : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="f9675-108">발생 시킬 $ $a 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="f9675-108">The number $a$ that is to be raised.</span></span>


### <a name="power--complexpolar"></a><span data-ttu-id="f9675-109">power: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="f9675-109">power : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="f9675-110">$A $가 발생 해야 하는 power $b $입니다.</span><span class="sxs-lookup"><span data-stu-id="f9675-110">The power $b$ to which $a$ should be raised.</span></span>



## <a name="output--complexpolar"></a><span data-ttu-id="f9675-111">출력: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="f9675-111">Output : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="f9675-112">Power $a ^ b $</span><span class="sxs-lookup"><span data-stu-id="f9675-112">The power $a^b$</span></span>