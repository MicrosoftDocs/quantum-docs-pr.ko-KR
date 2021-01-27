---
uid: Microsoft.Quantum.Math.PowCP
title: PowCP 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PowCP
qsharp.summary: Returns a number raised to a given power.
ms.openlocfilehash: 573eb4ecab62ad117787e0d248f00c7e51f7f98b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847033"
---
# <a name="powcp-function"></a><span data-ttu-id="18eb6-102">PowCP 함수</span><span class="sxs-lookup"><span data-stu-id="18eb6-102">PowCP function</span></span>

<span data-ttu-id="18eb6-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="18eb6-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="18eb6-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="18eb6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="18eb6-105">지정 된 지 수 만큼 거듭제곱 한 숫자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="18eb6-105">Returns a number raised to a given power.</span></span>

```qsharp
function PowCP (a : Microsoft.Quantum.Math.ComplexPolar, power : Microsoft.Quantum.Math.ComplexPolar) : Microsoft.Quantum.Math.ComplexPolar
```


## <a name="input"></a><span data-ttu-id="18eb6-106">입력</span><span class="sxs-lookup"><span data-stu-id="18eb6-106">Input</span></span>

### <a name="a--complexpolar"></a><span data-ttu-id="18eb6-107">a: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="18eb6-107">a : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="18eb6-108">발생 시킬 $ $a 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="18eb6-108">The number $a$ that is to be raised.</span></span>


### <a name="power--complexpolar"></a><span data-ttu-id="18eb6-109">power: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="18eb6-109">power : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="18eb6-110">$A $가 발생 해야 하는 power $b $입니다.</span><span class="sxs-lookup"><span data-stu-id="18eb6-110">The power $b$ to which $a$ should be raised.</span></span>



## <a name="output--complexpolar"></a><span data-ttu-id="18eb6-111">출력: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="18eb6-111">Output : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="18eb6-112">Power $a ^ b $</span><span class="sxs-lookup"><span data-stu-id="18eb6-112">The power $a^b$</span></span>