---
uid: Microsoft.Quantum.Math.PowC
title: PowC 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PowC
qsharp.summary: Returns a number raised to a given power.
ms.openlocfilehash: 7dbadbd4c3cc16c3fa0bcd9b5b1acbee990e24ac
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846812"
---
# <a name="powc-function"></a><span data-ttu-id="72252-102">PowC 함수</span><span class="sxs-lookup"><span data-stu-id="72252-102">PowC function</span></span>

<span data-ttu-id="72252-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="72252-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="72252-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="72252-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="72252-105">지정 된 지 수 만큼 거듭제곱 한 숫자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="72252-105">Returns a number raised to a given power.</span></span>

```qsharp
function PowC (a : Microsoft.Quantum.Math.Complex, power : Microsoft.Quantum.Math.Complex) : Microsoft.Quantum.Math.Complex
```


## <a name="input"></a><span data-ttu-id="72252-106">입력</span><span class="sxs-lookup"><span data-stu-id="72252-106">Input</span></span>

### <a name="a--complex"></a><span data-ttu-id="72252-107">a: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="72252-107">a : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="72252-108">발생 시킬 $ $a 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="72252-108">The number $a$ that is to be raised.</span></span>


### <a name="power--complex"></a><span data-ttu-id="72252-109">전원: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="72252-109">power : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="72252-110">$A $가 발생 해야 하는 power $b $입니다.</span><span class="sxs-lookup"><span data-stu-id="72252-110">The power $b$ to which $a$ should be raised.</span></span>



## <a name="output--complex"></a><span data-ttu-id="72252-111">출력: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="72252-111">Output : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="72252-112">Power $a ^ b $</span><span class="sxs-lookup"><span data-stu-id="72252-112">The power $a^b$</span></span>