---
uid: Microsoft.Quantum.Math.RealMod
title: RealMod 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 56da313fabb20655ec358120b8d9b435e4971159
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848357"
---
# <a name="realmod-function"></a><span data-ttu-id="456fa-102">RealMod 함수</span><span class="sxs-lookup"><span data-stu-id="456fa-102">RealMod function</span></span>

<span data-ttu-id="456fa-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="456fa-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="456fa-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="456fa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="456fa-105">두 실수 사이의 모듈러스를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="456fa-105">Computes the modulus between two real numbers.</span></span>

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a><span data-ttu-id="456fa-106">입력</span><span class="sxs-lookup"><span data-stu-id="456fa-106">Input</span></span>

### <a name="value--double"></a><span data-ttu-id="456fa-107">값: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="456fa-107">value : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="456fa-108">모듈러스를 사용할 실수 $x $입니다.</span><span class="sxs-lookup"><span data-stu-id="456fa-108">A real number $x$ to take the modulus of.</span></span>


### <a name="modulo--double"></a><span data-ttu-id="456fa-109">모듈로: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="456fa-109">modulo : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="456fa-110">와 관련 하 여 $x $의 모듈러스를 사용 하는 실수입니다.</span><span class="sxs-lookup"><span data-stu-id="456fa-110">A real number to take the modulus of $x$ with respect to.</span></span>


### <a name="minvalue--double"></a><span data-ttu-id="456fa-111">minValue: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="456fa-111">minValue : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="456fa-112">이 함수에서 반환할 최소 값입니다.</span><span class="sxs-lookup"><span data-stu-id="456fa-112">The smallest value to be returned by this function.</span></span>



## <a name="output--double"></a><span data-ttu-id="456fa-113">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="456fa-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="example"></a><span data-ttu-id="456fa-114">예</span><span class="sxs-lookup"><span data-stu-id="456fa-114">Example</span></span>

```qsharp
    // Returns 3 π / 2.
    let y = RealMod(5.5 * PI(), 2.0 * PI(), 0.0);
    // Returns -1.2, since +3.6 and -1.2 are 4.8 apart on the real line,
    // which is a multiple of 2.4.
    let z = RealMod(3.6, 2.4, -1.2);
```

## <a name="remarks"></a><span data-ttu-id="456fa-115">설명</span><span class="sxs-lookup"><span data-stu-id="456fa-115">Remarks</span></span>

<span data-ttu-id="456fa-116">이 함수는 unit 원에 대 한 실제 줄을 래핑하고 입력에 해당 하는 단위 원에서 각도를 찾는 방법으로 실제 모듈러스를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="456fa-116">This function computes the real modulus by wrapping the real line about the unit circle, then finding the angle on the unit circle corresponding to the input.</span></span>
<span data-ttu-id="456fa-117">`minValue`입력은 unit 원을 잘라낼 위치를 효과적으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="456fa-117">The `minValue` input then effectively specifies where to cut the unit circle.</span></span>