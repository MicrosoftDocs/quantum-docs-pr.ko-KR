---
uid: Microsoft.Quantum.Math.Lg
title: Lg 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Lg
qsharp.summary: Computes the base-2 logarithm of a number.
ms.openlocfilehash: da6548691437ffd9470bc93e6a69c8d38854c984
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851323"
---
# <a name="lg-function"></a><span data-ttu-id="25f63-102">Lg 함수</span><span class="sxs-lookup"><span data-stu-id="25f63-102">Lg function</span></span>

<span data-ttu-id="25f63-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="25f63-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="25f63-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="25f63-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="25f63-105">숫자의 밑이 2 인 로그를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="25f63-105">Computes the base-2 logarithm of a number.</span></span>

```qsharp
function Lg (input : Double) : Double
```


## <a name="input"></a><span data-ttu-id="25f63-106">입력</span><span class="sxs-lookup"><span data-stu-id="25f63-106">Input</span></span>

### <a name="input--double"></a><span data-ttu-id="25f63-107">입력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="25f63-107">input : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="25f63-108">실수 $x $입니다.</span><span class="sxs-lookup"><span data-stu-id="25f63-108">A real number $x$.</span></span>



## <a name="output--double"></a><span data-ttu-id="25f63-109">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="25f63-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="25f63-110">밑이 2 인 $y = \ log_2 (x) $는 $x = 2 ^ y $입니다.</span><span class="sxs-lookup"><span data-stu-id="25f63-110">The base-2 logarithm $y = \log_2(x)$ such that $x = 2^y$.</span></span>