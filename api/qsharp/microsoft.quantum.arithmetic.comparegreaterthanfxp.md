---
uid: Microsoft.Quantum.Arithmetic.CompareGreaterThanFxP
title: CompareGreaterThanFxP 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGreaterThanFxP
qsharp.summary: Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.
ms.openlocfilehash: bd3bcedd7a4a81fc600f7f4b6bdf1d2a797abbd4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721297"
---
# <a name="comparegreaterthanfxp-operation"></a><span data-ttu-id="01b6e-102">CompareGreaterThanFxP 작업</span><span class="sxs-lookup"><span data-stu-id="01b6e-102">CompareGreaterThanFxP operation</span></span>

<span data-ttu-id="01b6e-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="01b6e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="01b6e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="01b6e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="01b6e-105">퀀텀 레지스터에 저장 된 두 개의 고정 소수점 숫자를 비교 하 고 결과에서 대칭 이동을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="01b6e-105">Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.</span></span>

```qsharp
operation CompareGreaterThanFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="01b6e-106">입력</span><span class="sxs-lookup"><span data-stu-id="01b6e-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="01b6e-107">fp1: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="01b6e-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="01b6e-108">비교할 첫 번째 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="01b6e-108">First fixed-point number to be compared.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="01b6e-109">fp2: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="01b6e-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="01b6e-110">비교할 두 번째 고정 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="01b6e-110">Second fixed-point number to be compared.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="01b6e-111">결과: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="01b6e-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="01b6e-112">비교 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="01b6e-112">Result of the comparison.</span></span> <span data-ttu-id="01b6e-113">인 경우가 대칭 이동 됩니다 `fp1 > fp2` .</span><span class="sxs-lookup"><span data-stu-id="01b6e-113">Will be flipped if `fp1 > fp2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="01b6e-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="01b6e-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="01b6e-115">설명</span><span class="sxs-lookup"><span data-stu-id="01b6e-115">Remarks</span></span>

<span data-ttu-id="01b6e-116">현재 구현에서는 두 개의 고정 소수점 숫자가 동일한 점 위치와 동일한 수의 값을 갖도록 요구 합니다.</span><span class="sxs-lookup"><span data-stu-id="01b6e-116">The current implementation requires the two fixed-point numbers to have the same point position and the same number of qubits.</span></span>