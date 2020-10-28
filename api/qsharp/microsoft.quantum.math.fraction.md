---
uid: Microsoft.Quantum.Math.Fraction
title: 분수 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 350d470c374fc8e0a3f4c4a9a68ad8566ab88727
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723658"
---
# <a name="fraction-user-defined-type"></a><span data-ttu-id="7eca6-102">분수 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="7eca6-102">Fraction user defined type</span></span>

<span data-ttu-id="7eca6-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="7eca6-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="7eca6-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7eca6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7eca6-105">폼의 유리수를 나타냅니다 `p/q` .</span><span class="sxs-lookup"><span data-stu-id="7eca6-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="7eca6-106">정수 `p` 는 튜플의 첫 번째 요소이 고 `q` 는 튜플의 두 번째 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="7eca6-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a><span data-ttu-id="7eca6-107">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="7eca6-107">Named Items</span></span>

### <a name="numerator--int"></a><span data-ttu-id="7eca6-108">분자: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7eca6-108">Numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7eca6-109">분수의 분자입니다.</span><span class="sxs-lookup"><span data-stu-id="7eca6-109">Numerator of the fraction.</span></span>
### <a name="denominator--int"></a><span data-ttu-id="7eca6-110">분모: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7eca6-110">Denominator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7eca6-111">분수의 분모입니다.</span><span class="sxs-lookup"><span data-stu-id="7eca6-111">Denominator of the fraction/</span></span>