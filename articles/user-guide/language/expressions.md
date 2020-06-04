---
title: 'Q의 형식 식 #'
description: 'Q #에서 상수, 변수, 연산자, 작업 및 함수를 식으로 지정, 참조 및 결합 하는 방법을 이해 합니다.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
ms.openlocfilehash: c4b2cc0bed44ffdfb191ba522d6526959e7c6708
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327308"
---
# <a name="type-expressions-in-q"></a><span data-ttu-id="1dd0d-103">Q의 형식 식 #</span><span class="sxs-lookup"><span data-stu-id="1dd0d-103">Type Expressions in Q#</span></span>

## <a name="numeric-expressions"></a><span data-ttu-id="1dd0d-104">숫자 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-104">Numeric Expressions</span></span>

<span data-ttu-id="1dd0d-105">숫자 식은, 또는 형식의 식 `Int` 입니다 `BigInt` `Double` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-105">Numeric expressions are expressions of type `Int`, `BigInt`, or `Double`.</span></span>
<span data-ttu-id="1dd0d-106">즉, 정수 또는 부동 소수점 숫자 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-106">That is, they are either integer or floating-point numbers.</span></span>

<span data-ttu-id="1dd0d-107">`Int`Q #의 리터럴은 단순히 숫자 시퀀스로 작성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-107">`Int` literals in Q# are written simply as a sequence of digits.</span></span>
<span data-ttu-id="1dd0d-108">16 진수 및 이진 정수는 `0x` 각각 및 접두사를 사용 하 여 지원 됩니다 `0b` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-108">Hexadecimal and binary integers are supported with a `0x` and `0b` prefix, respectively.</span></span>

<span data-ttu-id="1dd0d-109">`BigInt`Q #의 리터럴은 후행 또는 접미사로 작성 됩니다 `l` `L` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-109">`BigInt` literals in Q# are written with a trailing `l` or `L` suffix.</span></span>
<span data-ttu-id="1dd0d-110">16 진수 큰 정수는 "0x" 접두사를 사용 하 여 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-110">Hexadecimal big integers are supported with a "0x" prefix.</span></span>
<span data-ttu-id="1dd0d-111">따라서 다음은 리터럴의 모든 유효한 사용입니다 `BigInt` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-111">Thus, the following are all valid uses of `BigInt` literals:</span></span>

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

<span data-ttu-id="1dd0d-112">`Double`Q #의 리터럴은 10 진수를 사용 하 여 작성 된 부동 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-112">`Double` literals in Q# are floating-point numbers written using decimal digits.</span></span>
<span data-ttu-id="1dd0d-113">소수점, `.` 및/또는 ' e ' 또는 ' e '로 표시 된 지 수 부분을 사용 하 여 작성할 수 있습니다 .이 경우에는 가능한 음수 부호와 소수 자릿수만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-113">They can be written with a decimal point, `.`, and/or an exponential part indicated with 'e' or 'E' (after which only a possible negative sign and decimal digits are valid).</span></span>
<span data-ttu-id="1dd0d-114">유효한 `Double` 리터럴은 `0.0` , `1.2e5` , `1e-5` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-114">The following are valid `Double` literals: `0.0`, `1.2e5`, `1e-5`.</span></span>

<span data-ttu-id="1dd0d-115">모든 요소 형식의 배열 식이 지정 된 경우 `Int` 기본 제공 함수를 사용 하 여 식을 구성 하 [`Length`](xref:microsoft.quantum.core.length) 고, 배열 식이 괄호로 묶여 있으며,를 사용 하 여 식을 만들 수 있습니다 `(` `)` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-115">Given an array expression of any element type, an `Int` expression may be formed using the [`Length`](xref:microsoft.quantum.core.length) built-in function, with the array expression enclosed in parentheses, `(` and `)`.</span></span>
<span data-ttu-id="1dd0d-116">예를 들어 `a` 가 배열에 바인딩된 경우 `Length(a)` 는 정수 식입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-116">For instance, if `a` is bound to an array, then `Length(a)` is an integer expression.</span></span>
<span data-ttu-id="1dd0d-117">`b`가 정수 배열의 배열인 경우는 `Int[][]` `Length(b)` 의 하위 배열 수이 `b` 고 `Length(b[1])` 은의 두 번째 하위 배열에 있는 정수 수입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-117">If `b` is an array of arrays of integers, `Int[][]`, then `Length(b)` is the number of sub-arrays in `b`, and `Length(b[1])` is the number of integers in the second sub-array in `b`.</span></span>

<span data-ttu-id="1dd0d-118">동일한 형식의 두 숫자 식이 지정 된 경우 이항 연산자 `+` , `-` , 및를 `*` `/` 사용 하 여 새 숫자 식을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-118">Given two numeric expressions of the same type, the binary operators `+`, `-`, `*`, and `/` may be used to form a new numeric expression.</span></span>
<span data-ttu-id="1dd0d-119">새 식의 형식은 구성 식의 형식과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-119">The type of the new expression will be the same as the types of the constituent expressions.</span></span>

<span data-ttu-id="1dd0d-120">두 개의 정수 식이 지정 되 면 이항 연산자 `^` (power)를 사용 하 여 새 정수 식을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-120">Given two integer expressions, the binary operator `^` (power) may be used to form a new integer expression.</span></span>
<span data-ttu-id="1dd0d-121">마찬가지로를 `^` 두 개의 double 식과 함께 사용 하 여 새 double 식을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-121">Similarly, `^` may be used with two double expressions to form a new double expression.</span></span>
<span data-ttu-id="1dd0d-122">마지막으로,은 `^` 왼쪽에서 큰 정수를 사용 하 고 오른쪽에는 정수를 사용 하 여 새 큰 정수 식을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-122">Finally, `^` may be used with a big integer on the left and an integer on the right to form a new big integer expression.</span></span>
<span data-ttu-id="1dd0d-123">이 경우 두 번째 매개 변수는 32 비트에 맞아야 합니다. 그렇지 않으면 런타임 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-123">In this case, the second parameter must fit into 32 bits; if not, a runtime error will be raised.</span></span>

<span data-ttu-id="1dd0d-124">두 개의 정수 또는 큰 정수 식이 지정 된 경우 `%` (모듈러스), `&&&` (비트 and), (비트 or `|||` ) 또는 `^^^` (비트 XOR) 연산자를 사용 하 여 새 정수 또는 큰 정수 식의 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-124">Given two integer or big integer expressions, a new integer or big integer expression may be formed using the `%` (modulus), `&&&` (bitwise AND), `|||` (bitwise OR), or `^^^` (bitwise XOR) operators.</span></span>

<span data-ttu-id="1dd0d-125">왼쪽에 정수 또는 큰 정수 식이 있고 오른쪽에 정수 식이 지정 된 경우 `<<<` (산술 왼쪽 시프트) 또는 `>>>` (산술 오른쪽 시프트) 연산자를 사용 하 여 왼쪽 식과 동일한 형식의 새 식을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-125">Given either an integer or big integer expression on the left, and an integer expression on the right, the `<<<` (arithmetic left shift) or `>>>` (arithmetic right shift) operators may be used to create a new expression with the same type as the left-hand expression.</span></span>

<span data-ttu-id="1dd0d-126">이동 작업에 대 한 두 번째 매개 변수 (이동 크기)는 0 보다 크거나 같아야 합니다. 음수 시프트 금액의 동작은 정의 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-126">The second parameter (the shift amount) to either shift operation must be greater than or equal to zero; the behavior for negative shift amounts is undefined.</span></span>
<span data-ttu-id="1dd0d-127">시프트 연산의 이동 양은 32 비트에도 맞아야 합니다. 그렇지 않으면 런타임 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-127">The shift amount for either shift operation must also fit into 32 bits; if not, a runtime error will be raised.</span></span>
<span data-ttu-id="1dd0d-128">이동할 숫자가 정수 이면 시프트 금액이 해석 됩니다 `mod 64` . 즉, 1의 시프트와 65의 시프트는 동일한 효과를 가집니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-128">If the number to be shifted is an integer, then the shift amount is interpreted `mod 64`; that is, a shift of 1 and a shift of 65 have the same effect.</span></span>

<span data-ttu-id="1dd0d-129">정수 및 큰 정수 값 모두에 대해 시프트는 산술 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-129">For both integer and big integer values, shifts are arithmetic.</span></span>
<span data-ttu-id="1dd0d-130">음수 값을 왼쪽 이나 오른쪽으로 이동 하면 음수가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-130">Shifting a negative value either left or right will result in a negative number.</span></span>
<span data-ttu-id="1dd0d-131">즉, 한 단계를 왼쪽 또는 오른쪽으로 이동 하는 것은 각각 2로의 곱하기 또는 나누기와 정확히 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-131">That is, shifting one step to the left or right is exactly the same as multiplying or dividing by 2, respectively.</span></span>

