---
title: Microsoft Q# 숫자 라이브러리 사용
description: Microsoft 퀀텀 숫자 라이브러리에서 사용할 수 있는 형식 및 작업에 대해 알아봅니다.
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: conceptual
uid: microsoft.quantum.numerics.usage
no-loc:
- Q#
- $$v
ms.openlocfilehash: 92efd3b8677d2f27bc59f986ce6c9e915cd23652
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856438"
---
# <a name="using-the-numerics-library"></a><span data-ttu-id="05374-103">숫자 라이브러리 사용</span><span class="sxs-lookup"><span data-stu-id="05374-103">Using the Numerics library</span></span>

## <a name="overview"></a><span data-ttu-id="05374-104">개요</span><span class="sxs-lookup"><span data-stu-id="05374-104">Overview</span></span>

<span data-ttu-id="05374-105">숫자 라이브러리는 세 가지 구성 요소로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05374-105">The Numerics library consists of three components</span></span>

1. <span data-ttu-id="05374-106">정수 adder 및 비교 연산자를 사용 하는 **기본 정수 산술 연산**</span><span class="sxs-lookup"><span data-stu-id="05374-106">**Basic integer arithmetic** with integer adders and comparators</span></span>
1. <span data-ttu-id="05374-107">기본 기능을 기반으로 하는 **상위 수준의 정수 기능** 여기에는 곱하기, 나누기, 역 등이 포함 됩니다.  부호 있는 정수와 부호 없는 정수에 대 한입니다.</span><span class="sxs-lookup"><span data-stu-id="05374-107">**High-level integer functionality** that is built on top of the basic  functionality; it includes multiplication, division, inversion, etc.  for signed and unsigned integers.</span></span>
1. <span data-ttu-id="05374-108">고정 소수점 초기화, 더하기, 곱하기, 상호, 다항식 계산 및 측정이 포함 된 **고정 소수점 산술 기능** 입니다.</span><span class="sxs-lookup"><span data-stu-id="05374-108">**Fixed-point arithmetic functionality** with fixed-point initialization,  addition, multiplication, reciprocal, polynomial evaluation, and measurement.</span></span>

<span data-ttu-id="05374-109">이러한 모든 구성 요소는 단일 문을 사용 하 여 액세스할 수 있습니다 `open` .</span><span class="sxs-lookup"><span data-stu-id="05374-109">All of these components can be accessed using a single `open` statement:</span></span>
```qsharp
open Microsoft.Quantum.Arithmetic;
```

## <a name="types"></a><span data-ttu-id="05374-110">유형</span><span class="sxs-lookup"><span data-stu-id="05374-110">Types</span></span>

<span data-ttu-id="05374-111">숫자 라이브러리는 다음 형식을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05374-111">The numerics library supports the following types</span></span>

1. <span data-ttu-id="05374-112">**`LittleEndian`**: `qArr : Qubit[]` 가 최하위 비트를 표시 하는 정수를 나타내는의 정수 배열입니다 `qArr[0]` .</span><span class="sxs-lookup"><span data-stu-id="05374-112">**`LittleEndian`**: A qubit array `qArr : Qubit[]` that represents an integer where `qArr[0]` denotes the least significant bit.</span></span>
1. <span data-ttu-id="05374-113">**`SignedLittleEndian`**: `LittleEndian` 2의 보수에 저장 된 부호 있는 정수를 나타내는 점을 제외 하 고와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="05374-113">**`SignedLittleEndian`**: Same as `LittleEndian` except that it represents a signed integer stored in two's complement.</span></span>
1. <span data-ttu-id="05374-114">**`FixedPoint`**:은 (는) 바이트 배열과 이진 점 위치로 구성 된 실수를 나타내며 `qArr2 : Qubit[]` `pos` ,이는 이진 점 왼쪽의 이진 자릿수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="05374-114">**`FixedPoint`**: Represents a real number consisting of a qubit array `qArr2 : Qubit[]` and a binary point position `pos`, which counts the number of binary digits to the left of the binary point.</span></span> <span data-ttu-id="05374-115">`qArr2` 는와 같은 방식으로 저장 됩니다 `SignedLittleEndian` .</span><span class="sxs-lookup"><span data-stu-id="05374-115">`qArr2` is stored in the same way as `SignedLittleEndian`.</span></span>

## <a name="operations"></a><span data-ttu-id="05374-116">작업</span><span class="sxs-lookup"><span data-stu-id="05374-116">Operations</span></span>

<span data-ttu-id="05374-117">위의 세 가지 형식 각각에 대해 다양 한 작업을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05374-117">For each of the three types above, a variety of operations is available:</span></span>

1. **`LittleEndian`**
    - <span data-ttu-id="05374-118">더하기</span><span class="sxs-lookup"><span data-stu-id="05374-118">Addition</span></span>
    - <span data-ttu-id="05374-119">비교</span><span class="sxs-lookup"><span data-stu-id="05374-119">Comparison</span></span>
    - <span data-ttu-id="05374-120">곱하기</span><span class="sxs-lookup"><span data-stu-id="05374-120">Multiplication</span></span>
    - <span data-ttu-id="05374-121">제곱</span><span class="sxs-lookup"><span data-stu-id="05374-121">Squaring</span></span>
    - <span data-ttu-id="05374-122">나누기 (나머지 포함)</span><span class="sxs-lookup"><span data-stu-id="05374-122">Division (with remainder)</span></span>

