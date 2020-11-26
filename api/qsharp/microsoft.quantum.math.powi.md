---
uid: Microsoft.Quantum.Math.PowI
title: PowI 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PowI
qsharp.summary: Returns a number raised to a given power.
ms.openlocfilehash: a0466cbadd324f4aec87ba043f90af99d0d74a10
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194681"
---
# <a name="powi-function"></a><span data-ttu-id="033bd-102">PowI 함수</span><span class="sxs-lookup"><span data-stu-id="033bd-102">PowI function</span></span>

<span data-ttu-id="033bd-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="033bd-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="033bd-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="033bd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="033bd-105">지정 된 지 수 만큼 거듭제곱 한 숫자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="033bd-105">Returns a number raised to a given power.</span></span>

```qsharp
function PowI (a : Int, power : Int) : Int
```


## <a name="input"></a><span data-ttu-id="033bd-106">입력</span><span class="sxs-lookup"><span data-stu-id="033bd-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="033bd-107">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="033bd-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="033bd-108">발생 시킬 $ $a 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="033bd-108">The number $a$ that is to be raised.</span></span>


### <a name="power--int"></a><span data-ttu-id="033bd-109">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="033bd-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="033bd-110">$A $가 발생 해야 하는 power $b $입니다.</span><span class="sxs-lookup"><span data-stu-id="033bd-110">The power $b$ to which $a$ should be raised.</span></span>



## <a name="output--int"></a><span data-ttu-id="033bd-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="033bd-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="033bd-112">Power $a ^ b $</span><span class="sxs-lookup"><span data-stu-id="033bd-112">The power $a^b$</span></span>