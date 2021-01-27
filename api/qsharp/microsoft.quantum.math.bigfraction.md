---
uid: Microsoft.Quantum.Math.BigFraction
title: 이상 소수 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: bfbf49e7a3d060417e506a1977c20adc08b81f0e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846912"
---
# <a name="bigfraction-user-defined-type"></a><span data-ttu-id="d1f07-102">이상 소수 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="d1f07-102">BigFraction user defined type</span></span>

<span data-ttu-id="d1f07-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="d1f07-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="d1f07-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d1f07-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d1f07-105">폼의 유리수를 나타냅니다 `p/q` .</span><span class="sxs-lookup"><span data-stu-id="d1f07-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="d1f07-106">정수 `p` 는 튜플의 첫 번째 요소이 고 `q` 는 튜플의 두 번째 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f07-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a><span data-ttu-id="d1f07-107">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="d1f07-107">Named Items</span></span>

### <a name="numerator--bigint"></a><span data-ttu-id="d1f07-108">분자: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d1f07-108">Numerator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d1f07-109">분수의 분자입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f07-109">Numerator of the fraction.</span></span>
### <a name="denominator--bigint"></a><span data-ttu-id="d1f07-110">분모: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d1f07-110">Denominator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d1f07-111">분수의 분모입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f07-111">Denominator of the fraction/</span></span>