1. **`SignedLittleEndian`**
    - <span data-ttu-id="05374-123">더하기</span><span class="sxs-lookup"><span data-stu-id="05374-123">Addition</span></span>
    - <span data-ttu-id="05374-124">비교</span><span class="sxs-lookup"><span data-stu-id="05374-124">Comparison</span></span>
    - <span data-ttu-id="05374-125">역 모듈로 2의 보수</span><span class="sxs-lookup"><span data-stu-id="05374-125">Inversion modulo 2's complement</span></span>
    - <span data-ttu-id="05374-126">곱하기</span><span class="sxs-lookup"><span data-stu-id="05374-126">Multiplication</span></span>
    - <span data-ttu-id="05374-127">제곱</span><span class="sxs-lookup"><span data-stu-id="05374-127">Squaring</span></span>

1. **`FixedPoint`**
    - <span data-ttu-id="05374-128">기존 값에 대 한 준비/초기화</span><span class="sxs-lookup"><span data-stu-id="05374-128">Preparation / initialization to a classical values</span></span>
    - <span data-ttu-id="05374-129">더하기 (기존 상수 또는 기타 퀀텀 고정 소수점)</span><span class="sxs-lookup"><span data-stu-id="05374-129">Addition (classical constant or other quantum fixed-point)</span></span>
    - <span data-ttu-id="05374-130">비교</span><span class="sxs-lookup"><span data-stu-id="05374-130">Comparison</span></span>
    - <span data-ttu-id="05374-131">곱하기</span><span class="sxs-lookup"><span data-stu-id="05374-131">Multiplication</span></span>
    - <span data-ttu-id="05374-132">제곱</span><span class="sxs-lookup"><span data-stu-id="05374-132">Squaring</span></span>
    - <span data-ttu-id="05374-133">짝수 및 홀수 함수를 위한 특수화로 다항식 계산</span><span class="sxs-lookup"><span data-stu-id="05374-133">Polynomial evaluation with specialization for even and odd functions</span></span>
    - <span data-ttu-id="05374-134">역 (1/x)</span><span class="sxs-lookup"><span data-stu-id="05374-134">Reciprocal (1/x)</span></span>
    - <span data-ttu-id="05374-135">측정 (고전적인 Double)</span><span class="sxs-lookup"><span data-stu-id="05374-135">Measurement (classical Double)</span></span>

<span data-ttu-id="05374-136">이러한 각 작업에 대 한 자세한 내용 및 자세한 설명서는 Q# [docs.microsoft.com](https://docs.microsoft.com/quantum) 에서 라이브러리 참조 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="05374-136">For more information and detailed documentation for each of these operations, see the Q# library reference docs at [docs.microsoft.com](https://docs.microsoft.com/quantum)</span></span>

## <a name="sample-integer-addition"></a><span data-ttu-id="05374-137">샘플: 정수 더하기</span><span class="sxs-lookup"><span data-stu-id="05374-137">Sample: Integer addition</span></span>

<span data-ttu-id="05374-138">기본 예로 $ $ \ket x\ket y\maps\ket x\ket {x + y} $ $를 사용 하는 것이 좋습니다. 즉, nstbit 정수 $x $ 및 n-또는 (n + 1)-stbit register $y $를 입력으로 사용 하 고 후자는 sum $ (x + y) $에 매핑되는 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="05374-138">As a basic example, consider the operation $$ \ket x\ket y\mapsto \ket x\ket{x+y} $$ that is, an operation that takes an n-qubit integer $x$ and an n- or (n+1)-qubit register $y$ as input, the latter of which it maps to the sum $(x+y)$.</span></span> <span data-ttu-id="05374-139">$Y $이 $n $ 비트 레지스터에 저장 된 경우 합계는 모듈러스 $2 ^ n $로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05374-139">Note that the sum is computed modulo $2^n$ if $y$ is stored in an $n$-bit register.</span></span>

<span data-ttu-id="05374-140">퀀텀 개발 키트를 사용 하 여 다음과 같이이 작업을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05374-140">Using the Quantum Development Kit, this operation can be applied as follows:</span></span>
```qsharp
operation TestMyAddition(xValue : Int, yValue : Int, n : Int) : Unit {
    using ((xQubits, yQubits) = (Qubit[n], Qubit[n]))
    {
        let x = LittleEndian(xQubits); // define bit order
        let y = LittleEndian(yQubits);
        
        ApplyXorInPlace(xValue, x); // initialize values
        ApplyXorInPlace(yValue, y);
        
        AddI(x, y); // perform addition x+y into y
        
        // ... (use the result)
    }
}
```

