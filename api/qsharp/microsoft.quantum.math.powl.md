---
uid: Microsoft.Quantum.Math.PowL
title: PowL 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PowL
qsharp.summary: Returns a number raised to a given power.
ms.openlocfilehash: f7282a3639ca87dae731e39594576aa73c4602ac
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857459"
---
# <a name="powl-function"></a><span data-ttu-id="fabce-102">PowL 함수</span><span class="sxs-lookup"><span data-stu-id="fabce-102">PowL function</span></span>

<span data-ttu-id="fabce-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="fabce-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="fabce-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fabce-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fabce-105">지정 된 지 수 만큼 거듭제곱 한 숫자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fabce-105">Returns a number raised to a given power.</span></span>

```qsharp
function PowL (a : BigInt, power : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="fabce-106">입력</span><span class="sxs-lookup"><span data-stu-id="fabce-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="fabce-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="fabce-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="fabce-108">발생 시킬 $ $a 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="fabce-108">The number $a$ that is to be raised.</span></span>


### <a name="power--int"></a><span data-ttu-id="fabce-109">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fabce-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fabce-110">$A $가 발생 해야 하는 power $b $입니다.</span><span class="sxs-lookup"><span data-stu-id="fabce-110">The power $b$ to which $a$ should be raised.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="fabce-111">출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="fabce-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="fabce-112">Power $a ^ b $</span><span class="sxs-lookup"><span data-stu-id="fabce-112">The power $a^b$</span></span>