<span data-ttu-id="1dd0d-132">정수 나누기와 정수 모듈러스는 c #과 같은 음수에 대해 동일한 동작을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-132">Integer division and integer modulus follow the same behavior for negative numbers as C#.</span></span>
<span data-ttu-id="1dd0d-133">즉,는 `a % b` 항상와 동일한 기호를 가집니다 .이는 항상와 동일 `a` `b * (a / b) + a % b` `a` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-133">That is, `a % b` will always have the same sign as `a`, and `b * (a / b) + a % b` will always equal `a`.</span></span>
<span data-ttu-id="1dd0d-134">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-134">For example:</span></span>

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 <span data-ttu-id="1dd0d-135">5</span><span class="sxs-lookup"><span data-stu-id="1dd0d-135">5</span></span> | <span data-ttu-id="1dd0d-136">2</span><span class="sxs-lookup"><span data-stu-id="1dd0d-136">2</span></span> | <span data-ttu-id="1dd0d-137">2</span><span class="sxs-lookup"><span data-stu-id="1dd0d-137">2</span></span> | <span data-ttu-id="1dd0d-138">1</span><span class="sxs-lookup"><span data-stu-id="1dd0d-138">1</span></span>
 <span data-ttu-id="1dd0d-139">5</span><span class="sxs-lookup"><span data-stu-id="1dd0d-139">5</span></span> | <span data-ttu-id="1dd0d-140">-2</span><span class="sxs-lookup"><span data-stu-id="1dd0d-140">-2</span></span> | <span data-ttu-id="1dd0d-141">-2</span><span class="sxs-lookup"><span data-stu-id="1dd0d-141">-2</span></span> | <span data-ttu-id="1dd0d-142">1</span><span class="sxs-lookup"><span data-stu-id="1dd0d-142">1</span></span>
 <span data-ttu-id="1dd0d-143">-5</span><span class="sxs-lookup"><span data-stu-id="1dd0d-143">-5</span></span> | <span data-ttu-id="1dd0d-144">2</span><span class="sxs-lookup"><span data-stu-id="1dd0d-144">2</span></span> | <span data-ttu-id="1dd0d-145">-2</span><span class="sxs-lookup"><span data-stu-id="1dd0d-145">-2</span></span> | <span data-ttu-id="1dd0d-146">-1</span><span class="sxs-lookup"><span data-stu-id="1dd0d-146">-1</span></span>
 <span data-ttu-id="1dd0d-147">-5</span><span class="sxs-lookup"><span data-stu-id="1dd0d-147">-5</span></span> | <span data-ttu-id="1dd0d-148">-2</span><span class="sxs-lookup"><span data-stu-id="1dd0d-148">-2</span></span> | <span data-ttu-id="1dd0d-149">2</span><span class="sxs-lookup"><span data-stu-id="1dd0d-149">2</span></span> | <span data-ttu-id="1dd0d-150">-1</span><span class="sxs-lookup"><span data-stu-id="1dd0d-150">-1</span></span>

<span data-ttu-id="1dd0d-151">큰 정수 나누기와 모듈러스는 동일한 방식으로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-151">Big integer division and modulus works the same way.</span></span>

<span data-ttu-id="1dd0d-152">숫자 식이 지정 된 경우 단항 연산자를 사용 하 여 새 식을 지정할 수 있습니다 `-` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-152">Given any numeric expression, a new expression may be formed using the `-` unary operator.</span></span>
<span data-ttu-id="1dd0d-153">새 식은 구성 식과 동일한 형식이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-153">The new expression will be the same type as the constituent expression.</span></span>

<span data-ttu-id="1dd0d-154">정수 또는 큰 정수 식이 지정 된 경우 `~~~` (비트 보수) 단항 연산자를 사용 하 여 동일한 유형의 새 식을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-154">Given any integer or big integer expression, a new expression of the same type may be formed using the `~~~` (bitwise complement) unary operator.</span></span>

## <a name="boolean-expressions"></a><span data-ttu-id="1dd0d-155">부울 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-155">Boolean Expressions</span></span>

<span data-ttu-id="1dd0d-156">두 `Bool` 리터럴 값은 `true` 및 `false` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-156">The two `Bool` literal values are `true` and `false`.</span></span>

<span data-ttu-id="1dd0d-157">동일한 기본 형식의 두 식이 지정 된 경우 `==` 및 `!=` 이항 연산자를 사용 하 여 식을 생성할 수 있습니다 `Bool` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-157">Given any two expressions of the same primitive type, the `==` and `!=` binary operators may be used to construct a `Bool` expression.</span></span>
<span data-ttu-id="1dd0d-158">식은 두 식이 같으면 true이 고, 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-158">The expression will be true if the two expressions are equal, and false if not.</span></span>

