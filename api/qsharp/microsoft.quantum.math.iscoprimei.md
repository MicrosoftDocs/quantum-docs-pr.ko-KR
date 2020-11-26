---
uid: Microsoft.Quantum.Math.IsCoprimeI
title: IsCoprimeI 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeI
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: 53131a755571ad1ac0a8a984bf229b16f67dbe51
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195361"
---
# <a name="iscoprimei-function"></a><span data-ttu-id="7c52a-102">IsCoprimeI 함수</span><span class="sxs-lookup"><span data-stu-id="7c52a-102">IsCoprimeI function</span></span>

<span data-ttu-id="7c52a-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="7c52a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="7c52a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7c52a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7c52a-105">$A $ 및 $b $가 같은 경우 true를 반환 하 고 그렇지 않으면 false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c52a-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="7c52a-106">입력</span><span class="sxs-lookup"><span data-stu-id="7c52a-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="7c52a-107">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7c52a-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7c52a-108">공동 primality을 테스트 하는 첫 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="7c52a-108">the first number of which co-primality is being tested</span></span>


### <a name="b--int"></a><span data-ttu-id="7c52a-109">b: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7c52a-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7c52a-110">공동 primality을 테스트 하는 두 번째 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="7c52a-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="7c52a-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7c52a-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7c52a-112">$A $ 및 $b $가 같은 경우 (예: 최대 공약수가 1 임) True이 고, 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="7c52a-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>