---
title: 'Q # 식'
description: 'Q #에서 상수, 변수, 연산자, 작업 및 함수를 식으로 지정, 참조 및 결합 하는 방법을 이해 합니다.'
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.expressions
ms.openlocfilehash: 095be52af27f827f3e52d39a70702f50d6d59ee8
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82683919"
---
# <a name="expressions"></a><span data-ttu-id="58b53-103">표현식</span><span class="sxs-lookup"><span data-stu-id="58b53-103">Expressions</span></span>

## <a name="grouping"></a><span data-ttu-id="58b53-104">Grouping(그룹화)</span><span class="sxs-lookup"><span data-stu-id="58b53-104">Grouping</span></span>

<span data-ttu-id="58b53-105">식이 지정 된 경우 괄호로 묶인 동일한 식이 동일한 형식의 식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-105">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="58b53-106">예를 들어 `(7)` ,은 `Int` 식 `([1,2,3])` 이며는 `Int`s `((1,2))` 형식의 식이고는 형식이 `(Int, Int)`인 식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-106">For instance, `(7)` is an `Int` expression, `([1,2,3])` is an expression of type array of `Int`s, and `((1,2))` is an expression with type `(Int, Int)`.</span></span>

<span data-ttu-id="58b53-107">[형식 모델](xref:microsoft.quantum.language.type-model#tuple-types) 에 설명 된 단순 값과 단일 요소 튜플의 동등성은 그룹 및 `(6)` `(6)` 단일 요소 튜플로 인 한 모호성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-107">The equivalence between simple values and single-element tuples described in [the type model](xref:microsoft.quantum.language.type-model#tuple-types) removes the ambiguity between `(6)` as a group and `(6)` as a single-element tuple.</span></span>

## <a name="symbols"></a><span data-ttu-id="58b53-108">기호</span><span class="sxs-lookup"><span data-stu-id="58b53-108">Symbols</span></span>

<span data-ttu-id="58b53-109">형식의 `'T` 값에 바인딩하거나 할당 된 기호의 이름은 형식의 `'T`식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-109">The name of a symbol bound or assigned to a value of type `'T` is an expression of type `'T`.</span></span>
<span data-ttu-id="58b53-110">예를 들어, 기호가 `count` 정수 값 `5`에 바인딩되면 `count` 는 정수 식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-110">For instance, if the symbol `count` is bound to the integer value `5`, then `count` is an integer expression.</span></span>

## <a name="numeric-expressions"></a><span data-ttu-id="58b53-111">숫자 식</span><span class="sxs-lookup"><span data-stu-id="58b53-111">Numeric Expressions</span></span>

<span data-ttu-id="58b53-112">숫자 식은, `Int` `BigInt`또는 `Double`형식의 식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-112">Numeric expressions are expressions of type `Int`, `BigInt`, or `Double`.</span></span>
<span data-ttu-id="58b53-113">즉, 정수 또는 부동 소수점 숫자 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-113">That is, they are either integer or floating-point numbers.</span></span>

<span data-ttu-id="58b53-114">`Int`Q #의 리터럴은 후행 "l" 또는 "L"이 필요 하거나 허용 되지 않는다는 점을 제외 하 고 c #의 정수 리터럴과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-114">`Int` literals in Q# are identical to integer literals in C#, except that no trailing "l" or "L" is required (or allowed).</span></span>
<span data-ttu-id="58b53-115">16 진수 및 이진 정수는 각각 "0x" 및 "0b" 접두사를 사용 하 여 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-115">Hexadecimal and binary integers are supported with a "0x" and "0b" prefix respectively.</span></span>

<span data-ttu-id="58b53-116">`BigInt`Q #의 리터럴은 .NET의 큰 정수 문자열과 같으며 그 뒤에는 "l" 또는 "L"이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-116">`BigInt` literals in Q# are identical to big integer strings in .NET, with a trailing "l" or "L".</span></span>
<span data-ttu-id="58b53-117">16 진수 큰 정수는 "0x" 접두사를 사용 하 여 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-117">Hexadecimal big integers are supported with a "0x" prefix.</span></span>
<span data-ttu-id="58b53-118">따라서 다음은 리터럴의 모든 유효한 사용입니다 `BigInt` .</span><span class="sxs-lookup"><span data-stu-id="58b53-118">Thus, the following are all valid uses of `BigInt` literals:</span></span>

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

<span data-ttu-id="58b53-119">`Double`Q #의 리터럴은 후행 "d" 또는 "D"가 필요 하거나 허용 되지 않는다는 점을 제외 하 고 c #의 이중 리터럴과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-119">`Double` literals in Q# are identical to double literals in C#, except that no trailing "d" or "D" is required (or allowed).</span></span>

<span data-ttu-id="58b53-120">모든 요소 형식의 배열 식이 `Int` 지정 된 경우 `Length` 기본 제공 함수를 사용 하 여 식을 구성 하 `(` 고, 배열 식이 괄호로 묶여 있으며 `)`,를 사용 하 여 식을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-120">Given an array expression of any element type, an `Int` expression may be formed using the `Length` built-in function, with the array expression enclosed in parentheses, `(` and `)`.</span></span>
<span data-ttu-id="58b53-121">예를 들어가 `a` 배열에 바인딩된 경우 `Length(a)` 는 정수 식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-121">For instance, if `a` is bound to an array, then `Length(a)` is an integer expression.</span></span>
<span data-ttu-id="58b53-122">가 `b` `Int[][]`정수 배열의 `Length(b)` 배열인 경우는의 `b`하위 배열 수이 고 `Length(b[1])` 은의 `b`두 번째 하위 배열에 있는 정수 수입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-122">If `b` is an array of arrays of integers, `Int[][]`, then `Length(b)` is the number of sub-arrays in `b`, and `Length(b[1])` is the number of integers in the second sub-array in `b`.</span></span>

<span data-ttu-id="58b53-123">동일한 형식의 두 숫자 식이 지정 된 경우 이항 `+`연산자, `-`, `*`및 `/` 를 사용 하 여 새 숫자 식을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-123">Given two numeric expressions of the same type, the binary operators `+`, `-`, `*`, and `/` may be used to form a new numeric expression.</span></span>
<span data-ttu-id="58b53-124">새 식의 형식은 구성 식의 형식과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-124">The type of the new expression will be the same as the types of the constituent expressions.</span></span>

<span data-ttu-id="58b53-125">두 개의 정수 식이 지정 되 면 이항 `^` 연산자 (power)를 사용 하 여 새 정수 식을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-125">Given two integer expressions, the binary operator `^` (power) may be used to form a new integer expression.</span></span>
<span data-ttu-id="58b53-126">마찬가지로를 `^` 두 개의 double 식과 함께 사용 하 여 새 double 식을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-126">Similarly, `^` may be used with two double expressions to form a new double expression.</span></span>
<span data-ttu-id="58b53-127">마지막으로 `^` ,은 왼쪽에서 큰 정수를 사용 하 고 오른쪽에는 정수를 사용 하 여 새 큰 정수 식을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-127">Finally, `^` may be used with a big integer on the left and an integer on the right to form a new big integer expression.</span></span>
<span data-ttu-id="58b53-128">이 경우 두 번째 매개 변수는 32 비트에 맞아야 합니다. 그렇지 않으면 런타임 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-128">In this case, the second parameter must fit into 32 bits; if not, a runtime error will be raised.</span></span>

<span data-ttu-id="58b53-129">두 개의 정수 또는 큰 정수 식이 지정 된 `%` 경우 (모듈러스), `&&&` (비트 and), `|||` (비트 or) 또는 `^^^` (비트 XOR) 연산자를 사용 하 여 새 정수 또는 큰 정수 식의 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-129">Given two integer or big integer expressions, a new integer or big integer expression may be formed using the `%` (modulus), `&&&` (bitwise AND), `|||` (bitwise OR), or `^^^` (bitwise XOR) operators.</span></span>

<span data-ttu-id="58b53-130">왼쪽에 정수 또는 큰 정수 식이 있고 오른쪽에 정수 식이 지정 된 경우 `<<<` (산술 왼쪽 시프트) 또는 `>>>` (산술 오른쪽 시프트) 연산자를 사용 하 여 왼쪽 식과 동일한 형식의 새 식을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-130">Given either an integer or big integer expression on the left, and an integer expression on the right, the `<<<` (arithmetic left shift) or `>>>` (arithmetic right shift) operators may be used to create a new expression with the same type as the left-hand expression.</span></span>

<span data-ttu-id="58b53-131">이동 작업에 대 한 두 번째 매개 변수 (이동 크기)는 0 보다 크거나 같아야 합니다. 음수 시프트 금액의 동작은 정의 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-131">The second parameter (the shift amount) to either shift operation must be greater than or equal to zero; the behavior for negative shift amounts is undefined.</span></span>
<span data-ttu-id="58b53-132">시프트 연산의 이동 양은 32 비트에도 맞아야 합니다. 그렇지 않으면 런타임 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-132">The shift amount for either shift operation must also fit into 32 bits; if not, a runtime error will be raised.</span></span>
<span data-ttu-id="58b53-133">이동할 숫자가 정수 이면 시프트 금액이 해석 `mod 64`됩니다. 즉, 1의 교대조와 65의 시프트는 동일한 효과를 가집니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-133">If the number to be shifted is an integer, then the shift amount is interpreted `mod 64`; that is, a shift of 1 and a shift of 65 have the same effect.</span></span>

<span data-ttu-id="58b53-134">정수 및 큰 정수 값 모두에 대해 시프트는 산술 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-134">For both integer and big integer values, shifts are arithmetic.</span></span>
<span data-ttu-id="58b53-135">음수 값을 왼쪽 이나 오른쪽으로 이동 하면 음수가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-135">Shifting a negative value either left or right will result in a negative number.</span></span>
<span data-ttu-id="58b53-136">즉, 한 단계를 왼쪽 또는 오른쪽으로 이동 하는 것은 각각 2로의 곱하기 또는 나누기와 정확히 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-136">That is, shifting one step to the left or right is exactly the same as multiplying or dividing by 2, respectively.</span></span>

<span data-ttu-id="58b53-137">정수 나누기와 정수 모듈러스는 c #과 같은 음수에 대해 동일한 동작을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-137">Integer division and integer modulus follow the same behavior for negative numbers as C#.</span></span>
<span data-ttu-id="58b53-138">즉, `a % b` 는 항상와 `a` `b * (a / b) + a % b` 동일한 기호를 가집니다 `a`.이는 항상와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-138">That is, `a % b` will always have the same sign as `a`, and `b * (a / b) + a % b` will always equal `a`.</span></span>
<span data-ttu-id="58b53-139">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="58b53-139">For example:</span></span>

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 <span data-ttu-id="58b53-140">5</span><span class="sxs-lookup"><span data-stu-id="58b53-140">5</span></span> | <span data-ttu-id="58b53-141">2</span><span class="sxs-lookup"><span data-stu-id="58b53-141">2</span></span> | <span data-ttu-id="58b53-142">2</span><span class="sxs-lookup"><span data-stu-id="58b53-142">2</span></span> | <span data-ttu-id="58b53-143">1</span><span class="sxs-lookup"><span data-stu-id="58b53-143">1</span></span>
 <span data-ttu-id="58b53-144">5</span><span class="sxs-lookup"><span data-stu-id="58b53-144">5</span></span> | <span data-ttu-id="58b53-145">-2</span><span class="sxs-lookup"><span data-stu-id="58b53-145">-2</span></span> | <span data-ttu-id="58b53-146">-2</span><span class="sxs-lookup"><span data-stu-id="58b53-146">-2</span></span> | <span data-ttu-id="58b53-147">1</span><span class="sxs-lookup"><span data-stu-id="58b53-147">1</span></span>
 <span data-ttu-id="58b53-148">-5</span><span class="sxs-lookup"><span data-stu-id="58b53-148">-5</span></span> | <span data-ttu-id="58b53-149">2</span><span class="sxs-lookup"><span data-stu-id="58b53-149">2</span></span> | <span data-ttu-id="58b53-150">-2</span><span class="sxs-lookup"><span data-stu-id="58b53-150">-2</span></span> | <span data-ttu-id="58b53-151">-1</span><span class="sxs-lookup"><span data-stu-id="58b53-151">-1</span></span>
 <span data-ttu-id="58b53-152">-5</span><span class="sxs-lookup"><span data-stu-id="58b53-152">-5</span></span> | <span data-ttu-id="58b53-153">-2</span><span class="sxs-lookup"><span data-stu-id="58b53-153">-2</span></span> | <span data-ttu-id="58b53-154">2</span><span class="sxs-lookup"><span data-stu-id="58b53-154">2</span></span> | <span data-ttu-id="58b53-155">-1</span><span class="sxs-lookup"><span data-stu-id="58b53-155">-1</span></span>

<span data-ttu-id="58b53-156">큰 정수 나누기와 모듈러스는 동일한 방식으로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-156">Big integer division and modulus works the same way.</span></span>

<span data-ttu-id="58b53-157">숫자 식이 지정 된 경우 `-` 단항 연산자를 사용 하 여 새 식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-157">Given any numeric expression, a new expression may be formed using the `-` unary operator.</span></span>
<span data-ttu-id="58b53-158">새 식은 구성 식과 동일한 형식이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-158">The new expression will be the same type as the constituent expression.</span></span>

<span data-ttu-id="58b53-159">정수 또는 큰 정수 식이 지정 된 경우 `~~~` (비트 보수) 단항 연산자를 사용 하 여 동일한 유형의 새 식을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-159">Given any integer or big integer expression, a new expression of the same type may be formed using the `~~~` (bitwise complement) unary operator.</span></span>

## <a name="boolean-expressions"></a><span data-ttu-id="58b53-160">부울 식</span><span class="sxs-lookup"><span data-stu-id="58b53-160">Boolean Expressions</span></span>

<span data-ttu-id="58b53-161">두 `Bool` 리터럴 값은 `true` 및 `false`입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-161">The two `Bool` literal values are `true` and `false`.</span></span>

<span data-ttu-id="58b53-162">동일한 기본 형식의 두 식이 지정 된 경우 `==` 및 `!=` 이항 연산자를 사용 하 여 `Bool` 식을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-162">Given any two expressions of the same primitive type, the `==` and `!=` binary operators may be used to construct a `Bool` expression.</span></span>
<span data-ttu-id="58b53-163">식은 두 식이 같으면 true이 고, 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-163">The expression will be true if the two expressions are equal, and false if not.</span></span>

<span data-ttu-id="58b53-164">사용자 정의 형식의 값을 비교할 수 없습니다. 래핑 해제 된 값만 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-164">Values of user-defined types may not be compared, only their unwrapped values can be compared.</span></span> <span data-ttu-id="58b53-165">예를 들어 "래핑 해제" 연산자 `!` ( [Q # 형식 모델 페이지](xref:microsoft.quantum.language.type-model#user-defined-types)에서 설명)를 사용 하는 경우</span><span class="sxs-lookup"><span data-stu-id="58b53-165">For example, using the "unwrap" operator `!` (explained in the [Q# type model page](xref:microsoft.quantum.language.type-model#user-defined-types)),</span></span>

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

<span data-ttu-id="58b53-166">값에 대 `Qubit` 한 같음 비교는 id 같음입니다. 즉, 두 식이 동일한의 비트를 식별 하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-166">Equality comparison for `Qubit` values is identity equality; that is, whether the two expressions identify the same qubit.</span></span>
<span data-ttu-id="58b53-167">이 비교로 두 비트의 상태를 비교, 액세스, 측정 또는 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-167">The state of the two qubits are not compared, accessed, measured, or modified by this comparison.</span></span>

<span data-ttu-id="58b53-168">반올림 결과 때문 `Double` 에 값에 대 한 같음 비교가 잘못 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-168">Equality comparison for `Double` values may be misleading due to rounding effects.</span></span>
<span data-ttu-id="58b53-169">예를 `49.0 * (1.0/49.0) != 1.0`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-169">For instance, `49.0 * (1.0/49.0) != 1.0`.</span></span>

<span data-ttu-id="58b53-170">두 숫자 식이 지정 된 경우 이항 `>`연산자, `<`, `>=`및 `<=` 를 사용 하 여 첫 번째 식이 두 번째 식 보다 크거나 같고 보다 작거나 같은 경우 true 인 새 부울 식을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-170">Given any two numeric expressions, the binary operators `>`, `<`, `>=`, and `<=` may be used to construct a new Boolean expression that is true if the first expression is respectively greater than, less than, greater than or equal to, or less than or equal to the second expression.</span></span>

<span data-ttu-id="58b53-171">부울 식을 두 개 지정 하는 `and` 경우 `or` 및 이항 연산자를 사용 하 여 두 식 중 하나 (응답 또는 둘 다)가 true 인 경우 true 인 새 부울 식을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-171">Given any two Boolean expressions, the `and` and `or` binary operators may be used to construct a new Boolean expression that is true if both of (resp. either or both of) the two expressions are true.</span></span>

<span data-ttu-id="58b53-172">부울 식이 지정 된 경우 `not` 단항 연산자를 사용 하 여 구성 식이 false 인 경우 true 인 새 부울 식을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-172">Given any Boolean expression, the `not` unary operator may be used to construct a new Boolean expression that is true if the constituent expression is false.</span></span>

## <a name="string-expressions"></a><span data-ttu-id="58b53-173">문자열 식</span><span class="sxs-lookup"><span data-stu-id="58b53-173">String Expressions</span></span>

<span data-ttu-id="58b53-174">Q #에서는 `fail` 문과 `Log` 표준 함수에 문자열을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-174">Q# allows strings to be used in the `fail` statement and the `Log` standard function.</span></span>

<span data-ttu-id="58b53-175">Q #의 문자열은 리터럴 또는 보간된 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-175">Strings in Q# are either literals or interpolated strings.</span></span>
<span data-ttu-id="58b53-176">문자열 리터럴은 대부분의 언어에서 간단한 문자열 리터럴과 유사 `"`합니다. 큰따옴표 안의 유니코드 문자 시퀀스입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-176">String literals are similar to simple string literals in most languages: a sequence of Unicode characters enclosed in double quotes, `"`.</span></span>
<span data-ttu-id="58b53-177">문자열 내 `\` 에서 백슬래시 문자를 사용 하 여 큰따옴표 문자를 이스케이프 하 고 새 줄을로 `\n`, 캐리지 리턴을로 `\r`, 탭을로 삽입할 수 있습니다. `\t`</span><span class="sxs-lookup"><span data-stu-id="58b53-177">Inside of a string, the back-slash character `\` may be used to escape a double quote character, and to insert a new-line as `\n`, a carriage return as `\r`, and a tab as `\t`.</span></span>
<span data-ttu-id="58b53-178">예:</span><span class="sxs-lookup"><span data-stu-id="58b53-178">For instance:</span></span>

```qsharp
"\"Hello world!\", she said.\n"
```

<span data-ttu-id="58b53-179">문자열 보간에 대 한 Q # 구문은 c # 7.0 구문의 하위 집합입니다. Q #에서는 축 자 (여러 줄) 보간된 문자열을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-179">The Q# syntax for string interpolations is a subset of the C# 7.0 syntax; Q# does not support verbatim (multi-line) interpolated strings.</span></span>
<span data-ttu-id="58b53-180">C # 구문에 대 한 [*보간된 문자열*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58b53-180">See [*Interpolated Strings*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) for the C# syntax.</span></span>

<span data-ttu-id="58b53-181">보간된 문자열 내부의 식은 c # 구문이 아니라 Q # 구문을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-181">Expressions inside of an interpolated string follow Q# syntax, not C# syntax.</span></span>
<span data-ttu-id="58b53-182">유효한 Q # 식은 보간된 문자열에 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-182">Any valid Q# expression may appear in an interpolated string.</span></span>

## <a name="qubit-expressions"></a><span data-ttu-id="58b53-183">Bit 식</span><span class="sxs-lookup"><span data-stu-id="58b53-183">Qubit Expressions</span></span>

<span data-ttu-id="58b53-184">유일한 `Qubit` 식은 `Qubit` `Qubit` 배열의 배열 요소 또는 값에 바인딩되는 기호입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-184">The only `Qubit` expressions are symbols that are bound to `Qubit` values or array elements of `Qubit` arrays.</span></span>
<span data-ttu-id="58b53-185">리터럴이 없습니다 `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="58b53-185">There are no `Qubit` literals.</span></span>

## <a name="pauli-expressions"></a><span data-ttu-id="58b53-186">Pauli 식</span><span class="sxs-lookup"><span data-stu-id="58b53-186">Pauli Expressions</span></span>

<span data-ttu-id="58b53-187">,, `Pauli` 및 `PauliZ`의 `PauliI`네 `PauliX`가지 `PauliY`값은 모두 유효한 `Pauli` 식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-187">The four `Pauli` values, `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, are all valid `Pauli` expressions.</span></span>

<span data-ttu-id="58b53-188">그 외에도 유일한 `Pauli` 식은 `Pauli` `Pauli` 배열의 배열 요소 또는 값에 바인딩되는 기호입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-188">Other than that, the only `Pauli` expressions are symbols that are bound to `Pauli` values or array elements of `Pauli` arrays.</span></span>

## <a name="result-expressions"></a><span data-ttu-id="58b53-189">결과 식</span><span class="sxs-lookup"><span data-stu-id="58b53-189">Result Expressions</span></span>

<span data-ttu-id="58b53-190">두 `Result` 값 `One` 및 `Zero`는 유효한 `Result` 식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-190">The two `Result` values, `One` and `Zero`, are valid `Result` expressions.</span></span>

<span data-ttu-id="58b53-191">그 외에도 유일한 `Result` 식은 `Result` `Result` 배열의 배열 요소 또는 값에 바인딩되는 기호입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-191">Other than that, the only `Result` expressions are symbols that are bound to `Result` values or array elements of `Result` arrays.</span></span>
<span data-ttu-id="58b53-192">특히 `One` 는 정수와 `1`동일 하지 않으며 두 요소 사이에 직접 변환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-192">In particular, note that `One` is not the same as the integer `1`, and there is no direct conversion between them.</span></span>
<span data-ttu-id="58b53-193">및 `Zero` `0`의 경우에도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-193">The same is true for `Zero` and `0`.</span></span>

## <a name="range-expressions"></a><span data-ttu-id="58b53-194">범위 식</span><span class="sxs-lookup"><span data-stu-id="58b53-194">Range Expressions</span></span>

<span data-ttu-id="58b53-195">3 개의 `Int` 식 `start` `step`, 및 `stop`가 지정 된 `start .. step .. stop` 경우이 전달 될 때까지 `start` `start+step` `start+step+step` `stop` 첫 번째 요소가이 고, 두 번째 요소가이 고, 세 번째 요소가 인 범위 식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-195">Given any three `Int` expressions `start`, `step`, and `stop`, `start .. step .. stop` is a range expression whose first element is `start`, second element is `start+step`, third element is `start+step+step`, etc., until `stop` is passed.</span></span>
<span data-ttu-id="58b53-196">예를 들어, `step` 가 양수인 경우 범위는 비어 있을 수 있습니다 `stop < start`.</span><span class="sxs-lookup"><span data-stu-id="58b53-196">A range may be empty if, for instance, `step` is positive and `stop < start`.</span></span>
<span data-ttu-id="58b53-197">범위의 `stop` 마지막 요소는 `start` 와 `stop` 의 차이가의 `step`정수 배수가 면가 됩니다. 즉, 범위는 양쪽 끝에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-197">The last element of the range will be `stop` if the difference between `start` and `stop` is an integral multiple of `step`; that is, the range is inclusive at both ends.</span></span>

<span data-ttu-id="58b53-198">`Int` 두 `start` 식 `stop`및 `start .. stop` 가 지정 된 경우는와 같은 범위 식입니다. `start .. 1 .. stop`</span><span class="sxs-lookup"><span data-stu-id="58b53-198">Given any two `Int` expressions `start` and `stop`, `start .. stop` is a range expression that is equal to `start .. 1 .. stop`.</span></span>
<span data-ttu-id="58b53-199">가 보다 `start`작은 경우 `step` `stop` 에도 암시는 + 1입니다. 이 경우 범위는 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-199">Note that the implied `step` is +1 even if `stop` is less than `start`; in such a case, the range is empty.</span></span>

<span data-ttu-id="58b53-200">몇 가지 예제 범위는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-200">Some example ranges are:</span></span>

- <span data-ttu-id="58b53-201">`1..3`은 1, 2, 3의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-201">`1..3` is the range 1, 2, 3.</span></span>
- <span data-ttu-id="58b53-202">`2..2..5`는 범위 2, 4입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-202">`2..2..5` is the range 2, 4.</span></span>
- <span data-ttu-id="58b53-203">`2..2..6`는 2, 4, 6 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-203">`2..2..6` is the range 2, 4, 6.</span></span>
- <span data-ttu-id="58b53-204">`6..-2..2`는 6, 4, 2 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-204">`6..-2..2` is the range 6, 4, 2.</span></span>
- <span data-ttu-id="58b53-205">`2..1`는 빈 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-205">`2..1` is the empty range.</span></span>
- <span data-ttu-id="58b53-206">`2..6..7`는 범위 2입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-206">`2..6..7` is the range 2.</span></span>
- <span data-ttu-id="58b53-207">`2..2..1`는 빈 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-207">`2..2..1` is the empty range.</span></span>
- <span data-ttu-id="58b53-208">`1..-1..2`는 빈 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-208">`1..-1..2` is the empty range.</span></span>

## <a name="callable-expressions"></a><span data-ttu-id="58b53-209">호출 가능 식</span><span class="sxs-lookup"><span data-stu-id="58b53-209">Callable Expressions</span></span>

<span data-ttu-id="58b53-210">호출 가능 리터럴은 컴파일 범위에서 정의 된 작업 또는 함수의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-210">A callable literal is the name of an operation or function defined in the compilation scope.</span></span>
<span data-ttu-id="58b53-211">예를 들어 `X` 는 표준 라이브러리 `X` 작업 `Message` 을 참조 하는 작업 리터럴이어야,는 표준 라이브러리 `Message` 함수를 참조 하는 함수 리터럴입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-211">For instance, `X` is an operation literal that refers to the standard library `X` operation, and `Message` is a function literal that refers to the standard library `Message` function.</span></span>

<span data-ttu-id="58b53-212">작업에서 `Adjoint` 함수를 지 원하는 경우 `Adjoint op` 는 연산 식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-212">If an operation supports the `Adjoint` functor, then `Adjoint op` is an operation expression.</span></span>
<span data-ttu-id="58b53-213">마찬가지로 작업에서 `Controlled` 함수를 지 원하는 경우 `Controlled op` 는 연산 식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-213">Similarly, if the operation supports the `Controlled` functor, then `Controlled op` is an operation expression.</span></span>
<span data-ttu-id="58b53-214">이러한 식의 형식은 [함수](xref:microsoft.quantum.language.type-model#functors)에서 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-214">The types of these expressions are specified in [Functors](xref:microsoft.quantum.language.type-model#functors).</span></span>

<span data-ttu-id="58b53-215">함수 (`Adjoint` 및 `Controlled`)는를 사용 하 여 `!` `[]`래핑 해제 연산자와 배열 인덱싱을 제외 하 고 다른 모든 연산자 보다 더 가깝게 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-215">Functors (`Adjoint` and `Controlled`) bind more closely than all other operators, except for the unwrap operator `!` and array indexing with `[]`.</span></span>
<span data-ttu-id="58b53-216">따라서 다음은 작업에서 사용 되는 함수를 지원 한다고 가정 하 여 모든 법률입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-216">Thus, the following are all legal, assuming that the operations support the functors used:</span></span>

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

<span data-ttu-id="58b53-217">호출 가능 리터럴은 값으로 사용 될 수 있습니다. 예를 들어 변수에 할당 하거나 다른 호출 가능으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-217">A callable literal may be used as a value, say to assign to a variable or to pass to another callable.</span></span>
<span data-ttu-id="58b53-218">이 경우 호출 가능에 형식 매개 변수가 있으면 해당 매개 변수를 호출 가능 값의 일부로 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-218">In this case, if the callable has type parameters, they must be provided as part of the callable value.</span></span>
<span data-ttu-id="58b53-219">호출 가능 값은 지정 되지 않은 형식 매개 변수를 가질 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-219">A callable value cannot have any unspecified type parameters.</span></span>

<span data-ttu-id="58b53-220">예를 들어가 `Fun` 시그니처 `'T1->Unit`를 사용 하는 함수인 경우는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-220">For instance, if `Fun` is a function with signature `'T1->Unit`:</span></span>

```qsharp
let f = Fun<Int>;            // f is Int->Unit.
SomeOtherFun(Fun<Double>);   // A Double->Unit is passed to SomeOtherFun.
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a><span data-ttu-id="58b53-221">호출 가능 호출 식</span><span class="sxs-lookup"><span data-stu-id="58b53-221">Callable Invocation Expressions</span></span>

<span data-ttu-id="58b53-222">호출 가능 식의 입력 형식에 대 한 호출 가능 (연산 또는 함수) 식과 튜플 식이 지정 된 경우 호출 식은 튜플 식을 호출 가능 식에 추가 하 여 구성 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-222">Given a callable (operation or function) expression and a tuple expression of the input type of the callable's signature, an invocation expression may be formed by appending the tuple expression to the callable expression.</span></span>
<span data-ttu-id="58b53-223">호출 식의 형식은 호출 가능 시그니처의 출력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-223">The type of the invocation expression is the output type of the callable's signature.</span></span>

<span data-ttu-id="58b53-224">예를 들어가 `Op` 서명이 `((Int, Qubit) => Double)`포함 된 작업 인 경우 `Op(3, qubit1)` 는 형식의 `Double`식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-224">For example, if `Op` is an operation with signature `((Int, Qubit) => Double)`, `Op(3, qubit1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="58b53-225">마찬가지로가 시그니처 `Sin` `(Double -> Double)`를 사용 하는 함수인 경우 `Sin(0.1)` 는 형식의 `Double`식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-225">Similarly, if `Sin` is a function with signature `(Double -> Double)`, `Sin(0.1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="58b53-226">마지막으로가 `Builder` 시그니처 `(Int -> (Int -> Int))`를 사용 하는 함수인 경우 `Builder(3)` 는에서 Int로의 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-226">Finally, if `Builder` is a function with signature `(Int -> (Int -> Int))`, then `Builder(3)` is a function from Into to Int.</span></span>

<span data-ttu-id="58b53-227">호출 가능 값 식의 결과를 호출 하려면 호출 가능 식 주위에 괄호 쌍을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-227">Invoking the result of a callable-valued expression requires an extra pair of parentheses around the callable expression.</span></span>
<span data-ttu-id="58b53-228">따라서 이전 단락에서 호출 `Builder` 결과를 호출 하려면 올바른 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-228">Thus, to invoke the result of calling `Builder` from the previous paragraph, the correct syntax is:</span></span>

```qsharp
(Builder(3))(2)
```

<span data-ttu-id="58b53-229">형식 매개 변수가 있는 호출 가능를 호출할 때 실제 형식 매개 변수는 꺾쇠 괄호 `<` 내에서 호출 `>` 가능 식 뒤에 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-229">When invoking a type-parameterized callable, the actual type parameters may be specified within angle brackets `<` and `>` after the callable expression.</span></span>
<span data-ttu-id="58b53-230">이는 일반적으로 Q # 컴파일러가 실제 형식을 유추 하므로 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-230">This is usually unnecessary as the Q# compiler will infer the actual types.</span></span>
<span data-ttu-id="58b53-231">형식 매개 변수가 있는 인수가 지정 되지 않은 상태로 남아 있는 경우 부분 응용 프로그램에 필요 합니다 (아래 참조).</span><span class="sxs-lookup"><span data-stu-id="58b53-231">It is required for partial application (see below) if a type-parameterized argument is left unspecified.</span></span>
<span data-ttu-id="58b53-232">또한 다른 함수를 사용 하는 작업을 호출할 수 있는 경우에도 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-232">It is also sometimes useful when passing operations with different functor supports to a callable.</span></span>

<span data-ttu-id="58b53-233">예를 들어, `Func` 에 시그니처가 `('T1, 'T2, 'T1) -> 'T2`있고 `Op1` , `Op2` 에 시그니처가 `(Qubit[] => Unit is Adj)`있고, `Op3` 가 첫 `(Qubit[] => Unit)`번째 인수로를 `Func` 사용 `Op1` 하 여를 호출 하 `Op2` 고,를 세 번째 `Op3` 인수로 호출 하는 시그니처가 있는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-233">For instance, if `Func` has signature `('T1, 'T2, 'T1) -> 'T2`, `Op1` and `Op2` have signature `(Qubit[] => Unit is Adj)`, and `Op3` has signature `(Qubit[] => Unit)`, to invoke `Func` with `Op1` as the first argument, `Op2` as the second, and `Op3` as the third:</span></span>

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

<span data-ttu-id="58b53-234">및 `Op3` `Op1` 에 다른 형식이 있으므로 형식 사양이 필요 합니다. 따라서 컴파일러는 사양을 사용 하지 않고이를 모호 하 게 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-234">The type specification is required because `Op3` and `Op1` have different types, so the compiler will treat this as ambiguous without the specification.</span></span>

### <a name="partial-application"></a><span data-ttu-id="58b53-235">부분 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="58b53-235">Partial Application</span></span>

<span data-ttu-id="58b53-236">호출 가능 식이 지정 된 경우 호출 가능에 인수의 하위 집합을 제공 하 여 새 호출 가능을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-236">Given a callable expression, a new callable may be created by providing a subset of the arguments to the callable.</span></span>
<span data-ttu-id="58b53-237">이를 _부분 응용 프로그램_이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-237">This is called _partial application_.</span></span>

<span data-ttu-id="58b53-238">Q #에서 부분적으로 적용 되는 호출 가능 인수에는 밑줄 ( `_`)을 사용 하 여 일반 호출 식을 작성 하는 방법으로 표현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-238">In Q#, a partially applied callable is expressed by writing a normal invocation expression, but using an underscore, `_`, for the unspecified arguments.</span></span>
<span data-ttu-id="58b53-239">결과로 생성 되는 호출 가능의 결과 형식은 기본 호출 가능 및 작업에 대 한 동일한 특수화와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-239">The resulting callable has the same result type as the base callable, and the same specializations for operations.</span></span>
<span data-ttu-id="58b53-240">부분 응용 프로그램의 입력 형식은 단순히 지정 된 인수가 제거 된 원래 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-240">The input type of the partial application is simply the original type with the specified arguments removed.</span></span>

<span data-ttu-id="58b53-241">부분 응용 프로그램을 만들 때 변경 가능한 변수가 지정 된 인수로 전달 되 면 변수의 현재 값이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-241">If a mutable variable is passed as a specified argument when creating a partial application, the current value of the variable is used.</span></span>
<span data-ttu-id="58b53-242">나중에 변수 값을 변경 해도 부분 응용 프로그램에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-242">Changing the value of the variable afterward will not impact the partial application.</span></span>

<span data-ttu-id="58b53-243">예를 들어, `Op` 의 형식은 `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-243">For example, if `Op` has type `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`:</span></span>

- <span data-ttu-id="58b53-244">`Op(5,(_,_))`에는 `(((Qubit,Qubit), Double) => Unit is Adj)`형식, 등이 `Op(5,_)`있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-244">`Op(5,(_,_))` has type `(((Qubit,Qubit), Double) => Unit is Adj)`, and so has `Op(5,_)`.</span></span>
- <span data-ttu-id="58b53-245">`Op(_,(_,1.0))`의 형식은 `((Int, (Qubit,Qubit)) => Unit is Adj)`입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-245">`Op(_,(_,1.0))` has type `((Int, (Qubit,Qubit)) => Unit is Adj)`.</span></span>
- <span data-ttu-id="58b53-246">`Op(_,((q1,q2),_))`의 형식은 `((Int,Double) => Unit is Adj)`입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-246">`Op(_,((q1,q2),_))` has type `((Int,Double) => Unit is Adj)`.</span></span>
   <span data-ttu-id="58b53-247">여기서는 단일 튜플 동등성을 적용 했습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-247">Note that we have applied singleton tuple equivalence here.</span></span>

<span data-ttu-id="58b53-248">부분적으로 적용 되는 호출 가능에서 컴파일러가 유추할 수 없는 형식 매개 변수를 포함 하는 경우 호출 사이트에서 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-248">If the partially-applied callable has type parameters that cannot be inferred by the compiler, they must be provided at the invocation site.</span></span>
<span data-ttu-id="58b53-249">부분 응용 프로그램에는 지정 되지 않은 형식 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-249">The partial application cannot have any unspecified type parameters.</span></span>

<span data-ttu-id="58b53-250">예를 들어, `Op` 의 형식은 `(('T1, Qubit, 'T1) => Unit : Adjoint)`다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-250">For example, if `Op` has type `(('T1, Qubit, 'T1) => Unit : Adjoint)`:</span></span>

```qsharp
let f1 = Op<Int>(_, qb, _); // f1 has type ((Int,Int) => Unit is Adj)
let f2 = Op(5, qb, _);      // f2 has type (Int => Unit is Adj)
let f3 = Op(_,qb, _);       // f3 generates a compilation error
```

### <a name="recursion"></a><span data-ttu-id="58b53-251">재귀</span><span class="sxs-lookup"><span data-stu-id="58b53-251">Recursion</span></span>

<span data-ttu-id="58b53-252">Q # callables은 직접 또는 간접적으로 재귀적으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-252">Q# callables are allowed to be directly or indirectly recursive.</span></span>
<span data-ttu-id="58b53-253">즉, 작업 또는 함수가 자신을 호출 하거나 호출 가능 작업을 직접 또는 간접적으로 호출 하는 다른 호출 가능 함수를 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-253">That is, an operation or function may call itself, or it may call another callable that directly or indirectly calls the callable operation.</span></span>

<span data-ttu-id="58b53-254">그러나 재귀 사용에 대 한 두 가지 중요 한 설명은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-254">There are two important comments about the use of recursion, however:</span></span>

- <span data-ttu-id="58b53-255">작업에서 재귀를 사용 하면 특정 최적화에 방해가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-255">The use of recursion in operations is likely to interfere with certain optimizations.</span></span>
  <span data-ttu-id="58b53-256">이는 알고리즘의 실행 시간에 상당한 영향을 미칠 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-256">This may have a substantial impact on the execution time of the algorithm.</span></span>
- <span data-ttu-id="58b53-257">실제 퀀텀 장치에서 실행 되는 경우 스택 공간이 제한 될 수 있으므로, 심층 재귀가 런타임 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-257">When executing on an actual quantum device, stack space may be limited, and so deep recursion may lead to a runtime error.</span></span>
  <span data-ttu-id="58b53-258">특히 Q # 컴파일러 및 런타임에서는 마무리 재귀를 식별 하 고 최적화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-258">In particular, the Q# compiler and runtime do not identify and optimize tail recursion.</span></span>

## <a name="tuple-expressions"></a><span data-ttu-id="58b53-259">튜플 식</span><span class="sxs-lookup"><span data-stu-id="58b53-259">Tuple Expressions</span></span>

<span data-ttu-id="58b53-260">튜플 리터럴은 `(` 및 `)`로 묶인 적절 한 형식의 요소 식 시퀀스로, 쉼표로 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-260">A tuple literal is a sequence of element expressions of the appropriate type, separated by commas, enclosed in `(` and `)`.</span></span>
<span data-ttu-id="58b53-261">예를 들어 `(1, One)` 은 `(Int, Result)` 식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-261">For instance, `(1, One)` is an `(Int, Result)` expression.</span></span>

<span data-ttu-id="58b53-262">리터럴 이외의 튜플 식은 튜플 값에 바인딩된 기호, 튜플 배열의 배열 요소 및 튜플을 반환 하는 호출 가능 호출입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-262">Other than literals, the only tuple expressions are symbols that are bound to tuple values, array elements of tuple arrays, and callable invocations that return tuples.</span></span>

## <a name="user-defined-type-expressions"></a><span data-ttu-id="58b53-263">사용자 정의 형식 식</span><span class="sxs-lookup"><span data-stu-id="58b53-263">User-Defined Type Expressions</span></span>

<span data-ttu-id="58b53-264">사용자 정의 형식의 리터럴은 형식 이름과 해당 형식의 기본 튜플 형식의 튜플 리터럴로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-264">A literal of a user-defined type consists of the type name followed by a tuple literal of the type’s base tuple type.</span></span>
<span data-ttu-id="58b53-265">예를 들어, `IntPair` 가를 기반으로 `(Int, Int)` `IntPair(2,3)` 하는 사용자 정의 형식인 경우는 해당 형식의 유효한 리터럴입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-265">For instance, if `IntPair` is a user-defined type based on `(Int, Int)`, then `IntPair(2,3)` would be a valid literal of that type.</span></span>

<span data-ttu-id="58b53-266">리터럴 외에 사용자 정의 형식의 유일한 식은 해당 형식의 값에 바인딩된 기호, 해당 형식의 배열 요소, 해당 형식을 반환 하는 호출 가능 호출입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-266">Other than literals, the only expressions of a user-defined type are symbols that are bound to values of that type, array elements of arrays of that type, and callable invocations that return that type.</span></span>

## <a name="unwrap-expressions"></a><span data-ttu-id="58b53-267">래핑 해제 식</span><span class="sxs-lookup"><span data-stu-id="58b53-267">Unwrap Expressions</span></span>

<span data-ttu-id="58b53-268">Q #에서 래핑 해제 연산자는 후행 감탄 부호 `!`입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-268">In Q#, the unwrap operator is a trailing exclamation mark `!`.</span></span>
<span data-ttu-id="58b53-269">예를 들어, `IntPair` 가 기본 형식의 `(Int, Int)`사용자 정의 형식이 고 `s` 값 `IntPair(2,3)` `s!` 이 인 변수인 경우는 `(2,3)`입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-269">For instance, if `IntPair` is a user-defined type with underlying type `(Int, Int)`, and `s` was a variable with value `IntPair(2,3)`, then `s!` would be `(2,3)`.</span></span>

<span data-ttu-id="58b53-270">사용자 정의 형식에 대해 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-270">For user-defined types defined in terms of other user-defined types.</span></span> <span data-ttu-id="58b53-271">래핑 해제 연산자는 반복 될 수 있습니다. 예를 `s!!` 들어는 이중 래핑 해제 된 값을 `s`나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-271">the unwrap operator may be repeated; for instance, `s!!` indicates the doubly-unwrapped value of `s`.</span></span>
<span data-ttu-id="58b53-272">따라서가 기본 `WrappedPair` `IntPair`형식의 사용자 `t` 정의 형식이 고가 값 `WrappedPair(IntPair(1,2))` `t!!` 이 포함 된 변수인 경우은 `(1,2)`입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-272">Thus, if `WrappedPair` is a user-defined type with underlying type `IntPair`, and `t` is a variable with value `WrappedPair(IntPair(1,2))`, then `t!!` would be `(1,2)`.</span></span>

<span data-ttu-id="58b53-273">연산자 `!` 는 배열 인덱싱 및 조각화를 위해 이외의 `[]` 다른 모든 연산자 보다 우선 순위가 높습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-273">The `!` operator has higher precedence than all other operators other than `[]` for array indexing and slicing.</span></span>
<span data-ttu-id="58b53-274">`!`및 `[]` bind 메서드에 액세스할; 즉, `a[i]![3]` 는의 `((a[i])!)[3]` `i` `a`' 번째 요소를 가져와 래핑 해제 한 다음 래핑 해제 된 값 (배열 이어야 함)의 세 번째 요소를 가져오기로 읽어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-274">`!` and `[]` bind positionally; that is, `a[i]![3]` should be read as `((a[i])!)[3]`: take the `i`'th element of `a`, unwrap it, and then get the 3rd element of the unwrapped value (which must be an array).</span></span>

<span data-ttu-id="58b53-275">`!` 연산자의 우선 순위에는 명확 하지 않을 수 있는 영향이 하나 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-275">The precedence of the `!` operator has one impact that might not be obvious.</span></span>
<span data-ttu-id="58b53-276">함수 또는 작업에서 래핑 해제 되는 값을 반환 하는 경우 인수 튜플이 래핑 되지 않고 호출에 바인딩되도록 함수 또는 작업 호출을 괄호로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-276">If a function or operation returns a value that then gets unwrapped, the function or operation call must be enclosed in parentheses so that the argument tuple binds to the call rather than to the unwrap.</span></span>
<span data-ttu-id="58b53-277">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="58b53-277">For example:</span></span>

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a><span data-ttu-id="58b53-278">배열 식</span><span class="sxs-lookup"><span data-stu-id="58b53-278">Array Expressions</span></span>

<span data-ttu-id="58b53-279">배열 리터럴은 `[` 및 `]`로 묶인 하나 이상의 요소 식의 시퀀스로, 쉼표로 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-279">An array literal is a sequence of one or more element expressions, separated by commas, enclosed in `[` and `]`.</span></span>
<span data-ttu-id="58b53-280">모든 요소는 동일한 형식과 호환 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-280">All elements must be compatible with the same type.</span></span>

<span data-ttu-id="58b53-281">공통 요소 형식이 작업 또는 함수 형식이 면 모든 요소에 동일한 입력 및 출력 형식이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-281">If the common element type is an operation or function type, all of the elements must have the same input and output types.</span></span>
<span data-ttu-id="58b53-282">배열의 요소 형식은 모든 요소에서 지원 되는 모든 함수을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-282">The element type of the array will support any functors that are supported by all of the elements.</span></span>
<span data-ttu-id="58b53-283">`Op1`예 `Op2` `Op3` 를 들어, 및 모두가 `Qubit[] => Unit`이지만,를 `Op1` 지원 `Adjoint` `Op2` `Controlled`하 고를 지원 하며 `Op3` 를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-283">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[] => Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="58b53-284">`[Op1, Op2]`는 작업의 `(Qubit[] => Unit)` 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-284">`[Op1, Op2]` is an array of `(Qubit[] => Unit)` operations.</span></span>
- <span data-ttu-id="58b53-285">`[Op1, Op3]`는 작업의 `(Qubit[] => Unit is Adj)` 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-285">`[Op1, Op3]` is an array of `(Qubit[] => Unit is Adj)` operations.</span></span>
- <span data-ttu-id="58b53-286">`[Op2, Op3]`는 작업의 `(Qubit[] => Unit is Ctl)` 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-286">`[Op2, Op3]` is an array of `(Qubit[] => Unit is Ctl)` operations.</span></span>

<span data-ttu-id="58b53-287">빈 배열 리터럴 `[]`는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-287">Empty array literals, `[]`, are not allowed.</span></span>
<span data-ttu-id="58b53-288">대신를 `new ★[0]`사용 하 `★` 는 대신를 사용 합니다. 여기서은 적절 한 형식에 대 한 자리 표시자입니다 .를 사용 하면 원하는 길이 0 배열을 만들 수 있습니다</span><span class="sxs-lookup"><span data-stu-id="58b53-288">Instead using `new ★[0]`, where `★` is as placeholder for a suitable type, allows to create the desired array of length zero.</span></span>

<span data-ttu-id="58b53-289">동일한 형식의 두 배열이 지정 된 경우 이항 `+` 연산자를 사용 하 여 두 배열의 연결 인 새 배열을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-289">Given two arrays of the same type, the binary `+` operator may be used to form a new array that is the concatenation of the two arrays.</span></span>
<span data-ttu-id="58b53-290">예를 `[1,2,3] + [4,5,6]` 들어은 `[1,2,3,4,5,6]`입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-290">For instance, `[1,2,3] + [4,5,6]` is `[1,2,3,4,5,6]`.</span></span>

### <a name="array-creation"></a><span data-ttu-id="58b53-291">배열 만들기</span><span class="sxs-lookup"><span data-stu-id="58b53-291">Array Creation</span></span>

<span data-ttu-id="58b53-292">형식 및 `Int` 식이 지정 된 경우 연산자를 `new` 사용 하 여 지정 된 크기의 새 배열을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-292">Given a type and an `Int` expression, the `new` operator may be used to allocate a new array of the given size.</span></span>
<span data-ttu-id="58b53-293">예를 `new Int[i+1]` 들어는 `Int` `i+1` 요소로 새 배열을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-293">For instance, `new Int[i+1]` would allocate a new `Int` array with `i+1` elements.</span></span>

<span data-ttu-id="58b53-294">새 배열의 요소는 형식 종속 기본값으로 초기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-294">The elements of a new array are initialized to a type-dependent default value.</span></span>
<span data-ttu-id="58b53-295">대부분의 경우이 값은 0으로 변형 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-295">In most cases this is some variation of zero.</span></span>

<span data-ttu-id="58b53-296">엔터티를 참조 하는 callables 및 callables의 경우 적절 한 기본값이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-296">For qubits and callables, which are references to entities, there is no reasonable default value.</span></span>
<span data-ttu-id="58b53-297">따라서 이러한 형식의 경우 기본값은 런타임 오류를 발생 시 키 지 않고 사용할 수 없는 잘못 된 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-297">Thus, for these types, the default is an invalid reference that cannot be used without causing a runtime error.</span></span>
<span data-ttu-id="58b53-298">이는 c #, Java 등의 언어에서 null 참조와 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-298">This is similar to a null reference in languages such as C# or Java.</span></span>
<span data-ttu-id="58b53-299">요소가 안전 하 게 사용 되기 전에는 기본값이 아닌 값을 사용 하 여 valbits 또는 callables을 포함 하는 배열을 적절 하 게 초기화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-299">Arrays containing qubits or callables must be properly initialized with non-default values before their elements may be safely used.</span></span> <span data-ttu-id="58b53-300">적절 한 초기화 루틴은에서 <xref:microsoft.quantum.arrays>찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-300">Suitable initialization routines can be found in <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="58b53-301">각 형식에 대 한 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-301">The default values for each type are:</span></span>

<span data-ttu-id="58b53-302">Type</span><span class="sxs-lookup"><span data-stu-id="58b53-302">Type</span></span> | <span data-ttu-id="58b53-303">기본값</span><span class="sxs-lookup"><span data-stu-id="58b53-303">Default</span></span>
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | <span data-ttu-id="58b53-304">_invalid qubit_</span><span class="sxs-lookup"><span data-stu-id="58b53-304">_invalid qubit_</span></span>
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | <span data-ttu-id="58b53-305">빈 범위`1..1..0`</span><span class="sxs-lookup"><span data-stu-id="58b53-305">The empty range, `1..1..0`</span></span>
 `Callable` | <span data-ttu-id="58b53-306">_invalid callable_</span><span class="sxs-lookup"><span data-stu-id="58b53-306">_invalid callable_</span></span>
 `Array['T]` | `'T[0]`

<span data-ttu-id="58b53-307">튜플 형식은 요소에 의해 초기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-307">Tuple types are initialized element-by-element.</span></span>


### <a name="jagged-arrays"></a><span data-ttu-id="58b53-308">가변 배열</span><span class="sxs-lookup"><span data-stu-id="58b53-308">Jagged Arrays</span></span>

<span data-ttu-id="58b53-309">"배열의 배열"이 라고도 하는 가변 배열은 요소가 배열인 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-309">A jagged array, sometimes called an "array of arrays", is an array whose elements are arrays.</span></span> <span data-ttu-id="58b53-310">가변 배열의 요소는 크기가 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-310">The elements of a jagged array can be of different sizes.</span></span> <span data-ttu-id="58b53-311">다음 예에서는 곱하기 테이블을 나타내는 가변 배열을 선언 하 고 초기화 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-311">The following example shows how to declare and initialize a jagged array representing a multiplication table.</span></span>

```qsharp
let N = 4;
mutable multiplicationTable = new Int[][N];
for (i in 1..N) {

    mutable row = new Int[i];
    for (j in 1..i) {
        set row w/= j-1 <- i * j;
    }
    set multiplicationTable w/= i-1 <- row;
}
```


### <a name="array-slices"></a><span data-ttu-id="58b53-312">배열 조각</span><span class="sxs-lookup"><span data-stu-id="58b53-312">Array Slices</span></span>

<span data-ttu-id="58b53-313">배열 식과 `Range` 식이 지정 된 경우 `[` 및 `]` 배열 조각 연산자를 사용 하 여 새 식을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-313">Given an array expression and a `Range` expression, a new expression may be formed using the `[` and `]` array slice operator.</span></span>
<span data-ttu-id="58b53-314">새 식은 배열과 동일한 형식이 되며의 `Range`요소에 의해 인덱싱된 배열 항목이에 `Range`정의 된 순서 대로 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-314">The new expression will be the same type as the array and will contain the array items indexed by the elements of the `Range`, in the order defined by the `Range`.</span></span>
<span data-ttu-id="58b53-315">예를 들어, `a` `Double`가 s의 배열에 바인딩된 경우는의 `a[3..-1..0]` `Double[]` `a` 처음 4 개 요소를 포함 하지만에 `a`표시 되는 역순으로를 포함 하는 식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-315">For instance, if `a` is bound to an array of `Double`s, then `a[3..-1..0]` is a `Double[]` expression that contains the first four elements of `a` but in the reverse order as they appear in `a`.</span></span>

<span data-ttu-id="58b53-316">`Range` 이 비어 있으면 결과 배열 조각의 길이가 0이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-316">If the `Range` is empty, then the resulting array slice will be zero length.</span></span>

<span data-ttu-id="58b53-317">배열 식이 단순 식별자가 아니면 조각화 하기 위해 괄호로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-317">If the array expression is not a simple identifier, it must be enclosed it parentheses in order to slice.</span></span>
<span data-ttu-id="58b53-318">예를 들어 및 `a` `b` 가 모두 s의 `Int`배열인 경우 연결의 조각이 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-318">For instance, if `a` and `b` are both arrays of `Int`s, a slice from the concatenation would be expressed as:</span></span>

```qsharp
(a+b)[1..2..7]
```

<span data-ttu-id="58b53-319">Q #의 모든 배열은 0부터 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-319">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="58b53-320">즉, 배열의 `a` 첫 번째 요소는 항상 `a[0]`입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-320">That is, the first element of an array `a` is always `a[0]`.</span></span>

<span data-ttu-id="58b53-321">0.8 릴리스부터는 범위 조각화를 위한 상황별 식을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-321">Starting with our 0.8 release, we support contextual expressions for range slicing.</span></span> <span data-ttu-id="58b53-322">특히 범위 분할 식의 컨텍스트에서는 범위 시작 값과 끝 값을 생략할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-322">In particular, range start and end values may be omitted in the context of a range slicing expression.</span></span> <span data-ttu-id="58b53-323">이 경우 컴파일러는 범위에 대해 의도 된 구분 기호를 유추 하기 위해 다음 규칙을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-323">In that case, the compiler will apply the following rules to infer the intended delimiters for the range.</span></span> 

<span data-ttu-id="58b53-324">예를 들어 range start 값을 생략 하면 유추 된 시작 값이</span><span class="sxs-lookup"><span data-stu-id="58b53-324">For example, if the range start value is omitted, then the inferred start value</span></span> 
- <span data-ttu-id="58b53-325">지정 된 단계가 없거나 지정 된 단계가 양수 이면 0이 고, 그렇지 않으면입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-325">is zero if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="58b53-326">지정 된 단계가 음수인 경우 분리 된 배열의 길이에서 1을 뺀 값입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-326">is the length of sliced array minus one if the specified step is negative.</span></span> 

<span data-ttu-id="58b53-327">범위 끝 값이 생략 된 경우에는 유추 된 끝 값이</span><span class="sxs-lookup"><span data-stu-id="58b53-327">If the range end value is omitted, then the inferred end value</span></span> 
- <span data-ttu-id="58b53-328">지정 된 단계가 없고 지정 된 단계가 양수인 경우 분리 된 배열의 길이가 1을 뺀 값입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-328">is the length of sliced array minus one if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="58b53-329">지정 된 단계가 음수 이면 0이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-329">is zero if the specified step is negative.</span></span> 

```qsharp
let arr = [1,2,3,4,5,6];
let slice1  = arr[3...];      // slice1 is [4,5,6];
let slice2  = arr[0..2...];   // slice2 is [1,3,5];
let slice3  = arr[...2];      // slice3 is [1,2,3];
let slice4  = arr[...2..3];   // slice4 is [1,3];
let slice5  = arr[...2...];   // slice5 is [1,3,5];
let slice7  = arr[4..-2...];  // slice7 is [5,3,1];
let slice8  = arr[...-1..3];  // slice8 is [6,5,4];
let slice9  = arr[...-1...];  // slice9 is [6,5,4,3,2,1];
let slice10 = arr[...];       // slice10 is [1,2,3,4,5,6];
```

## <a name="array-element-expressions"></a><span data-ttu-id="58b53-330">배열 요소 식</span><span class="sxs-lookup"><span data-stu-id="58b53-330">Array Element Expressions</span></span>

<span data-ttu-id="58b53-331">배열 식과 `Int` 식이 지정 된 경우 `[` 및 `]` 배열 요소 연산자를 사용 하 여 새 식을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-331">Given an array expression and an `Int` expression, a new expression may be formed using the `[` and `]` array element operator.</span></span>
<span data-ttu-id="58b53-332">새 식은 배열의 요소 형식과 동일한 형식이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-332">The new expression will be the same type as the element type of the array.</span></span>
<span data-ttu-id="58b53-333">예를 들어, `a` 가 s `Double` `a[4]` 의 배열에 바인딩되면은 `Double` 식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-333">For instance, if `a` is bound to an array of `Double`s, then `a[4]` is a `Double` expression.</span></span>

<span data-ttu-id="58b53-334">배열 식이 단순 식별자가 아닌 경우 요소를 선택 하기 위해 괄호로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-334">If the array expression is not a simple identifier, it must be enclosed it parentheses in order to select an element.</span></span>
<span data-ttu-id="58b53-335">예를 들어 및 `a` `b` 가 모두 s의 `Int`배열인 경우 연결의 요소가 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-335">For instance, if `a` and `b` are both arrays of `Int`s, an element from the concatenation would be expressed as:</span></span>

```qsharp
(a+b)[13]
```

<span data-ttu-id="58b53-336">Q #의 모든 배열은 0부터 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-336">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="58b53-337">즉, 배열의 `a` 첫 번째 요소는 항상 `a[0]`입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-337">That is, the first element of an array `a` is always `a[0]`.</span></span>


## <a name="copy-and-update-expressions"></a><span data-ttu-id="58b53-338">복사 및 업데이트 식</span><span class="sxs-lookup"><span data-stu-id="58b53-338">Copy-and-Update Expressions</span></span>

<span data-ttu-id="58b53-339">기존 배열에서 복사 및 업데이트 식을 통해 새 배열을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-339">New arrays can be created from existing ones via copy-and-update expressions.</span></span>
<span data-ttu-id="58b53-340">복사 및 `expression1 w/ expression2 <- expression3`업데이트 식은 형식의 식이 며, 여기서 `expression1` 은 특정 형식의 `T[]` `T`형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-340">A copy-and-update expression is an expression of the form `expression1 w/ expression2 <- expression3`, where `expression1` has to be of type `T[]` for some type `T`.</span></span> <span data-ttu-id="58b53-341">두 번째 `expression2` 는에서 `expression1` 배열과 비교 하 여 수정할 요소의 인덱스를 정의 하 고, 형식 `Int` 또는 형식 중 하나 여야 `Range`합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-341">The second `expression2` defines the indices of the element(s) to modify compared to the array in `expression1` and has to be either of type `Int` or of type `Range`.</span></span> <span data-ttu-id="58b53-342">가 `expression2` 형식이 `Int` `expression3` 면은 형식 `T`이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-342">If `expression2` is of type `Int`, `expression3` has to be of type `T`.</span></span> <span data-ttu-id="58b53-343">가 `expression2` 형식이 `Range` `expression3` 면은 형식 `T[]`이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-343">If `expression2` is of type `Range`, `expression3` has to be of type `T[]`.</span></span>

<span data-ttu-id="58b53-344">`arr w/ idx <- value` 복사 및 업데이트 식은의 해당 요소로 설정 된 모든 요소를 포함 하는 새 배열을 생성 합니다. `arr`이 요소는의 요소 `idx`를 제외 하 고는의 `value`해당 요소로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-344">A copy-and-update expression `arr w/ idx <- value` constructs a new array with all elements set to the corresponding element in `arr`, except for the element(s) at `idx`, which are set to the one(s) in `value`.</span></span> <span data-ttu-id="58b53-345">예를 들어에 `arr` 배열이 `[0,1,2,3]`포함 된 경우</span><span class="sxs-lookup"><span data-stu-id="58b53-345">For example, if `arr` contains an array `[0,1,2,3]`, then</span></span> 
- <span data-ttu-id="58b53-346">`arr w/ 0 <- 10`는 배열 `[10,1,2,3]`입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-346">`arr w/ 0 <- 10` is the array `[10,1,2,3]`.</span></span>
- <span data-ttu-id="58b53-347">`arr w/ 2 <- 10`는 배열 `[0,1,10,3]`입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-347">`arr w/ 2 <- 10` is the array `[0,1,10,3]`.</span></span>
- <span data-ttu-id="58b53-348">`arr w/ 0..2..3 <- [10,12]`는 배열 `[10,1,12,3]`입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-348">`arr w/ 0..2..3 <- [10,12]` is the array `[10,1,12,3]`.</span></span>

<span data-ttu-id="58b53-349">사용자 정의 형식에 명명 된 항목에 대 한 유사한 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-349">Similar expressions exist for named items in user-defined types.</span></span> <span data-ttu-id="58b53-350">예를 들어 형식</span><span class="sxs-lookup"><span data-stu-id="58b53-350">Consider for example the type</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="58b53-351">에 `c` 형식의 `Complex(1.,-1.)`값 `c w/ Re <- 0.` 이 포함 된 경우는로 `Complex` `Complex(0.,-1.)`계산 되는 형식의 식입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-351">If `c` contains the value of type `Complex(1.,-1.)`, then `c w/ Re <- 0.` is an expression of type `Complex` that evaluates to `Complex(0.,-1.)`.</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="58b53-352">조건 식</span><span class="sxs-lookup"><span data-stu-id="58b53-352">Conditional Expressions</span></span>

<span data-ttu-id="58b53-353">동일한 형식 및 부울 식의 다른 두 식이 지정 된 경우 물음표 `?` 및 세로 막대 `|`를 사용 하 여 조건 식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-353">Given two other expressions of the same type and a Boolean expression, the conditional expression may be formed using the question mark `?` and the vertical bar `|`.</span></span>
<span data-ttu-id="58b53-354">예를 `a==b ? c | d`들면입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-354">For instance, `a==b ? c | d`.</span></span>
<span data-ttu-id="58b53-355">이 예에서는 조건식 `c` `a==b` 의 값이 true 이면이 고 `d` , 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-355">In this example, the value of the conditional expression will be `c` if `a==b` is true and `d` if it is false.</span></span>

<span data-ttu-id="58b53-356">두 식은 동일한 입력 및 출력을 포함 하는 작업으로 평가 될 수 있지만 다른 함수을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-356">The two expressions may evaluate to operations that have the same inputs and outputs but support different functors.</span></span>
<span data-ttu-id="58b53-357">이 경우 조건식의 형식은 두 식에서 지원 되는 모든 함수를 지 원하는 입력 및 출력을 사용 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-357">In this case, the type of the conditional expression is an operation with those inputs and outputs that supports any functors supported by both expressions.</span></span>
<span data-ttu-id="58b53-358">`Op1`예 `Op2` `Op3` 를 들어, 및 모두가 `Qubit[]=>Unit`이지만,를 `Op1` 지원 `Adjoint` `Op2` `Controlled`하 고를 지원 하며 `Op3` 를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-358">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[]=>Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="58b53-359">`flag ? Op1 | Op2`은 `(Qubit[] => Unit)` 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-359">`flag ? Op1 | Op2` is a `(Qubit[] => Unit)` operation.</span></span>
- <span data-ttu-id="58b53-360">`flag ? Op1 | Op3`은 `(Qubit[] => Unit is Adj)` 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-360">`flag ? Op1 | Op3` is a `(Qubit[] => Unit is Adj)` operation.</span></span>
- <span data-ttu-id="58b53-361">`flag ? Op2 | Op3`은 `(Qubit[] => Unit is Ctl)` 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-361">`flag ? Op2 | Op3` is a `(Qubit[] => Unit is Ctl)` operation.</span></span>

<span data-ttu-id="58b53-362">가능한 두 결과 식 중 하나에 함수 또는 작업 호출이 포함 된 경우 해당 호출은 호출의 값이 되는 경우에만 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-362">If either of the two possible result expressions include a function or operation call, that call will only take place if that result is the one that will be the value of the call.</span></span>
<span data-ttu-id="58b53-363">`a==b ? C(qs) | D(qs)`예를 들어 `a==b` ,이 true 이면 `C` 작업이 호출 되 고 false 인 경우에만 `D` 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-363">For instance, in the case `a==b ? C(qs) | D(qs)`, if `a==b` is true then the `C` operation will be invoked, and if it is false then only `D` will be invoked.</span></span>
<span data-ttu-id="58b53-364">이는 다른 언어의 단락과 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-364">This is similar to short-circuiting in other languages.</span></span>


## <a name="operator-precedence"></a><span data-ttu-id="58b53-365">연산자 우선 순위</span><span class="sxs-lookup"><span data-stu-id="58b53-365">Operator Precedence</span></span>

<span data-ttu-id="58b53-366">모든 이항 연산자는를 제외 하 고 오른쪽 결합성 `^`이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-366">All binary operators are right-associative, except for `^`.</span></span>

<span data-ttu-id="58b53-367">`[` 대괄호 및는 배열 조각화 및 인덱싱의 경우 모든 연산자 앞에 `]`바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-367">Brackets, `[` and `]`, for array slicing and indexing, bind before any operator.</span></span>

<span data-ttu-id="58b53-368">함수 `Adjoint` 및 `Controlled` 는 배열 인덱싱 후 다른 모든 연산자 앞에 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-368">The functors `Adjoint` and `Controlled` bind after array indexing but before all other operators.</span></span>

<span data-ttu-id="58b53-369">연산 및 함수 호출에 대 한 괄호는 모든 연산자 앞에, 배열 인덱싱 및 함수 후에도 바인딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-369">Parentheses for operation and function invocation also bind before any operator but after array indexing and functors.</span></span>

<span data-ttu-id="58b53-370">우선 순위 순으로 최고에서 최저 순으로 연산자.</span><span class="sxs-lookup"><span data-stu-id="58b53-370">Operators in order of precedence, from highest to lowest:</span></span>

<span data-ttu-id="58b53-371">연산자</span><span class="sxs-lookup"><span data-stu-id="58b53-371">Operator</span></span> | <span data-ttu-id="58b53-372">숫자</span><span class="sxs-lookup"><span data-stu-id="58b53-372">Arity</span></span> | <span data-ttu-id="58b53-373">설명</span><span class="sxs-lookup"><span data-stu-id="58b53-373">Description</span></span> | <span data-ttu-id="58b53-374">피연산자 형식</span><span class="sxs-lookup"><span data-stu-id="58b53-374">Operand Types</span></span>
---------|----------|---------|---------------
 <span data-ttu-id="58b53-375">붙이지`!`</span><span class="sxs-lookup"><span data-stu-id="58b53-375">trailing `!`</span></span> | <span data-ttu-id="58b53-376">단항</span><span class="sxs-lookup"><span data-stu-id="58b53-376">Unary</span></span> | <span data-ttu-id="58b53-377">래핑 취소</span><span class="sxs-lookup"><span data-stu-id="58b53-377">Unwrap</span></span> | <span data-ttu-id="58b53-378">사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="58b53-378">Any user-defined type</span></span>
 <span data-ttu-id="58b53-379">`-`, `~~~`, `not`</span><span class="sxs-lookup"><span data-stu-id="58b53-379">`-`, `~~~`, `not`</span></span> | <span data-ttu-id="58b53-380">단항</span><span class="sxs-lookup"><span data-stu-id="58b53-380">Unary</span></span> | <span data-ttu-id="58b53-381">숫자 음수, 비트 보수, 논리 부정</span><span class="sxs-lookup"><span data-stu-id="58b53-381">Numeric negative, bitwise complement, logical negation</span></span> | <span data-ttu-id="58b53-382">`Int``BigInt` `Double` `-`,의 `Int` 경우,,의 경우,의 경우 `BigInt` `~~~` `Bool``not`</span><span class="sxs-lookup"><span data-stu-id="58b53-382">`Int`, `BigInt` or `Double` for `-`, `Int` or `BigInt` for `~~~`, `Bool` for `not`</span></span>
 `^` | <span data-ttu-id="58b53-383">이진</span><span class="sxs-lookup"><span data-stu-id="58b53-383">Binary</span></span> | <span data-ttu-id="58b53-384">정수 거듭제곱</span><span class="sxs-lookup"><span data-stu-id="58b53-384">Integer power</span></span> | <span data-ttu-id="58b53-385">`Int`또는 `BigInt` 기준 `Int` 의 경우 지 수의 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="58b53-385">`Int` or `BigInt` for the base, `Int` for the exponent</span></span>
 <span data-ttu-id="58b53-386">`/`, `*`, `%`</span><span class="sxs-lookup"><span data-stu-id="58b53-386">`/`, `*`, `%`</span></span> | <span data-ttu-id="58b53-387">이진</span><span class="sxs-lookup"><span data-stu-id="58b53-387">Binary</span></span> | <span data-ttu-id="58b53-388">나누기, 곱하기, 정수 모듈러스</span><span class="sxs-lookup"><span data-stu-id="58b53-388">Division, multiplication, integer modulus</span></span> | <span data-ttu-id="58b53-389">`Int``Double` `BigInt` ,,, 또는 `BigInt` 의 경우 `/` `*` `Int``%`</span><span class="sxs-lookup"><span data-stu-id="58b53-389">`Int`, `BigInt` or `Double` for `/` and `*`, `Int` or `BigInt` for `%`</span></span>
 <span data-ttu-id="58b53-390">`+`, `-`</span><span class="sxs-lookup"><span data-stu-id="58b53-390">`+`, `-`</span></span> | <span data-ttu-id="58b53-391">이진</span><span class="sxs-lookup"><span data-stu-id="58b53-391">Binary</span></span> | <span data-ttu-id="58b53-392">더하기 또는 문자열 및 배열 연결, 빼기</span><span class="sxs-lookup"><span data-stu-id="58b53-392">Addition or string and array concatenation, subtraction</span></span> | <span data-ttu-id="58b53-393">`Int`, `BigInt` , `Double`또는 `String` 에 대 한 배열 형식입니다.`+`</span><span class="sxs-lookup"><span data-stu-id="58b53-393">`Int`, `BigInt` or `Double`, additionally `String` or any array type for `+`</span></span>
 <span data-ttu-id="58b53-394">`<<<`, `>>>`</span><span class="sxs-lookup"><span data-stu-id="58b53-394">`<<<`, `>>>`</span></span> | <span data-ttu-id="58b53-395">이진</span><span class="sxs-lookup"><span data-stu-id="58b53-395">Binary</span></span> | <span data-ttu-id="58b53-396">왼쪽 시프트, 오른쪽 시프트</span><span class="sxs-lookup"><span data-stu-id="58b53-396">Left shift, right shift</span></span> | <span data-ttu-id="58b53-397">`Int` 또는 `BigInt`</span><span class="sxs-lookup"><span data-stu-id="58b53-397">`Int` or `BigInt`</span></span>
 <span data-ttu-id="58b53-398">`<`, `<=`, `>`, `>=`</span><span class="sxs-lookup"><span data-stu-id="58b53-398">`<`, `<=`, `>`, `>=`</span></span> | <span data-ttu-id="58b53-399">이진</span><span class="sxs-lookup"><span data-stu-id="58b53-399">Binary</span></span> | <span data-ttu-id="58b53-400">보다 작음, 작거나 같음, 보다 큼, 보다 큼, 크거나 같음 비교</span><span class="sxs-lookup"><span data-stu-id="58b53-400">Less-than, less-than-or-equal, greater-than, greater-than-or-equal comparisons</span></span> | <span data-ttu-id="58b53-401">`Int`, `BigInt` 또는`Double`</span><span class="sxs-lookup"><span data-stu-id="58b53-401">`Int`, `BigInt` or `Double`</span></span>
 <span data-ttu-id="58b53-402">`==`, `!=`</span><span class="sxs-lookup"><span data-stu-id="58b53-402">`==`, `!=`</span></span> | <span data-ttu-id="58b53-403">이진</span><span class="sxs-lookup"><span data-stu-id="58b53-403">Binary</span></span> | <span data-ttu-id="58b53-404">같음, 같지 않음 비교</span><span class="sxs-lookup"><span data-stu-id="58b53-404">equal, not-equal comparisons</span></span> | <span data-ttu-id="58b53-405">모든 기본 형식</span><span class="sxs-lookup"><span data-stu-id="58b53-405">any primitive type</span></span>
 `&&&` | <span data-ttu-id="58b53-406">이진</span><span class="sxs-lookup"><span data-stu-id="58b53-406">Binary</span></span> | <span data-ttu-id="58b53-407">비트 AND</span><span class="sxs-lookup"><span data-stu-id="58b53-407">Bitwise AND</span></span> | <span data-ttu-id="58b53-408">`Int` 또는 `BigInt`</span><span class="sxs-lookup"><span data-stu-id="58b53-408">`Int` or `BigInt`</span></span>
 `^^^` | <span data-ttu-id="58b53-409">이진</span><span class="sxs-lookup"><span data-stu-id="58b53-409">Binary</span></span> | <span data-ttu-id="58b53-410">비트 XOR</span><span class="sxs-lookup"><span data-stu-id="58b53-410">Bitwise XOR</span></span> | <span data-ttu-id="58b53-411">`Int` 또는 `BigInt`</span><span class="sxs-lookup"><span data-stu-id="58b53-411">`Int` or `BigInt`</span></span>
 <code>\|\|\|</code> | <span data-ttu-id="58b53-412">이진</span><span class="sxs-lookup"><span data-stu-id="58b53-412">Binary</span></span> | <span data-ttu-id="58b53-413">비트 OR</span><span class="sxs-lookup"><span data-stu-id="58b53-413">Bitwise OR</span></span> | <span data-ttu-id="58b53-414">`Int` 또는 `BigInt`</span><span class="sxs-lookup"><span data-stu-id="58b53-414">`Int` or `BigInt`</span></span>
 `and` | <span data-ttu-id="58b53-415">이진</span><span class="sxs-lookup"><span data-stu-id="58b53-415">Binary</span></span> | <span data-ttu-id="58b53-416">논리적 AND</span><span class="sxs-lookup"><span data-stu-id="58b53-416">Logical AND</span></span> | `Bool`
 `or` | <span data-ttu-id="58b53-417">이진</span><span class="sxs-lookup"><span data-stu-id="58b53-417">Binary</span></span> | <span data-ttu-id="58b53-418">논리적 OR</span><span class="sxs-lookup"><span data-stu-id="58b53-418">Logical OR</span></span> | `Bool`
 `..` | <span data-ttu-id="58b53-419">Binary/삼항</span><span class="sxs-lookup"><span data-stu-id="58b53-419">Binary/Ternary</span></span> | <span data-ttu-id="58b53-420">Range 연산자</span><span class="sxs-lookup"><span data-stu-id="58b53-420">Range operator</span></span> | `Int`
 <span data-ttu-id="58b53-421">`?` `|`</span><span class="sxs-lookup"><span data-stu-id="58b53-421">`?` `|`</span></span> | <span data-ttu-id="58b53-422">진</span><span class="sxs-lookup"><span data-stu-id="58b53-422">Ternary</span></span> | <span data-ttu-id="58b53-423">조건부</span><span class="sxs-lookup"><span data-stu-id="58b53-423">Conditional</span></span> | <span data-ttu-id="58b53-424">`Bool`왼쪽의 경우</span><span class="sxs-lookup"><span data-stu-id="58b53-424">`Bool` for the left-hand-side</span></span>
<span data-ttu-id="58b53-425">`w/` `<-`</span><span class="sxs-lookup"><span data-stu-id="58b53-425">`w/` `<-`</span></span> | <span data-ttu-id="58b53-426">진</span><span class="sxs-lookup"><span data-stu-id="58b53-426">Ternary</span></span> | <span data-ttu-id="58b53-427">복사 및 업데이트</span><span class="sxs-lookup"><span data-stu-id="58b53-427">Copy-and-update</span></span> | <span data-ttu-id="58b53-428">[복사 및 업데이트 식](#copy-and-update-expressions) 참조</span><span class="sxs-lookup"><span data-stu-id="58b53-428">see [copy-and-update expressions](#copy-and-update-expressions)</span></span>
