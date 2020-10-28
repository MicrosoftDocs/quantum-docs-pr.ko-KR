---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: NearEqualityFactD 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 5b55f515b27667071218a3f604ef703a6a15206d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712650"
---
# <a name="nearequalityfactd-function"></a><span data-ttu-id="85e1c-102">NearEqualityFactD 함수</span><span class="sxs-lookup"><span data-stu-id="85e1c-102">NearEqualityFactD function</span></span>

<span data-ttu-id="85e1c-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="85e1c-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="85e1c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="85e1c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="85e1c-105">고전적인 부동 소수점 값에 필요한 값이 1e-10의 최대 허용 오차 보다 작은 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e1c-105">Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.</span></span>

```qsharp
function NearEqualityFactD (actual : Double, expected : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="85e1c-106">입력</span><span class="sxs-lookup"><span data-stu-id="85e1c-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="85e1c-107">실제: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="85e1c-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="85e1c-108">확인할 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="85e1c-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="85e1c-109">예상: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="85e1c-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="85e1c-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="85e1c-110">The expected value.</span></span>



## <a name="output--unit"></a><span data-ttu-id="85e1c-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="85e1c-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="85e1c-112">설명</span><span class="sxs-lookup"><span data-stu-id="85e1c-112">Remarks</span></span>

<span data-ttu-id="85e1c-113">이는 <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> 하드 코드 된 허용 오차를 $10 ^ $로 사용 하는 것과 같습니다 {-10} .</span><span class="sxs-lookup"><span data-stu-id="85e1c-113">This is equivalent to <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> with hardcoded tolerance of $10^{-10}$.</span></span>