---
uid: Microsoft.Quantum.Math.IsCoprimeI
title: IsCoprimeI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeI
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: 2c110f9abf18ee81bd72a68601d5c41ff756290a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851360"
---
# <a name="iscoprimei-function"></a><span data-ttu-id="ae4ed-102">IsCoprimeI 함수</span><span class="sxs-lookup"><span data-stu-id="ae4ed-102">IsCoprimeI function</span></span>

<span data-ttu-id="ae4ed-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="ae4ed-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="ae4ed-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ae4ed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ae4ed-105">$A $ 및 $b $가 같은 경우 true를 반환 하 고 그렇지 않으면 false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ed-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="ae4ed-106">입력</span><span class="sxs-lookup"><span data-stu-id="ae4ed-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="ae4ed-107">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ae4ed-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ae4ed-108">공동 primality을 테스트 하는 첫 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ed-108">the first number of which co-primality is being tested</span></span>


### <a name="b--int"></a><span data-ttu-id="ae4ed-109">b: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ae4ed-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ae4ed-110">공동 primality을 테스트 하는 두 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ed-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="ae4ed-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ae4ed-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ae4ed-112">$A $ 및 $b $가 같은 경우 (예: 최대 공약수가 1 임) True이 고, 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ed-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>