<span data-ttu-id="1dd0d-159">사용자 정의 형식의 값을 비교할 수 없습니다. 래핑 해제 된 값만 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-159">Values of user-defined types may not be compared, only their unwrapped values can be compared.</span></span> <span data-ttu-id="1dd0d-160">예를 들어 "래핑 해제" 연산자 `!` ( [Q #의 형식](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)에 자세히 설명 되어 있음)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-160">For example, using the "unwrap" operator `!` (explained in detail at [Types in Q#](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),</span></span>

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

<span data-ttu-id="1dd0d-161">값에 대 한 같음 비교 `Qubit` 는 id 같음입니다. 즉, 두 식이 동일한의 비트를 식별 하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-161">Equality comparison for `Qubit` values is identity equality; that is, whether the two expressions identify the same qubit.</span></span>
<span data-ttu-id="1dd0d-162">이 비교로 두 비트의 상태를 비교, 액세스, 측정 또는 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-162">The state of the two qubits are not compared, accessed, measured, or modified by this comparison.</span></span>

<span data-ttu-id="1dd0d-163">반올림 결과 때문에 값에 대 한 같음 비교가 `Double` 잘못 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-163">Equality comparison for `Double` values may be misleading due to rounding effects.</span></span>
<span data-ttu-id="1dd0d-164">예를 들면 `49.0 * (1.0/49.0) != 1.0` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-164">For instance, `49.0 * (1.0/49.0) != 1.0`.</span></span>

<span data-ttu-id="1dd0d-165">두 숫자 식이 지정 된 경우 이항 연산자 `>` , `<` , 및를 `>=` `<=` 사용 하 여 첫 번째 식이 두 번째 식 보다 크거나 같고 보다 작거나 같은 경우 true 인 새 부울 식을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-165">Given any two numeric expressions, the binary operators `>`, `<`, `>=`, and `<=` may be used to construct a new Boolean expression that is true if the first expression is respectively greater than, less than, greater than or equal to, or less than or equal to the second expression.</span></span>

<span data-ttu-id="1dd0d-166">부울 식을 두 개 지정 하는 `and` `or` 경우 및 이항 연산자를 사용 하 여 두 식 중 하나 (응답 또는 둘 다)가 true 인 경우 true 인 새 부울 식을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-166">Given any two Boolean expressions, the `and` and `or` binary operators may be used to construct a new Boolean expression that is true if both of (resp. either or both of) the two expressions are true.</span></span>

<span data-ttu-id="1dd0d-167">부울 식이 지정 된 `not` 경우 단항 연산자를 사용 하 여 구성 식이 false 인 경우 true 인 새 부울 식을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-167">Given any Boolean expression, the `not` unary operator may be used to construct a new Boolean expression that is true if the constituent expression is false.</span></span>

## <a name="string-expressions"></a><span data-ttu-id="1dd0d-168">문자열 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-168">String Expressions</span></span>

<span data-ttu-id="1dd0d-169">Q #에서는 문에 사용 되는 문자열 `fail` ( [제어 흐름](xref:microsoft.quantum.guide.controlflow#fail-statement)에 설명)과 표준 함수를 사용할 수 있습니다 [`Message`](xref:microsoft.quantum.intrinsic.message) .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-169">Q# allows strings to be used in the `fail` statement (explained at [Control Flow](xref:microsoft.quantum.guide.controlflow#fail-statement)) and in the [`Message`](xref:microsoft.quantum.intrinsic.message) standard function.</span></span>
<span data-ttu-id="1dd0d-170">후자의 특정 동작은 사용 되는 시뮬레이터에 따라 다르지만 일반적으로 Q # 프로그램을 실행 하는 동안 호출 될 때 호스트 콘솔에 메시지를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-170">The specific behavior of the latter depends on the simulator being used, but typically writes a message to the host console when called during a Q# program.</span></span>

<span data-ttu-id="1dd0d-171">Q #의 문자열은 리터럴 또는 보간된 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-171">Strings in Q# are either literals or interpolated strings.</span></span>

<span data-ttu-id="1dd0d-172">문자열 리터럴은 대부분의 언어에서 간단한 문자열 리터럴과 유사 합니다. 큰따옴표 안의 유니코드 문자 시퀀스 `"` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-172">String literals are similar to simple string literals in most languages: a sequence of Unicode characters enclosed in double quotes, `"`.</span></span>
<span data-ttu-id="1dd0d-173">문자열 내에서 백슬래시 문자를 사용 하 여 `\` 큰따옴표 문자를 이스케이프 하 고 새 줄을로 `\n` , 캐리지 리턴을로 `\r` , 탭을로 삽입할 수 있습니다 `\t` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-173">Inside of a string, the back-slash character `\` may be used to escape a double quote character, and to insert a new-line as `\n`, a carriage return as `\r`, and a tab as `\t`.</span></span>
<span data-ttu-id="1dd0d-174">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-174">For instance:</span></span>

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a><span data-ttu-id="1dd0d-175">보간된 문자열</span><span class="sxs-lookup"><span data-stu-id="1dd0d-175">Interpolated strings</span></span>

<span data-ttu-id="1dd0d-176">문자열 보간에 대 한 Q # 구문은 c # 구문의 하위 집합 이지만 여기서는 Q #와 관련 된 주요 요점을 요약 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-176">The Q# syntax for string interpolations is a subset of the C# syntax, but we summarize here the key points as they pertain to Q#.</span></span>
<span data-ttu-id="1dd0d-177">주요 차이점은 아래에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-177">The main distinctions are discussed below.</span></span>

<span data-ttu-id="1dd0d-178">문자열 리터럴을 보간된 문자열로 식별하려면 `$` 기호를 사용하여 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-178">To identify a string literal as an interpolated string, prepend it with the `$` symbol.</span></span>
<span data-ttu-id="1dd0d-179">`$` `"` 문자열과 문자열 리터럴을 시작 하는 사이에는 공백을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-179">You cannot have any white space between the `$`and the `"` that starts a string literal.</span></span>

<span data-ttu-id="1dd0d-180">다음은 함수를 사용 하 여 [`Message`](xref:microsoft.quantum.intrinsic.message) 다른 Q # 식과 함께 측정 결과를 콘솔에 쓰는 기본적인 예입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-180">The following is a basic example using the [`Message`](xref:microsoft.quantum.intrinsic.message) function to write the result of a measurement to the console, alongside other Q# expressions.</span></span>

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```
<span data-ttu-id="1dd0d-181">유효한 Q # 식은 보간된 문자열에 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-181">Any valid Q# expression may appear in an interpolated string.</span></span>

<span data-ttu-id="1dd0d-182">C # 구문에 대 한 자세한 내용은 [*보간된 문자열*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-182">Further details on the C# syntax can be found at [*Interpolated Strings*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span></span>
<span data-ttu-id="1dd0d-183">가장 주목할 만한 차이점은 Q #은 축 자 (여러 줄) 보간된 문자열을 지원 하지 않는다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-183">The most notable distinction is that Q# does not support verbatim (multi-line) interpolated strings.</span></span>
<span data-ttu-id="1dd0d-184">보간된 문자열 내부의 식은 c # 구문이 아니라 Q # 구문을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-184">Expressions inside of an interpolated string follow Q# syntax, not C# syntax.</span></span>

## <a name="range-expressions"></a><span data-ttu-id="1dd0d-185">범위 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-185">Range Expressions</span></span>

<span data-ttu-id="1dd0d-186">3 개의 식, 및가 지정 된 경우이 `Int` `start` `step` `stop` `start .. step .. stop` `start` `start+step` `start+step+step` 전달 될 때까지 첫 번째 요소가이 고, 두 번째 요소가 `stop` 이 고, 세 번째 요소가 인 범위 식입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-186">Given any three `Int` expressions `start`, `step`, and `stop`, `start .. step .. stop` is a range expression whose first element is `start`, second element is `start+step`, third element is `start+step+step`, etc., until `stop` is passed.</span></span>
<span data-ttu-id="1dd0d-187">예를 들어,가 양수인 경우 범위는 비어 있을 수 있습니다 `step` `stop < start` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-187">A range may be empty if, for instance, `step` is positive and `stop < start`.</span></span>
<span data-ttu-id="1dd0d-188">범위의 마지막 요소는 `stop` 와의 차이가의 정수 배수가 면가 `start` 됩니다 `stop` `step` . 즉, 범위는 양쪽 끝에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-188">The last element of the range will be `stop` if the difference between `start` and `stop` is an integral multiple of `step`; that is, the range is inclusive at both ends.</span></span>

<span data-ttu-id="1dd0d-189">두 식 및가 지정 된 경우는와 `Int` `start` `stop` `start .. stop` 같은 범위 식입니다 `start .. 1 .. stop` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-189">Given any two `Int` expressions `start` and `stop`, `start .. stop` is a range expression that is equal to `start .. 1 .. stop`.</span></span>
<span data-ttu-id="1dd0d-190">`step`가 보다 작은 경우에도 암시는 + 1입니다 .이 `stop` `start` 경우 범위는 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-190">Note that the implied `step` is +1 even if `stop` is less than `start`; in such a case, the range is empty.</span></span>

<span data-ttu-id="1dd0d-191">몇 가지 예제 범위는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-191">Some example ranges are:</span></span>

- <span data-ttu-id="1dd0d-192">`1..3`은 1, 2, 3의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-192">`1..3` is the range 1, 2, 3.</span></span>
- <span data-ttu-id="1dd0d-193">`2..2..5`는 범위 2, 4입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-193">`2..2..5` is the range 2, 4.</span></span>
- <span data-ttu-id="1dd0d-194">`2..2..6`는 2, 4, 6 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-194">`2..2..6` is the range 2, 4, 6.</span></span>
- <span data-ttu-id="1dd0d-195">`6..-2..2`는 6, 4, 2 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-195">`6..-2..2` is the range 6, 4, 2.</span></span>
- <span data-ttu-id="1dd0d-196">`2..1`는 빈 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-196">`2..1` is the empty range.</span></span>
- <span data-ttu-id="1dd0d-197">`2..6..7`는 범위 2입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-197">`2..6..7` is the range 2.</span></span>
- <span data-ttu-id="1dd0d-198">`2..2..1`는 빈 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-198">`2..2..1` is the empty range.</span></span>
- <span data-ttu-id="1dd0d-199">`1..-1..2`는 빈 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-199">`1..-1..2` is the empty range.</span></span>

## <a name="qubit-expressions"></a><span data-ttu-id="1dd0d-200">Bit 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-200">Qubit Expressions</span></span>

<span data-ttu-id="1dd0d-201">유일한 `Qubit` 식은 `Qubit` 배열의 배열 요소 또는 값에 바인딩되는 기호입니다 `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-201">The only `Qubit` expressions are symbols that are bound to `Qubit` values or array elements of `Qubit` arrays.</span></span>
<span data-ttu-id="1dd0d-202">`Qubit`리터럴이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-202">There are no `Qubit` literals.</span></span>

## <a name="pauli-expressions"></a><span data-ttu-id="1dd0d-203">Pauli 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-203">Pauli Expressions</span></span>

<span data-ttu-id="1dd0d-204">,, 및의 네 가지 `Pauli` 값은 `PauliI` `PauliX` `PauliY` `PauliZ` 모두 유효한 `Pauli` 식입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-204">The four `Pauli` values, `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, are all valid `Pauli` expressions.</span></span>

<span data-ttu-id="1dd0d-205">그 외에도 유일한 `Pauli` 식은 `Pauli` 배열의 배열 요소 또는 값에 바인딩되는 기호입니다 `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-205">Other than that, the only `Pauli` expressions are symbols that are bound to `Pauli` values or array elements of `Pauli` arrays.</span></span>

## <a name="result-expressions"></a><span data-ttu-id="1dd0d-206">결과 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-206">Result Expressions</span></span>

<span data-ttu-id="1dd0d-207">두 `Result` 값 및는 `One` `Zero` 유효한 `Result` 식입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-207">The two `Result` values, `One` and `Zero`, are valid `Result` expressions.</span></span>

<span data-ttu-id="1dd0d-208">그 외에도 유일한 `Result` 식은 `Result` 배열의 배열 요소 또는 값에 바인딩되는 기호입니다 `Result` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-208">Other than that, the only `Result` expressions are symbols that are bound to `Result` values or array elements of `Result` arrays.</span></span>
<span data-ttu-id="1dd0d-209">특히는 `One` 정수와 동일 하지 않으며 `1` 두 요소 사이에 직접 변환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-209">In particular, note that `One` is not the same as the integer `1`, and there is no direct conversion between them.</span></span>
<span data-ttu-id="1dd0d-210">및의 경우에도 마찬가지입니다 `Zero` `0` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-210">The same is true for `Zero` and `0`.</span></span>

## <a name="tuple-expressions"></a><span data-ttu-id="1dd0d-211">튜플 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-211">Tuple Expressions</span></span>

<span data-ttu-id="1dd0d-212">튜플 리터럴은 및로 묶인 적절 한 형식의 요소 식 시퀀스로, 쉼표로 구분 됩니다 `(` `)` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-212">A tuple literal is a sequence of element expressions of the appropriate type, separated by commas, enclosed in `(` and `)`.</span></span>
<span data-ttu-id="1dd0d-213">예를 들어 `(1, One)` 은 `(Int, Result)` 식입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-213">For instance, `(1, One)` is an `(Int, Result)` expression.</span></span>

<span data-ttu-id="1dd0d-214">리터럴 이외의 튜플 식은 튜플 값에 바인딩된 기호, 튜플 배열의 배열 요소 및 튜플을 반환 하는 호출 가능 호출입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-214">Other than literals, the only tuple expressions are symbols that are bound to tuple values, array elements of tuple arrays, and callable invocations that return tuples.</span></span>

## <a name="user-defined-type-expressions"></a><span data-ttu-id="1dd0d-215">사용자 정의 형식 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-215">User-Defined Type Expressions</span></span>

<span data-ttu-id="1dd0d-216">사용자 정의 형식의 리터럴은 형식 이름과 해당 형식의 기본 튜플 형식의 튜플 리터럴로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-216">A literal of a user-defined type consists of the type name followed by a tuple literal of the type’s base tuple type.</span></span>
<span data-ttu-id="1dd0d-217">예를 들어, `IntPair` 가를 기반으로 하는 사용자 정의 형식인 경우 `(Int, Int)` `IntPair(2, 3)` 는 해당 형식의 유효한 리터럴입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-217">For instance, if `IntPair` is a user-defined type based on `(Int, Int)`, then `IntPair(2, 3)` would be a valid literal of that type.</span></span>

<span data-ttu-id="1dd0d-218">리터럴 외에 사용자 정의 형식의 유일한 식은 해당 형식의 값에 바인딩된 기호, 해당 형식의 배열 요소, 해당 형식을 반환 하는 호출 가능 호출입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-218">Other than literals, the only expressions of a user-defined type are symbols that are bound to values of that type, array elements of arrays of that type, and callable invocations that return that type.</span></span>

## <a name="unwrap-expressions"></a><span data-ttu-id="1dd0d-219">래핑 해제 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-219">Unwrap Expressions</span></span>

<span data-ttu-id="1dd0d-220">Q #에서 래핑 해제 연산자는 후행 감탄 부호 `!` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-220">In Q#, the unwrap operator is a trailing exclamation mark `!`.</span></span>
<span data-ttu-id="1dd0d-221">예를 들어, `IntPair` 가 기본 형식의 사용자 정의 형식이 `(Int, Int)` 고 `s` 값이 인 변수인 경우는 `IntPair(2, 3)` `s!` `(2, 3)` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-221">For instance, if `IntPair` is a user-defined type with underlying type `(Int, Int)`, and `s` was a variable with value `IntPair(2, 3)`, then `s!` would be `(2, 3)`.</span></span>

<span data-ttu-id="1dd0d-222">사용자 정의 형식에 대해 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-222">For user-defined types defined in terms of other user-defined types.</span></span> <span data-ttu-id="1dd0d-223">래핑 해제 연산자는 반복 될 수 있습니다. 예를 들어는 `s!!` 이중 래핑 해제 된 값을 `s` 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-223">the unwrap operator may be repeated; for instance, `s!!` indicates the doubly-unwrapped value of `s`.</span></span>
<span data-ttu-id="1dd0d-224">따라서 `WrappedPair` 가 기본 형식의 사용자 정의 형식이 `IntPair` 고 `t` 가 값이 포함 된 변수인 경우은 `WrappedPair(IntPair(1,2))` `t!!` `(1,2)` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-224">Thus, if `WrappedPair` is a user-defined type with underlying type `IntPair`, and `t` is a variable with value `WrappedPair(IntPair(1,2))`, then `t!!` would be `(1,2)`.</span></span>

<span data-ttu-id="1dd0d-225">`!`연산자는 `[]` 배열 인덱싱 및 조각화를 위해 이외의 다른 모든 연산자 보다 우선 순위가 높습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-225">The `!` operator has higher precedence than all other operators other than `[]` for array indexing and slicing.</span></span>
<span data-ttu-id="1dd0d-226">`!`및 `[]` bind 메서드에 액세스할. 즉, `a[i]![3]` `((a[i])!)[3]` `i` 의 ' 번째 요소를 가져와 래핑 해제 한 `a` 다음 래핑 해제 된 값 (배열 이어야 함)의 세 번째 요소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-226">`!` and `[]` bind positionally; that is, `a[i]![3]` should be read as `((a[i])!)[3]`: take the `i`'th element of `a`, unwrap it, and then get the 3rd element of the unwrapped value (which must be an array).</span></span>

<span data-ttu-id="1dd0d-227">연산자의 우선 순위에는 `!` 명확 하지 않을 수 있는 영향이 하나 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-227">The precedence of the `!` operator has one impact that might not be obvious.</span></span>
<span data-ttu-id="1dd0d-228">함수 또는 작업에서 래핑 해제 되는 값을 반환 하는 경우 인수 튜플이 래핑 되지 않고 호출에 바인딩되도록 함수 또는 작업 호출을 괄호로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-228">If a function or operation returns a value that then gets unwrapped, the function or operation call must be enclosed in parentheses so that the argument tuple binds to the call rather than to the unwrap.</span></span>
<span data-ttu-id="1dd0d-229">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-229">For example:</span></span>

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a><span data-ttu-id="1dd0d-230">배열 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-230">Array Expressions</span></span>

<span data-ttu-id="1dd0d-231">배열 리터럴은 및로 묶인 하나 이상의 요소 식의 시퀀스로, 쉼표로 구분 됩니다 `[` `]` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-231">An array literal is a sequence of one or more element expressions, separated by commas, enclosed in `[` and `]`.</span></span>
<span data-ttu-id="1dd0d-232">모든 요소는 동일한 형식과 호환 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-232">All elements must be compatible with the same type.</span></span>

<span data-ttu-id="1dd0d-233">동일한 형식의 두 배열이 지정 된 경우 이항 연산자를 `+` 사용 하 여 두 배열의 연결 인 새 배열을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-233">Given two arrays of the same type, the binary `+` operator may be used to form a new array that is the concatenation of the two arrays.</span></span>
<span data-ttu-id="1dd0d-234">예를 들어 `[1,2,3] + [4,5,6]` 은 `[1,2,3,4,5,6]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-234">For instance, `[1,2,3] + [4,5,6]` is `[1,2,3,4,5,6]`.</span></span>

### <a name="array-creation"></a><span data-ttu-id="1dd0d-235">배열 만들기</span><span class="sxs-lookup"><span data-stu-id="1dd0d-235">Array Creation</span></span>

<span data-ttu-id="1dd0d-236">형식 및 식이 지정 된 경우 `Int` 연산자를 `new` 사용 하 여 지정 된 크기의 새 배열을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-236">Given a type and an `Int` expression, the `new` operator may be used to allocate a new array of the given size.</span></span>
<span data-ttu-id="1dd0d-237">예를 들어는 `new Int[i + 1]` `Int` 요소로 새 배열을 할당 `i + 1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-237">For instance, `new Int[i + 1]` would allocate a new `Int` array with `i + 1` elements.</span></span>

<span data-ttu-id="1dd0d-238">빈 배열 리터럴는 `[]` 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-238">Empty array literals, `[]`, are not allowed.</span></span>
<span data-ttu-id="1dd0d-239">대신를 사용 하는 대신를 사용 합니다 `new ★[0]` `★` . 여기서은 적절 한 형식에 대 한 자리 표시자입니다 .를 사용 하면 원하는 길이 0 배열을 만들 수 있습니다</span><span class="sxs-lookup"><span data-stu-id="1dd0d-239">Instead using `new ★[0]`, where `★` is as placeholder for a suitable type, allows to create the desired array of length zero.</span></span>

<span data-ttu-id="1dd0d-240">새 배열의 요소는 형식 종속 기본값으로 초기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-240">The elements of a new array are initialized to a type-dependent default value.</span></span>
<span data-ttu-id="1dd0d-241">대부분의 경우이 값은 0으로 변형 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-241">In most cases this is some variation of zero.</span></span>

<span data-ttu-id="1dd0d-242">엔터티를 참조 하는 callables 및 callables의 경우 적절 한 기본값이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-242">For qubits and callables, which are references to entities, there is no reasonable default value.</span></span>
<span data-ttu-id="1dd0d-243">따라서 이러한 형식의 경우 기본값은 런타임 오류를 발생 시 키 지 않고 사용할 수 없는 잘못 된 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-243">Thus, for these types, the default is an invalid reference that cannot be used without causing a runtime error.</span></span>
<span data-ttu-id="1dd0d-244">이는 c #, Java 등의 언어에서 null 참조와 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-244">This is similar to a null reference in languages such as C# or Java.</span></span>
<span data-ttu-id="1dd0d-245">요소가 안전 하 게 사용 되기 전에는 기본값이 아닌 값을 사용 하 여 valbits 또는 callables을 포함 하는 배열을 적절 하 게 초기화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-245">Arrays containing qubits or callables must be properly initialized with non-default values before their elements may be safely used.</span></span> <span data-ttu-id="1dd0d-246">적절 한 초기화 루틴은에서 찾을 수 있습니다 <xref:microsoft.quantum.arrays> .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-246">Suitable initialization routines can be found in <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="1dd0d-247">각 형식에 대 한 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-247">The default values for each type are:</span></span>

<span data-ttu-id="1dd0d-248">Type</span><span class="sxs-lookup"><span data-stu-id="1dd0d-248">Type</span></span> | <span data-ttu-id="1dd0d-249">기본값</span><span class="sxs-lookup"><span data-stu-id="1dd0d-249">Default</span></span>
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | <span data-ttu-id="1dd0d-250">_invalid qubit_</span><span class="sxs-lookup"><span data-stu-id="1dd0d-250">_invalid qubit_</span></span>
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | <span data-ttu-id="1dd0d-251">빈 범위`1..1..0`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-251">The empty range, `1..1..0`</span></span>
 `Callable` | <span data-ttu-id="1dd0d-252">_invalid callable_</span><span class="sxs-lookup"><span data-stu-id="1dd0d-252">_invalid callable_</span></span>
 `Array['T]` | `'T[0]`

<span data-ttu-id="1dd0d-253">튜플 형식은 요소에 의해 초기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-253">Tuple types are initialized element-by-element.</span></span>


### <a name="array-elements"></a><span data-ttu-id="1dd0d-254">배열 요소</span><span class="sxs-lookup"><span data-stu-id="1dd0d-254">Array Elements</span></span>

<span data-ttu-id="1dd0d-255">배열 식과 식이 지정 된 경우 `Int` `[` 및 `]` 배열 요소 연산자를 사용 하 여 새 식을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-255">Given an array expression and an `Int` expression, a new expression may be formed using the `[` and `]` array element operator.</span></span>
<span data-ttu-id="1dd0d-256">새 식은 배열의 요소 형식과 동일한 형식이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-256">The new expression will be the same type as the element type of the array.</span></span>
<span data-ttu-id="1dd0d-257">예를 들어, `a` 가 s의 배열에 바인딩되면은 `Double` 식입니다 `a[4]` `Double` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-257">For instance, if `a` is bound to an array of `Double`s, then `a[4]` is a `Double` expression.</span></span>

<span data-ttu-id="1dd0d-258">배열 식이 단순 식별자가 아니면 요소를 선택 하기 위해 괄호로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-258">If the array expression is not a simple identifier, it must be enclosed in parentheses in order to select an element.</span></span>
<span data-ttu-id="1dd0d-259">예를 들어 `a` 및 `b` 가 모두 s의 배열인 경우 `Int` 연결의 요소가 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-259">For instance, if `a` and `b` are both arrays of `Int`s, an element from the concatenation would be expressed as:</span></span>

```qsharp
(a + b)[13]
```

<span data-ttu-id="1dd0d-260">Q #의 모든 배열은 0부터 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-260">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="1dd0d-261">즉, 배열의 첫 번째 요소는 `a` 항상 `a[0]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-261">That is, the first element of an array `a` is always `a[0]`.</span></span>


### <a name="array-slices"></a><span data-ttu-id="1dd0d-262">배열 조각</span><span class="sxs-lookup"><span data-stu-id="1dd0d-262">Array Slices</span></span>

<span data-ttu-id="1dd0d-263">배열 식과 식이 지정 된 경우 `Range` `[` 및 `]` 배열 조각 연산자를 사용 하 여 새 식을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-263">Given an array expression and a `Range` expression, a new expression may be formed using the `[` and `]` array slice operator.</span></span>
<span data-ttu-id="1dd0d-264">새 식은 배열과 동일한 형식이 되며의 요소에 의해 인덱싱된 배열 항목이 `Range` 에 정의 된 순서 대로 포함 됩니다 `Range` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-264">The new expression will be the same type as the array and will contain the array items indexed by the elements of the `Range`, in the order defined by the `Range`.</span></span>
<span data-ttu-id="1dd0d-265">예를 들어, `a` 가 s의 배열에 바인딩된 경우는 `Double` `a[3..-1..0]` `Double[]` 의 처음 4 개 요소를 포함 `a` 하지만에 표시 되는 역순으로를 포함 하는 식입니다 `a` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-265">For instance, if `a` is bound to an array of `Double`s, then `a[3..-1..0]` is a `Double[]` expression that contains the first four elements of `a` but in the reverse order as they appear in `a`.</span></span>

<span data-ttu-id="1dd0d-266">`Range`이 비어 있으면 결과 배열 조각의 길이가 0이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-266">If the `Range` is empty, then the resulting array slice will be zero length.</span></span>

<span data-ttu-id="1dd0d-267">참조 하는 배열 요소와 마찬가지로, 배열 식이 단순 식별자가 아니면 조각화 하기 위해 괄호로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-267">Just as with referencing array elements, if the array expression is not a simple identifier, it must be enclosed it parentheses in order to slice.</span></span>
<span data-ttu-id="1dd0d-268">`a`및 `b` 가 모두 s 배열인 경우 `Int` 연결의 조각이 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-268">If `a` and `b` are both arrays of `Int`s, a slice from the concatenation would be expressed as:</span></span>

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a><span data-ttu-id="1dd0d-269">유추 된 시작/끝 값</span><span class="sxs-lookup"><span data-stu-id="1dd0d-269">Inferred start/end values</span></span>

<span data-ttu-id="1dd0d-270">0.8 릴리스부터는 범위 조각화를 위한 상황별 식을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-270">Starting with our 0.8 release, we support contextual expressions for range slicing.</span></span> <span data-ttu-id="1dd0d-271">특히 범위 분할 식의 컨텍스트에서는 범위 시작 값과 끝 값을 생략할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-271">In particular, range start and end values may be omitted in the context of a range slicing expression.</span></span> <span data-ttu-id="1dd0d-272">이 경우 컴파일러는 범위에 대해 의도 된 구분 기호를 유추 하기 위해 다음 규칙을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-272">In that case, the compiler will apply the following rules to infer the intended delimiters for the range.</span></span> 

<span data-ttu-id="1dd0d-273">예를 들어 range start 값을 생략 하면 유추 된 시작 값이</span><span class="sxs-lookup"><span data-stu-id="1dd0d-273">For example, if the range start value is omitted,  then the inferred start value</span></span> 
- <span data-ttu-id="1dd0d-274">지정 된 단계가 없거나 지정 된 단계가 양수 이면 0이 고, 그렇지 않으면입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-274">is zero if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="1dd0d-275">지정 된 단계가 음수인 경우 분리 된 배열의 길이에서 1을 뺀 값입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-275">is the length of sliced array minus one if the specified step is negative.</span></span> 

<span data-ttu-id="1dd0d-276">범위 끝 값이 생략 된 경우에는 유추 된 끝 값이</span><span class="sxs-lookup"><span data-stu-id="1dd0d-276">If the range end value is omitted,  then the inferred end value</span></span> 
- <span data-ttu-id="1dd0d-277">지정 된 단계가 없고 지정 된 단계가 양수인 경우 분리 된 배열의 길이가 1을 뺀 값입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-277">is the length of sliced array minus one if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="1dd0d-278">지정 된 단계가 음수 이면 0이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-278">is zero if the specified step is negative.</span></span> 

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

### <a name="copy-and-update-expressions"></a><span data-ttu-id="1dd0d-279">복사 및 업데이트 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-279">Copy-and-Update Expressions</span></span>

<span data-ttu-id="1dd0d-280">모든 Q # 형식은 값 형식이 며,이는 모든 것이 특별 한 역할을 수행 하기 때문에 값이 기호에 바인딩되거나 기호가 바인딩 되었을 때 "copy"가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-280">Since all Q# types are value types — with the qubits taking a somewhat special role —formally a "copy" is created when a value is bound to a symbol, or when a symbol is rebound.</span></span> <span data-ttu-id="1dd0d-281">즉, Q #의 동작은 할당 시 복사본이 생성 된 경우와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-281">That is to say, the behavior of Q# is the same as if a copy were created on assignment.</span></span>
<span data-ttu-id="1dd0d-282">물론 관련 된 부분만 실제로 필요에 따라 다시 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-282">Of course in practice only the relevant pieces are actually recreated as needed.</span></span> 

<span data-ttu-id="1dd0d-283">특히 배열도 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-283">This in particular also includes arrays.</span></span>
<span data-ttu-id="1dd0d-284">특히 배열 항목을 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-284">In particular, it is not possible to update array items.</span></span> <span data-ttu-id="1dd0d-285">기존 배열을 수정 하려면 *복사 및 업데이트* 메커니즘을 활용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-285">To modify an existing array requires leveraging a *copy-and-update* mechanism.</span></span>

<span data-ttu-id="1dd0d-286">기존 배열에서 *복사 및 업데이트* 식을 통해 새 배열을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-286">New arrays can be created from existing ones via *copy-and-update* expressions.</span></span>
<span data-ttu-id="1dd0d-287">복사 및 업데이트 식은 형식의 식이 며 `expression1 w/ expression2 <- expression3` , 여기서은 `expression1` `T[]` 특정 형식의 형식 이어야 `T` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-287">A copy-and-update expression is an expression of the form `expression1 w/ expression2 <- expression3`, where `expression1` has to be of type `T[]` for some type `T`.</span></span>
<span data-ttu-id="1dd0d-288">두 번째는 `expression2` 에서 배열과 비교 하 여 수정할 요소의 인덱스를 정의 하 고, 형식 또는 형식 중 `expression1` 하나 여야 `Int` `Range` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-288">The second `expression2` defines the indices of the element(s) to modify compared to the array in `expression1` and has to be either of type `Int` or of type `Range`.</span></span>
<span data-ttu-id="1dd0d-289">`expression2`가 형식이 면은 `Int` `expression3` 형식 이어야 `T` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-289">If `expression2` is of type `Int`, `expression3` has to be of type `T`.</span></span> <span data-ttu-id="1dd0d-290">`expression2`가 형식이 면은 `Range` `expression3` 형식 이어야 `T[]` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-290">If `expression2` is of type `Range`, `expression3` has to be of type `T[]`.</span></span>

<span data-ttu-id="1dd0d-291">복사 및 업데이트 식은의 `arr w/ idx <- value` 해당 요소로 설정 된 모든 요소를 포함 하는 새 배열을 생성 합니다 .이 요소는의 요소를 제외 하 고는의 해당 요소로 `arr` `idx` 설정 됩니다 `value` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-291">A copy-and-update expression `arr w/ idx <- value` constructs a new array with all elements set to the corresponding element in `arr`, except for the element(s) at `idx`, which are set to the one(s) in `value`.</span></span> <span data-ttu-id="1dd0d-292">예를 들어에 `arr` 배열이 포함 된 `[0,1,2,3]` 경우</span><span class="sxs-lookup"><span data-stu-id="1dd0d-292">For example, if `arr` contains an array `[0,1,2,3]`, then</span></span> 
- <span data-ttu-id="1dd0d-293">`arr w/ 0 <- 10`는 배열 `[10,1,2,3]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-293">`arr w/ 0 <- 10` is the array `[10,1,2,3]`.</span></span>
- <span data-ttu-id="1dd0d-294">`arr w/ 2 <- 10`는 배열 `[0,1,10,3]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-294">`arr w/ 2 <- 10` is the array `[0,1,10,3]`.</span></span>
- <span data-ttu-id="1dd0d-295">`arr w/ 0..2..3 <- [10,12]`는 배열 `[10,1,12,3]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-295">`arr w/ 0..2..3 <- [10,12]` is the array `[10,1,12,3]`.</span></span>

#### <a name="copy-and-update-expressions-for-named-items"></a><span data-ttu-id="1dd0d-296">명명 된 항목에 대 한 복사 및 업데이트 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-296">Copy-and-update expressions for named items</span></span>

<span data-ttu-id="1dd0d-297">사용자 정의 형식에 명명 된 항목에 대 한 유사한 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-297">Similar expressions exist for named items in user-defined types.</span></span> 

<span data-ttu-id="1dd0d-298">예를 들어 형식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-298">Consider for example the type</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="1dd0d-299">에 `c` 형식의 값이 포함 된 경우 `Complex(1., -1.)` `c w/ Re <- 0.` 는 `Complex` 로 계산 되는 형식의 식입니다 `Complex(0., -1.)` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-299">If `c` contains the value of type `Complex(1., -1.)`, then `c w/ Re <- 0.` is an expression of type `Complex` that evaluates to `Complex(0., -1.)`.</span></span>

### <a name="jagged-arrays"></a><span data-ttu-id="1dd0d-300">가변 배열</span><span class="sxs-lookup"><span data-stu-id="1dd0d-300">Jagged Arrays</span></span>

<span data-ttu-id="1dd0d-301">"배열의 배열"이 라고도 하는 가변 배열은 요소가 배열인 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-301">A jagged array, sometimes called an "array of arrays," is an array whose elements are arrays.</span></span>
<span data-ttu-id="1dd0d-302">가변 배열의 요소는 크기가 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-302">The elements of a jagged array can be of different sizes.</span></span>
<span data-ttu-id="1dd0d-303">다음 예에서는 곱하기 테이블을 나타내는 가변 배열을 선언 하 고 초기화 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-303">The following example shows how to declare and initialize a jagged array representing a multiplication table.</span></span>

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

### <a name="arrays-of-callables"></a><span data-ttu-id="1dd0d-304">Callables 배열</span><span class="sxs-lookup"><span data-stu-id="1dd0d-304">Arrays of callables</span></span> 

<span data-ttu-id="1dd0d-305">호출 가능 형식에 대 한 자세한 내용은 다음 페이지, [Q #의 작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions)에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-305">Note that more details on callable types can be found below, as well as on the next page, [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

<span data-ttu-id="1dd0d-306">공통 요소 형식이 작업 또는 함수 형식이 면 모든 요소에 동일한 입력 및 출력 형식이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-306">If the common element type is an operation or function type, all of the elements must have the same input and output types.</span></span>
<span data-ttu-id="1dd0d-307">배열의 요소 형식은 모든 요소에서 지원 되는 모든 함수을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-307">The element type of the array will support any functors that are supported by all of the elements.</span></span>
<span data-ttu-id="1dd0d-308">예를 들어, `Op1` `Op2` 및 `Op3` 모두가 이지만,를 `Qubit[] => Unit` `Op1` 지원 하 `Adjoint` `Op2` `Controlled` 고 `Op3` 를 지원 하며를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-308">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[] => Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="1dd0d-309">`[Op1, Op2]`는 작업의 배열입니다 `(Qubit[] => Unit)` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-309">`[Op1, Op2]` is an array of `(Qubit[] => Unit)` operations.</span></span>
- <span data-ttu-id="1dd0d-310">`[Op1, Op3]`는 작업의 배열입니다 `(Qubit[] => Unit is Adj)` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-310">`[Op1, Op3]` is an array of `(Qubit[] => Unit is Adj)` operations.</span></span>
- <span data-ttu-id="1dd0d-311">`[Op2, Op3]`는 작업의 배열입니다 `(Qubit[] => Unit is Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-311">`[Op2, Op3]` is an array of `(Qubit[] => Unit is Ctl)` operations.</span></span>

<span data-ttu-id="1dd0d-312">그러나 `(Qubit[] => Unit is Adj)` 및 `(Qubit[] => Unit is Ctl)` 작업의 공통 기본 형식은 이지만 `(Qubit[] => Unit)` 이러한 연산자 *의* 배열은 공통 기본 형식을 공유 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-312">However, while `(Qubit[] => Unit is Adj)` and  `(Qubit[] => Unit is Ctl)` operations have the common base type of `(Qubit[] => Unit)`, note that arrays *of* these operators do not share a common base type.</span></span> <span data-ttu-id="1dd0d-313">예를 들어는 `[[Op1], [Op2]]` 호환 되지 않는 배열 형식 및의 배열을 만들려고 하기 때문에 현재 오류를 발생 시킵니다 `(Qubit[] => Unit is Adj)[]` `(Qubit[] => Unit is Ctl)[]` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-313">For example, `[[Op1], [Op2]]` would currently raise an error because it is attempting to create an array of the incompatible array types `(Qubit[] => Unit is Adj)[]` and `(Qubit[] => Unit is Ctl)[]`.</span></span>


## <a name="conditional-expressions"></a><span data-ttu-id="1dd0d-314">조건 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-314">Conditional Expressions</span></span>

<span data-ttu-id="1dd0d-315">동일한 형식 및 부울 식의 다른 두 식이 지정 된 경우 물음표 및 세로 막대를 사용 하 여 조건 식을 지정할 수 있습니다 `?` `|` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-315">Given two other expressions of the same type and a Boolean expression, the conditional expression may be formed using the question mark `?` and the vertical bar `|`.</span></span>
<span data-ttu-id="1dd0d-316">예를 들면 `a==b ? c | d` 입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-316">For instance, `a==b ? c | d`.</span></span>
<span data-ttu-id="1dd0d-317">이 예에서는 조건식의 값이 true 이면이 고, `c` 그렇지 `a==b` `d` 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-317">In this example, the value of the conditional expression will be `c` if `a==b` is true and `d` if it is false.</span></span>

### <a name="conditional-expressions-with-callables"></a><span data-ttu-id="1dd0d-318">Callables 사용 조건 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-318">Conditional expressions with callables</span></span>

<span data-ttu-id="1dd0d-319">두 식은 동일한 입력 및 출력을 포함 하는 작업으로 평가 될 수 있지만 다른 함수을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-319">The two expressions may evaluate to operations that have the same inputs and outputs but support different functors.</span></span>
<span data-ttu-id="1dd0d-320">이 경우 조건식의 형식은 두 식에서 지원 되는 모든 함수를 지 원하는 입력 및 출력을 사용 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-320">In this case, the type of the conditional expression is an operation with those inputs and outputs that supports any functors supported by both expressions.</span></span>
<span data-ttu-id="1dd0d-321">예를 들어, `Op1` `Op2` 및 `Op3` 모두가 이지만,를 `Qubit[]=>Unit` `Op1` 지원 하 `Adjoint` `Op2` `Controlled` 고 `Op3` 를 지원 하며를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-321">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[]=>Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="1dd0d-322">`flag ? Op1 | Op2`은 `(Qubit[] => Unit)` 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-322">`flag ? Op1 | Op2` is a `(Qubit[] => Unit)` operation.</span></span>
- <span data-ttu-id="1dd0d-323">`flag ? Op1 | Op3`은 `(Qubit[] => Unit is Adj)` 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-323">`flag ? Op1 | Op3` is a `(Qubit[] => Unit is Adj)` operation.</span></span>
- <span data-ttu-id="1dd0d-324">`flag ? Op2 | Op3`은 `(Qubit[] => Unit is Ctl)` 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-324">`flag ? Op2 | Op3` is a `(Qubit[] => Unit is Ctl)` operation.</span></span>

<span data-ttu-id="1dd0d-325">가능한 두 결과 식 중 하나에 함수 또는 작업 호출이 포함 된 경우 해당 호출은 호출의 값이 되는 경우에만 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-325">If either of the two possible result expressions include a function or operation call, that call will only take place if that result is the one that will be the value of the call.</span></span>
<span data-ttu-id="1dd0d-326">예를 들어, `a==b ? C(qs) | D(qs)` `a==b` 이 true 이면 `C` 작업이 호출 되 고 false 인 경우에만 `D` 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-326">For instance, in the case `a==b ? C(qs) | D(qs)`, if `a==b` is true then the `C` operation will be invoked, and if it is false then only `D` will be invoked.</span></span>
<span data-ttu-id="1dd0d-327">이는 다른 언어의 단락과 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-327">This is similar to short-circuiting in other languages.</span></span>

## <a name="callable-expressions"></a><span data-ttu-id="1dd0d-328">호출 가능 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-328">Callable Expressions</span></span>

<span data-ttu-id="1dd0d-329">호출 가능 리터럴은 컴파일 범위에서 정의 된 작업 또는 함수의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-329">A callable literal is the name of an operation or function defined in the compilation scope.</span></span>
<span data-ttu-id="1dd0d-330">예를 들어 `X` 는 표준 라이브러리 작업을 참조 하는 작업 리터럴이어야,는 `X` `Message` 표준 라이브러리 함수를 참조 하는 함수 리터럴입니다 `Message` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-330">For instance, `X` is an operation literal that refers to the standard library `X` operation, and `Message` is a function literal that refers to the standard library `Message` function.</span></span>

<span data-ttu-id="1dd0d-331">작업에서 함수를 지 원하는 경우 `Adjoint` `Adjoint op` 는 연산 식입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-331">If an operation supports the `Adjoint` functor, then `Adjoint op` is an operation expression.</span></span>
<span data-ttu-id="1dd0d-332">마찬가지로 작업에서 함수를 지 원하는 경우 `Controlled` `Controlled op` 는 연산 식입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-332">Similarly, if the operation supports the `Controlled` functor, then `Controlled op` is an operation expression.</span></span>
<span data-ttu-id="1dd0d-333">이러한 식의 형식은 [작업 특수화 호출](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations)시 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-333">The types of these expressions are specified at [Calling operation specializations](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).</span></span>

<span data-ttu-id="1dd0d-334">함수 ( `Adjoint` 및 `Controlled` )은 `!` [] '로 래핑 연산자 및 배열 인덱싱을 제외 하 고 다른 모든 연산자 보다 더 가깝게 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-334">Functors (`Adjoint` and `Controlled`) bind more closely than all other operators, except for the unwrap operator `!` and array indexing with []\`.</span></span>
<span data-ttu-id="1dd0d-335">따라서 다음은 작업에서 사용 되는 함수를 지원 한다고 가정 하 여 모든 법률입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-335">Thus, the following are all legal, assuming that the operations support the functors used:</span></span>

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a><span data-ttu-id="1dd0d-336">형식 매개 변수가 있는 호출 가능 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-336">Type-parameterized callable expressions</span></span>

<span data-ttu-id="1dd0d-337">호출 가능 리터럴은 값으로 사용 될 수 있습니다. 예를 들어 변수에 할당 하거나 다른 호출 가능으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-337">A callable literal may be used as a value, say to assign to a variable or to pass to another callable.</span></span>
<span data-ttu-id="1dd0d-338">이 경우 호출 가능에 [형식 매개 변수가 있으면 해당 매개 변수](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables)를 호출 가능 값의 일부로 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-338">In this case, if the callable has [type parameters](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), they must be provided as part of the callable value.</span></span>
<span data-ttu-id="1dd0d-339">호출 가능 값은 지정 되지 않은 형식 매개 변수를 가질 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-339">A callable value cannot have any unspecified type parameters.</span></span>

<span data-ttu-id="1dd0d-340">예를 들어 `Fun` 가 시그니처를 사용 하는 함수인 경우는 `'T1->Unit` 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-340">For instance, if `Fun` is a function with signature `'T1->Unit`:</span></span>

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a><span data-ttu-id="1dd0d-341">호출 가능 호출 식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-341">Callable Invocation Expressions</span></span>

<span data-ttu-id="1dd0d-342">호출 가능 식의 입력 형식에 대 한 호출 가능 (연산 또는 함수) 식과 튜플 식이 지정 된 경우 호출 식은 튜플 식을 호출 가능 식에 추가 하 여 구성 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-342">Given a callable (operation or function) expression and a tuple expression of the input type of the callable's signature, an invocation expression may be formed by appending the tuple expression to the callable expression.</span></span>
<span data-ttu-id="1dd0d-343">호출 식의 형식은 호출 가능 시그니처의 출력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-343">The type of the invocation expression is the output type of the callable's signature.</span></span>

<span data-ttu-id="1dd0d-344">예를 들어 `Op` 가 서명이 포함 된 작업 인 `((Int, Qubit) => Double)` 경우 `Op(3, qubit1)` 는 형식의 식입니다 `Double` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-344">For example, if `Op` is an operation with signature `((Int, Qubit) => Double)`, `Op(3, qubit1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="1dd0d-345">마찬가지로 `Sin` 가 시그니처를 사용 하는 함수인 `(Double -> Double)` 경우 `Sin(0.1)` 는 형식의 식입니다 `Double` .</span><span class="sxs-lookup"><span data-stu-id="1dd0d-345">Similarly, if `Sin` is a function with signature `(Double -> Double)`, `Sin(0.1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="1dd0d-346">마지막으로 `Builder` 가 시그니처를 사용 하는 함수인 경우 `(Int -> (Int -> Int))` `Builder(3)` 는에서 Int로의 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-346">Finally, if `Builder` is a function with signature `(Int -> (Int -> Int))`, then `Builder(3)` is a function from Into to Int.</span></span>

<span data-ttu-id="1dd0d-347">호출 가능 값 식의 결과를 호출 하려면 호출 가능 식 주위에 괄호 쌍을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-347">Invoking the result of a callable-valued expression requires an extra pair of parentheses around the callable expression.</span></span>
<span data-ttu-id="1dd0d-348">따라서 이전 단락에서 호출 결과를 호출 하려면 `Builder` 올바른 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-348">Thus, to invoke the result of calling `Builder` from the previous paragraph, the correct syntax is:</span></span>

```qsharp
(Builder(3))(2)
```

<span data-ttu-id="1dd0d-349">[형식 매개 변수가 있는](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) 호출 가능를 호출할 때 실제 형식 매개 변수는 꺾쇠 괄호 내에서 `<` `>` 호출 가능 식 뒤에 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-349">When invoking a [type-parameterized](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) callable, the actual type parameters may be specified within angle brackets `<` and `>` after the callable expression.</span></span>
<span data-ttu-id="1dd0d-350">이는 일반적으로 Q # 컴파일러가 실제 형식을 유추 하므로 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-350">This is usually unnecessary as the Q# compiler will infer the actual types.</span></span>
<span data-ttu-id="1dd0d-351">그러나 형식 매개 변수가 있는 인수를 지정 하지 *않은 상태로 두면* [부분 응용 프로그램](xref:microsoft.quantum.guide.operationsfunctions#partial-application) 에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-351">However, it *is* required for [partial application](xref:microsoft.quantum.guide.operationsfunctions#partial-application) if a type-parameterized argument is left unspecified.</span></span>
<span data-ttu-id="1dd0d-352">또한 다른 함수를 사용 하는 작업을 호출할 수 있는 경우에도 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-352">It is also sometimes useful when passing operations with different functor supports to a callable.</span></span>

<span data-ttu-id="1dd0d-353">예를 들어,에 시그니처가 있고,에 시그니처가 있고,가 첫 번째 인수로를 사용 하 여를 호출 하 고,를 `Func` `('T1, 'T2, 'T1) -> 'T2` 세 번째 `Op1` `Op2` `(Qubit[] => Unit is Adj)` `Op3` `(Qubit[] => Unit)` 인수로 호출 하는 시그니처가 `Func` `Op1` `Op2` `Op3` 있는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-353">For instance, if `Func` has signature `('T1, 'T2, 'T1) -> 'T2`, `Op1` and `Op2` have signature `(Qubit[] => Unit is Adj)`, and `Op3` has signature `(Qubit[] => Unit)`, to invoke `Func` with `Op1` as the first argument, `Op2` as the second, and `Op3` as the third:</span></span>

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

<span data-ttu-id="1dd0d-354">및에 다른 형식이 있으므로 형식 사양이 필요 합니다 `Op3` `Op1` . 따라서 컴파일러는 사양을 사용 하지 않고이를 모호 하 게 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-354">The type specification is required because `Op3` and `Op1` have different types, so the compiler will treat this as ambiguous without the specification.</span></span>


## <a name="operator-precedence"></a><span data-ttu-id="1dd0d-355">연산자 우선 순위</span><span class="sxs-lookup"><span data-stu-id="1dd0d-355">Operator Precedence</span></span>

<span data-ttu-id="1dd0d-356">모든 이항 연산자는를 제외 하 고 오른쪽 결합성이 `^` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-356">All binary operators are right-associative, except for `^`.</span></span>

<span data-ttu-id="1dd0d-357">대괄호 및 `[` 는 `]` 배열 조각화 및 인덱싱의 경우 모든 연산자 앞에 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-357">Brackets, `[` and `]`, for array slicing and indexing, bind before any operator.</span></span>

<span data-ttu-id="1dd0d-358">함수 `Adjoint` 및는 `Controlled` 배열 인덱싱 후 다른 모든 연산자 앞에 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-358">The functors `Adjoint` and `Controlled` bind after array indexing but before all other operators.</span></span>

<span data-ttu-id="1dd0d-359">연산 및 함수 호출에 대 한 괄호는 모든 연산자 앞에, 배열 인덱싱 및 함수 후에도 바인딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-359">Parentheses for operation and function invocation also bind before any operator but after array indexing and functors.</span></span>

<span data-ttu-id="1dd0d-360">우선 순위 순으로 최고에서 최저 순으로 연산자.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-360">Operators in order of precedence, from highest to lowest:</span></span>

<span data-ttu-id="1dd0d-361">연산자</span><span class="sxs-lookup"><span data-stu-id="1dd0d-361">Operator</span></span> | <span data-ttu-id="1dd0d-362">숫자</span><span class="sxs-lookup"><span data-stu-id="1dd0d-362">Arity</span></span> | <span data-ttu-id="1dd0d-363">설명</span><span class="sxs-lookup"><span data-stu-id="1dd0d-363">Description</span></span> | <span data-ttu-id="1dd0d-364">피연산자 형식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-364">Operand Types</span></span>
---------|----------|---------|---------------
 <span data-ttu-id="1dd0d-365">붙이지`!`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-365">trailing `!`</span></span> | <span data-ttu-id="1dd0d-366">단항 연산자</span><span class="sxs-lookup"><span data-stu-id="1dd0d-366">Unary</span></span> | <span data-ttu-id="1dd0d-367">래핑 취소</span><span class="sxs-lookup"><span data-stu-id="1dd0d-367">Unwrap</span></span> | <span data-ttu-id="1dd0d-368">사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-368">Any user-defined type</span></span>
 <span data-ttu-id="1dd0d-369">`-`, `~~~`, `not`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-369">`-`, `~~~`, `not`</span></span> | <span data-ttu-id="1dd0d-370">단항 연산자</span><span class="sxs-lookup"><span data-stu-id="1dd0d-370">Unary</span></span> | <span data-ttu-id="1dd0d-371">숫자 음수, 비트 보수, 논리 부정</span><span class="sxs-lookup"><span data-stu-id="1dd0d-371">Numeric negative, bitwise complement, logical negation</span></span> | <span data-ttu-id="1dd0d-372">`Int`,의 경우,,의 경우,의 경우 `BigInt` `Double` `-` `Int` `BigInt` `~~~` `Bool``not`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-372">`Int`, `BigInt` or `Double` for `-`, `Int` or `BigInt` for `~~~`, `Bool` for `not`</span></span>
 `^` | <span data-ttu-id="1dd0d-373">이진</span><span class="sxs-lookup"><span data-stu-id="1dd0d-373">Binary</span></span> | <span data-ttu-id="1dd0d-374">정수 거듭제곱</span><span class="sxs-lookup"><span data-stu-id="1dd0d-374">Integer power</span></span> | <span data-ttu-id="1dd0d-375">`Int`또는 기준의 경우 지 수의 경우입니다. `BigInt` `Int`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-375">`Int` or `BigInt` for the base, `Int` for the exponent</span></span>
 <span data-ttu-id="1dd0d-376">`/`, `*`, `%`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-376">`/`, `*`, `%`</span></span> | <span data-ttu-id="1dd0d-377">이진</span><span class="sxs-lookup"><span data-stu-id="1dd0d-377">Binary</span></span> | <span data-ttu-id="1dd0d-378">나누기, 곱하기, 정수 모듈러스</span><span class="sxs-lookup"><span data-stu-id="1dd0d-378">Division, multiplication, integer modulus</span></span> | <span data-ttu-id="1dd0d-379">`Int`,,, 또는 `BigInt` `Double` `/` `*` `Int` `BigInt` 의 경우`%`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-379">`Int`, `BigInt` or `Double` for `/` and `*`, `Int` or `BigInt` for `%`</span></span>
 <span data-ttu-id="1dd0d-380">`+`, `-`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-380">`+`, `-`</span></span> | <span data-ttu-id="1dd0d-381">이진</span><span class="sxs-lookup"><span data-stu-id="1dd0d-381">Binary</span></span> | <span data-ttu-id="1dd0d-382">더하기 또는 문자열 및 배열 연결, 빼기</span><span class="sxs-lookup"><span data-stu-id="1dd0d-382">Addition or string and array concatenation, subtraction</span></span> | <span data-ttu-id="1dd0d-383">`Int`,, `BigInt` 또는 `Double` `String` 에 대 한 배열 형식입니다.`+`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-383">`Int`, `BigInt` or `Double`, additionally `String` or any array type for `+`</span></span>
 <span data-ttu-id="1dd0d-384">`<<<`, `>>>`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-384">`<<<`, `>>>`</span></span> | <span data-ttu-id="1dd0d-385">이진</span><span class="sxs-lookup"><span data-stu-id="1dd0d-385">Binary</span></span> | <span data-ttu-id="1dd0d-386">왼쪽 시프트, 오른쪽 시프트</span><span class="sxs-lookup"><span data-stu-id="1dd0d-386">Left shift, right shift</span></span> | <span data-ttu-id="1dd0d-387">`Int` 또는 `BigInt`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-387">`Int` or `BigInt`</span></span>
 <span data-ttu-id="1dd0d-388">`<`, `<=`, `>`, `>=`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-388">`<`, `<=`, `>`, `>=`</span></span> | <span data-ttu-id="1dd0d-389">이진</span><span class="sxs-lookup"><span data-stu-id="1dd0d-389">Binary</span></span> | <span data-ttu-id="1dd0d-390">보다 작음, 작거나 같음, 보다 큼, 보다 큼, 크거나 같음 비교</span><span class="sxs-lookup"><span data-stu-id="1dd0d-390">Less-than, less-than-or-equal, greater-than, greater-than-or-equal comparisons</span></span> | <span data-ttu-id="1dd0d-391">`Int`, `BigInt` 또는`Double`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-391">`Int`, `BigInt` or `Double`</span></span>
 <span data-ttu-id="1dd0d-392">`==`, `!=`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-392">`==`, `!=`</span></span> | <span data-ttu-id="1dd0d-393">이진</span><span class="sxs-lookup"><span data-stu-id="1dd0d-393">Binary</span></span> | <span data-ttu-id="1dd0d-394">같음, 같지 않음 비교</span><span class="sxs-lookup"><span data-stu-id="1dd0d-394">equal, not-equal comparisons</span></span> | <span data-ttu-id="1dd0d-395">모든 기본 형식</span><span class="sxs-lookup"><span data-stu-id="1dd0d-395">any primitive type</span></span>
 `&&&` | <span data-ttu-id="1dd0d-396">이진</span><span class="sxs-lookup"><span data-stu-id="1dd0d-396">Binary</span></span> | <span data-ttu-id="1dd0d-397">비트 AND</span><span class="sxs-lookup"><span data-stu-id="1dd0d-397">Bitwise AND</span></span> | <span data-ttu-id="1dd0d-398">`Int` 또는 `BigInt`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-398">`Int` or `BigInt`</span></span>
 `^^^` | <span data-ttu-id="1dd0d-399">이진</span><span class="sxs-lookup"><span data-stu-id="1dd0d-399">Binary</span></span> | <span data-ttu-id="1dd0d-400">비트 XOR</span><span class="sxs-lookup"><span data-stu-id="1dd0d-400">Bitwise XOR</span></span> | <span data-ttu-id="1dd0d-401">`Int` 또는 `BigInt`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-401">`Int` or `BigInt`</span></span>
 <code>\|\|\|</code> | <span data-ttu-id="1dd0d-402">이진</span><span class="sxs-lookup"><span data-stu-id="1dd0d-402">Binary</span></span> | <span data-ttu-id="1dd0d-403">비트 OR</span><span class="sxs-lookup"><span data-stu-id="1dd0d-403">Bitwise OR</span></span> | <span data-ttu-id="1dd0d-404">`Int` 또는 `BigInt`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-404">`Int` or `BigInt`</span></span>
 `and` | <span data-ttu-id="1dd0d-405">이진</span><span class="sxs-lookup"><span data-stu-id="1dd0d-405">Binary</span></span> | <span data-ttu-id="1dd0d-406">논리적 AND</span><span class="sxs-lookup"><span data-stu-id="1dd0d-406">Logical AND</span></span> | `Bool`
 `or` | <span data-ttu-id="1dd0d-407">이진</span><span class="sxs-lookup"><span data-stu-id="1dd0d-407">Binary</span></span> | <span data-ttu-id="1dd0d-408">논리적 OR</span><span class="sxs-lookup"><span data-stu-id="1dd0d-408">Logical OR</span></span> | `Bool`
 `..` | <span data-ttu-id="1dd0d-409">Binary/삼항</span><span class="sxs-lookup"><span data-stu-id="1dd0d-409">Binary/Ternary</span></span> | <span data-ttu-id="1dd0d-410">Range 연산자</span><span class="sxs-lookup"><span data-stu-id="1dd0d-410">Range operator</span></span> | `Int`
 <span data-ttu-id="1dd0d-411">`?` `|`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-411">`?` `|`</span></span> | <span data-ttu-id="1dd0d-412">진</span><span class="sxs-lookup"><span data-stu-id="1dd0d-412">Ternary</span></span> | <span data-ttu-id="1dd0d-413">조건부</span><span class="sxs-lookup"><span data-stu-id="1dd0d-413">Conditional</span></span> | <span data-ttu-id="1dd0d-414">`Bool`왼쪽의 경우</span><span class="sxs-lookup"><span data-stu-id="1dd0d-414">`Bool` for the left-hand-side</span></span>
<span data-ttu-id="1dd0d-415">`w/` `<-`</span><span class="sxs-lookup"><span data-stu-id="1dd0d-415">`w/` `<-`</span></span> | <span data-ttu-id="1dd0d-416">진</span><span class="sxs-lookup"><span data-stu-id="1dd0d-416">Ternary</span></span> | <span data-ttu-id="1dd0d-417">복사 및 업데이트</span><span class="sxs-lookup"><span data-stu-id="1dd0d-417">Copy-and-update</span></span> | <span data-ttu-id="1dd0d-418">[복사 및 업데이트 식](#copy-and-update-expressions) 참조</span><span class="sxs-lookup"><span data-stu-id="1dd0d-418">see [copy-and-update expressions](#copy-and-update-expressions)</span></span>

## <a name="next-steps"></a><span data-ttu-id="1dd0d-419">다음 단계</span><span class="sxs-lookup"><span data-stu-id="1dd0d-419">Next steps</span></span>

<span data-ttu-id="1dd0d-420">이제 Q #에서 식 작업을 수행할 수 있으므로 [q #의 작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions) 를 사용 하 여 작업 및 함수를 정의 하 고 호출 하는 방법을 배울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd0d-420">Now that you can work with expressions in Q#, you can head to [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions) to learn how to define and call operations and functions.</span></span>
