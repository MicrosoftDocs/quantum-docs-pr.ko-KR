---
uid: Microsoft.Quantum.Math._ExtendedGreatestCommonDivisorI
title: _ExtendedGreatestCommonDivisorI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: _ExtendedGreatestCommonDivisorI
qsharp.summary: Internal recursive call to calculate the GCD.
ms.openlocfilehash: 57b5fa7d7d1a97e4f335529d6c905467137a3175
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846935"
---
# <a name="_extendedgreatestcommondivisori-function"></a><span data-ttu-id="a46dd-102">_ExtendedGreatestCommonDivisorI 함수</span><span class="sxs-lookup"><span data-stu-id="a46dd-102">_ExtendedGreatestCommonDivisorI function</span></span>

<span data-ttu-id="a46dd-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="a46dd-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="a46dd-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a46dd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a46dd-105">GCD을 계산 하는 내부 재귀 호출입니다.</span><span class="sxs-lookup"><span data-stu-id="a46dd-105">Internal recursive call to calculate the GCD.</span></span>

```qsharp
function _ExtendedGreatestCommonDivisorI (signA : Int, signB : Int, r : (Int, Int), s : (Int, Int), t : (Int, Int)) : (Int, Int)
```


## <a name="input"></a><span data-ttu-id="a46dd-106">입력</span><span class="sxs-lookup"><span data-stu-id="a46dd-106">Input</span></span>

### <a name="signa--int"></a><span data-ttu-id="a46dd-107">signA: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a46dd-107">signA : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="signb--int"></a><span data-ttu-id="a46dd-108">signB: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a46dd-108">signB : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="r--intint"></a><span data-ttu-id="a46dd-109">r: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="a46dd-109">r : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>




### <a name="s--intint"></a><span data-ttu-id="a46dd-110">s: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="a46dd-110">s : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>




### <a name="t--intint"></a><span data-ttu-id="a46dd-111">t: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="a46dd-111">t : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>





## <a name="output--intint"></a><span data-ttu-id="a46dd-112">Output: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="a46dd-112">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

