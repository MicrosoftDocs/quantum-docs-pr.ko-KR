---
uid: Microsoft.Quantum.Math.PowI
title: PowI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PowI
qsharp.summary: Returns a number raised to a given power.
ms.openlocfilehash: c4e59f7c398a88485ada9d2b313b93aac530ce02
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857472"
---
# <a name="powi-function"></a><span data-ttu-id="28b09-102">PowI 함수</span><span class="sxs-lookup"><span data-stu-id="28b09-102">PowI function</span></span>

<span data-ttu-id="28b09-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="28b09-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="28b09-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="28b09-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="28b09-105">지정 된 지 수 만큼 거듭제곱 한 숫자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b09-105">Returns a number raised to a given power.</span></span>

```qsharp
function PowI (a : Int, power : Int) : Int
```


## <a name="input"></a><span data-ttu-id="28b09-106">입력</span><span class="sxs-lookup"><span data-stu-id="28b09-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="28b09-107">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="28b09-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="28b09-108">발생 시킬 $ $a 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="28b09-108">The number $a$ that is to be raised.</span></span>


### <a name="power--int"></a><span data-ttu-id="28b09-109">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="28b09-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="28b09-110">$A $가 발생 해야 하는 power $b $입니다.</span><span class="sxs-lookup"><span data-stu-id="28b09-110">The power $b$ to which $a$ should be raised.</span></span>



## <a name="output--int"></a><span data-ttu-id="28b09-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="28b09-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="28b09-112">Power $a ^ b $</span><span class="sxs-lookup"><span data-stu-id="28b09-112">The power $a^b$</span></span>