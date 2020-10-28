---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: EqualityWithinToleranceFact 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: de15a32d5b38c5ab8c681d2c052669a48cf676cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712748"
---
# <a name="equalitywithintolerancefact-function"></a><span data-ttu-id="1dc25-102">EqualityWithinToleranceFact 함수</span><span class="sxs-lookup"><span data-stu-id="1dc25-102">EqualityWithinToleranceFact function</span></span>

<span data-ttu-id="1dc25-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="1dc25-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="1dc25-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1dc25-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1dc25-105">고전 부동 소수점 값에 지정 된 절대 허용 오차 값이 필요한 값을 포함 하는 클레임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1dc25-105">Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.</span></span>

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="1dc25-106">입력</span><span class="sxs-lookup"><span data-stu-id="1dc25-106">Input</span></span>

### <a name="actual--double"></a><span data-ttu-id="1dc25-107">실제: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1dc25-107">actual : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1dc25-108">확인할 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="1dc25-108">The number to be checked.</span></span>


### <a name="expected--double"></a><span data-ttu-id="1dc25-109">예상: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1dc25-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1dc25-110">예상 값입니다.</span><span class="sxs-lookup"><span data-stu-id="1dc25-110">The expected value.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="1dc25-111">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1dc25-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1dc25-112">실제 및 예상의 차이에 대 한 절대 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="1dc25-112">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1dc25-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1dc25-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