## <a name="sample-evaluating-smooth-functions"></a><span data-ttu-id="05374-141">샘플: 부드러운 함수 계산</span><span class="sxs-lookup"><span data-stu-id="05374-141">Sample: Evaluating smooth functions</span></span>

<span data-ttu-id="05374-142">퀀텀 컴퓨터에서 $ \sin (x) $와 같은 부드러운 함수를 평가 하기 위해 $x $은 퀀텀 번호이 `FixedPoint` 고, 퀀텀 개발 키트 숫자 라이브러리는 작업 및를 제공 합니다 `EvaluatePolynomialFxP` `Evaluate[Even/Odd]PolynomialFxP` .</span><span class="sxs-lookup"><span data-stu-id="05374-142">To evaluate smooth functions such as $\sin(x)$ on a quantum computer, where $x$ is a quantum `FixedPoint` number, the Quantum Development Kit numerics library provides the operations `EvaluatePolynomialFxP` and `Evaluate[Even/Odd]PolynomialFxP`.</span></span>

<span data-ttu-id="05374-143">첫 번째에서는 `EvaluatePolynomialFxP` $ $ P (x) = a_0 + a_1x + a_2x ^ 2 + \cdots ^ d, $ $ 형식의 다항식을 평가할 수 있습니다. 여기서 $d $는 *정도* 를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="05374-143">The first, `EvaluatePolynomialFxP`, allows to evaluate a polynomial of the form $$ P(x) = a_0 + a_1x + a_2x^2 + \cdots + a_dx^d, $$ where $d$ denotes the *degree*.</span></span> <span data-ttu-id="05374-144">이렇게 하려면 다항식 계수 `[a_0,..., a_d]` (형식 `Double[]` ), 입력 `x : FixedPoint` 및 출력 `y : FixedPoint` (처음에는 0)이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="05374-144">To do so, all that is needed are the polynomial coefficients `[a_0,..., a_d]` (of type `Double[]`), the input `x : FixedPoint` and the output `y : FixedPoint` (initially zero):</span></span>
```qsharp
EvaluatePolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="05374-145">결과 $P (x) = 1 + 2x $가에 저장 됩니다 `yFxP` .</span><span class="sxs-lookup"><span data-stu-id="05374-145">The result, $P(x)=1+2x$, will be stored in `yFxP`.</span></span>

<span data-ttu-id="05374-146">두 번째, `EvaluateEvenPolynomialFxP` 및 세 번째는 `EvaluateOddPolynomialFxP` 각각 짝수 및 홀수 함수의 사례에 대 한 특수화입니다.</span><span class="sxs-lookup"><span data-stu-id="05374-146">The second, `EvaluateEvenPolynomialFxP`, and the third, `EvaluateOddPolynomialFxP`, are specializations for the cases of even and odd functions, respectively.</span></span> <span data-ttu-id="05374-147">즉, 짝수/홀수 함수 $f (x) $ 및 $ $ P_ {짝수} (x) = a_0 + a_1 x ^ 2 + a_2 x ^ 4 + \cs+ a_d x ^ {2d}의 경우 $ $ $f (x) $는 $P _ {짝수} (x) $ 또는 $P _ {홀수} (x): = x\cdot P_ {짝수} (x) $에서 각각 합니다.</span><span class="sxs-lookup"><span data-stu-id="05374-147">That is, for an even/odd function $f(x)$ and $$ P_{even}(x)=a_0 + a_1 x^2 + a_2 x^4 + \cdots + a_d x^{2d}, $$ $f(x)$ is approximated well by $P_{even}(x)$ or $P_{odd}(x) := x\cdot P_{even}(x)$, respectively.</span></span>
<span data-ttu-id="05374-148">에서 Q# 이러한 두 가지 사례는 다음과 같이 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05374-148">In Q#, these two cases can be handled as follows:</span></span>
```qsharp
EvaluateEvenPolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="05374-149">이는 $P _ {짝수} (x) = 1 + 2x ^ 2 $를 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="05374-149">which evaluates $P_{even}(x) = 1 + 2x^2$, and</span></span>
```qsharp
EvaluateOddPolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="05374-150">$P _ {홀수} (x) = x + 2x ^ 3 $를 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="05374-150">which evaluates $P_{odd}(x) = x + 2x^3$.</span></span>

## <a name="more-samples"></a><span data-ttu-id="05374-151">다른 샘플</span><span class="sxs-lookup"><span data-stu-id="05374-151">More samples</span></span>

<span data-ttu-id="05374-152">[주 샘플 리포지토리에서](https://github.com/Microsoft/Quantum)더 많은 샘플을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05374-152">You can find more samples in the [main samples repository](https://github.com/Microsoft/Quantum).</span></span>

<span data-ttu-id="05374-153">시작 하려면 리포지토리를 복제 하 고 `Numerics` 하위 폴더를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="05374-153">To get started, clone the repo and open the `Numerics` subfolder:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics
```

<span data-ttu-id="05374-154">그런 다음 `cd` 샘플 폴더 중 하나에을 (를) 통해 샘플을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="05374-154">Then, `cd` into one of the sample folders and run the sample via</span></span>

```bash
dotnet run
```
