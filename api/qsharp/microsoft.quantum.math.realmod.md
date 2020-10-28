---
uid: Microsoft.Quantum.Math.RealMod
title: RealMod 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 6ec799885bd2f0d35314ed727356499efbe9fcf8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720404"
---
# <a name="realmod-function"></a><span data-ttu-id="36b85-102">RealMod 함수</span><span class="sxs-lookup"><span data-stu-id="36b85-102">RealMod function</span></span>

<span data-ttu-id="36b85-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="36b85-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="36b85-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="36b85-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="36b85-105">두 실수 사이의 모듈러스를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="36b85-105">Computes the modulus between two real numbers.</span></span>

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a><span data-ttu-id="36b85-106">입력</span><span class="sxs-lookup"><span data-stu-id="36b85-106">Input</span></span>

### <a name="value--double"></a><span data-ttu-id="36b85-107">값: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="36b85-107">value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="36b85-108">모듈러스를 사용할 실수 $x $입니다.</span><span class="sxs-lookup"><span data-stu-id="36b85-108">A real number $x$ to take the modulus of.</span></span>


### <a name="modulo--double"></a><span data-ttu-id="36b85-109">모듈로: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="36b85-109">modulo : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="36b85-110">와 관련 하 여 $x $의 모듈러스를 사용 하는 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="36b85-110">A real number to take the modulus of $x$ with respect to.</span></span>


### <a name="minvalue--double"></a><span data-ttu-id="36b85-111">minValue: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="36b85-111">minValue : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="36b85-112">이 함수에서 반환할 최소 값입니다.</span><span class="sxs-lookup"><span data-stu-id="36b85-112">The smallest value to be returned by this function.</span></span>



## <a name="output--double"></a><span data-ttu-id="36b85-113">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="36b85-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="36b85-114">설명</span><span class="sxs-lookup"><span data-stu-id="36b85-114">Remarks</span></span>

<span data-ttu-id="36b85-115">이 함수는 unit 원에 대 한 실제 줄을 래핑하고 입력에 해당 하는 단위 원에서 각도를 찾는 방법으로 실제 모듈러스를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="36b85-115">This function computes the real modulus by wrapping the real line about the unit circle, then finding the angle on the unit circle corresponding to the input.</span></span>
<span data-ttu-id="36b85-116">`minValue`입력은 unit 원을 잘라낼 위치를 효과적으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36b85-116">The `minValue` input then effectively specifies where to cut the unit circle.</span></span>