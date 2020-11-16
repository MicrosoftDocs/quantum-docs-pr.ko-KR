---
title: '식의 Q#'
description: '에서 상수, 변수, 연산자, 작업 및 함수를 식으로 지정, 참조 및 결합 하는 방법을 이해 Q# 합니다.'
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: e95a7cb9b74136ef9a6f51b4bbc32d1d93c43a0d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691592"
---
# <a name="expressions-in-no-locq"></a><span data-ttu-id="5526f-103">식의 Q#</span><span class="sxs-lookup"><span data-stu-id="5526f-103">Expressions in Q#</span></span>

## <a name="numeric-expressions"></a><span data-ttu-id="5526f-104">숫자 식</span><span class="sxs-lookup"><span data-stu-id="5526f-104">Numeric Expressions</span></span>

<span data-ttu-id="5526f-105">숫자 식은, 또는 형식의 식 `Int` 입니다 `BigInt` `Double` .</span><span class="sxs-lookup"><span data-stu-id="5526f-105">Numeric expressions are expressions of type `Int`, `BigInt`, or `Double`.</span></span>
<span data-ttu-id="5526f-106">즉, 정수 또는 부동 소수점 숫자 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-106">That is, they are either integer or floating-point numbers.</span></span>

<span data-ttu-id="5526f-107">`Int` 의 리터럴은 Q# 숫자 시퀀스로 작성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-107">`Int` literals in Q# are written as a sequence of digits.</span></span>
<span data-ttu-id="5526f-108">16 진수 및 이진 정수는 `0x` 각각 및 접두사를 사용 하 여 지원 되 고 작성 됩니다 `0b` .</span><span class="sxs-lookup"><span data-stu-id="5526f-108">Hexadecimal and binary integers are supported and written with a `0x` and `0b` prefix, respectively.</span></span>

<span data-ttu-id="5526f-109">`BigInt` 의 리터럴에 Q# 는 후행 `l` 또는 `L` 접미사가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-109">`BigInt` literals in Q# have a trailing `l` or `L` suffix.</span></span>
<span data-ttu-id="5526f-110">16 진수 큰 정수는 "0x" 접두사를 사용 하 여 지원 되 고 작성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-110">Hexadecimal big integers are supported and written with a "0x" prefix.</span></span>
<span data-ttu-id="5526f-111">따라서 다음은 리터럴의 모든 유효한 사용입니다 `BigInt` .</span><span class="sxs-lookup"><span data-stu-id="5526f-111">Thus, the following are all valid uses of `BigInt` literals:</span></span>

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

<span data-ttu-id="5526f-112">`Double` 의 리터럴은 Q# 10 진수를 사용 하 여 작성 된 부동 소수점 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-112">`Double` literals in Q# are floating-point numbers written using decimal digits.</span></span>
<span data-ttu-id="5526f-113">소수점 또는 ' `.` e ' 또는 ' e '로 표시 된 지 수 부분 (음수 부호와 소수 자릿수가 유효 함)을 사용 하거나 사용 하지 않고 쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-113">They can be written with or without a decimal point, `.`, or an exponential part indicated with 'e' or 'E' (after which only a possible negative sign and decimal digits are valid).</span></span>
<span data-ttu-id="5526f-114">유효한 `Double` 리터럴은 `0.0` , `1.2e5` , `1e-5` 입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-114">The following are valid `Double` literals: `0.0`, `1.2e5`, `1e-5`.</span></span>

<span data-ttu-id="5526f-115">모든 요소 형식의 배열 식이 지정 된 경우 `Int` 기본 제공 함수를 사용 하 여 식을 구성 하 고 [`Length`](xref:Microsoft.Quantum.Core.Length) 배열 식이 괄호로 묶여 있게 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-115">Given an array expression of any element type, you can form an `Int` expression using the [`Length`](xref:Microsoft.Quantum.Core.Length) built-in function, with the array expression enclosed in parentheses.</span></span>
<span data-ttu-id="5526f-116">예를 들어 `a` 가 배열에 바인딩된 경우 `Length(a)` 는 정수 식입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-116">For example, if `a` is bound to an array, then `Length(a)` is an integer expression.</span></span>
<span data-ttu-id="5526f-117">`b`가 정수 배열의 배열인 경우는 `Int[][]` `Length(b)` 의 하위 배열 수이 `b` 고 `Length(b[1])` 은의 두 번째 하위 배열에 있는 정수 수입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="5526f-117">If `b` is an array of arrays of integers, `Int[][]`, then `Length(b)` is the number of sub-arrays in `b`, and `Length(b[1])` is the number of integers in the second sub-array in `b`.</span></span>

<span data-ttu-id="5526f-118">동일한 형식의 두 숫자 식이 지정 된 경우 이항 연산자 `+` , `-` , 및를 `*` `/` 사용 하 여 새 숫자 식을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-118">Given two numeric expressions of the same type, the binary operators `+`, `-`, `*`, and `/` may be used to form a new numeric expression.</span></span>
<span data-ttu-id="5526f-119">새 식의 형식은 구성 식의 형식과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-119">The type of the new expression is the same as the types of the constituent expressions.</span></span>

<span data-ttu-id="5526f-120">두 개의 정수 식이 지정 된 경우 이항 연산자 `^` (power)를 사용 하 여 새 정수 식을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-120">Given two integer expressions, use the binary operator `^` (power) to form a new integer expression.</span></span>
<span data-ttu-id="5526f-121">마찬가지로 두 개의 double 식에를 사용 `^` 하 여 새 double 식을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-121">Similarly, you can also use `^` with two double expressions to form a new double expression.</span></span>
<span data-ttu-id="5526f-122">마지막으로 왼쪽에 큰 정수를 사용 하 고 오른쪽에 정수를 사용 하 여 `^` 새 큰 정수 식을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-122">Finally, you can use `^` with a big integer on the left and an integer on the right to form a new big integer expression.</span></span>
<span data-ttu-id="5526f-123">이 경우 두 번째 매개 변수는 32 비트에 맞아야 합니다. 그렇지 않으면 런타임 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-123">In this case, the second parameter must fit into 32 bits; if not, it raises a runtime error.</span></span>

<span data-ttu-id="5526f-124">두 개의 정수 또는 큰 정수 식이 지정 된 경우 `%` (모듈러스), `&&&` (비트 and), (비트 or `|||` ) 또는 `^^^` (비트 XOR) 연산자를 사용 하 여 새로운 정수 또는 큰 정수 식을 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-124">Given two integer or big integer expressions, form a new integer or big integer expression using the `%` (modulus), `&&&` (bitwise AND), `|||` (bitwise OR), or `^^^` (bitwise XOR) operators.</span></span>

<span data-ttu-id="5526f-125">왼쪽에 정수 또는 큰 정수 식이 있고 오른쪽에 정수 식이 지정 된 경우 `<<<` (산술 왼쪽 시프트) 또는 `>>>` (산술 오른쪽 시프트) 연산자를 사용 하 여 왼쪽 식과 동일한 형식의 새 식을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-125">Given either an integer or big integer expression on the left, and an integer expression on the right, use the `<<<` (arithmetic left shift) or `>>>` (arithmetic right shift) operators to create a new expression with the same type as the left-hand expression.</span></span>

<span data-ttu-id="5526f-126">이동 작업에 대 한 두 번째 매개 변수 (이동 크기)는 0 보다 크거나 같아야 합니다. 음수 시프트 금액의 동작은 정의 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-126">The second parameter (the shift amount) to either shift operation must be greater than or equal to zero; the behavior for negative shift amounts is undefined.</span></span>
<span data-ttu-id="5526f-127">시프트 연산의 이동 양은 32 비트에도 맞아야 합니다. 그렇지 않으면 런타임 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-127">The shift amount for either shift operation must also fit into 32 bits; if not, it raises a runtime error.</span></span>
<span data-ttu-id="5526f-128">이동 하는 수가 정수 이면 시프트 금액이 해석 됩니다 `mod 64` . 즉, 1과 65의 시프트는 동일한 효과를 가집니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-128">If the number shifted is an integer, then the shift amount is interpreted `mod 64`; that is, a shift of 1 and a shift of 65 have the same effect.</span></span>

<span data-ttu-id="5526f-129">정수 및 큰 정수 값 모두에 대해 시프트는 산술 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-129">For both integer and big integer values, shifts are arithmetic.</span></span>
<span data-ttu-id="5526f-130">음수 값을 왼쪽 또는 오른쪽으로 이동 하면 음수가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-130">Shifting a negative value either left or right results in a negative number.</span></span>
<span data-ttu-id="5526f-131">즉, 한 단계를 왼쪽 또는 오른쪽으로 이동 하는 것은 각각 2로 곱하기 또는 나누기와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-131">That is, shifting one step to the left or right is the same as multiplying or dividing by 2, respectively.</span></span>

<span data-ttu-id="5526f-132">정수 나누기와 정수 모듈러스는 c #과 같은 음수에 대해 동일한 동작을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-132">Integer division and integer modulus follow the same behavior for negative numbers as C#.</span></span> <span data-ttu-id="5526f-133">즉,는 `a % b` 항상와 동일한 부호를 가지 `a` 며 `b * (a / b) + a % b` 항상와 동일 `a` 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-133">That is, `a % b` always has the same sign as `a`, and `b * (a / b) + a % b` always equals `a`.</span></span> <span data-ttu-id="5526f-134">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-134">For example:</span></span>

|`A` | `B` | `A / B` | `A % B`|
|:---------:|:----------:|:---------:|:---------:|
| <span data-ttu-id="5526f-135">5</span><span class="sxs-lookup"><span data-stu-id="5526f-135">5</span></span> | <span data-ttu-id="5526f-136">2</span><span class="sxs-lookup"><span data-stu-id="5526f-136">2</span></span> | <span data-ttu-id="5526f-137">2</span><span class="sxs-lookup"><span data-stu-id="5526f-137">2</span></span> | <span data-ttu-id="5526f-138">1</span><span class="sxs-lookup"><span data-stu-id="5526f-138">1</span></span> |
| <span data-ttu-id="5526f-139">5</span><span class="sxs-lookup"><span data-stu-id="5526f-139">5</span></span> | <span data-ttu-id="5526f-140">-2</span><span class="sxs-lookup"><span data-stu-id="5526f-140">-2</span></span> | <span data-ttu-id="5526f-141">-2</span><span class="sxs-lookup"><span data-stu-id="5526f-141">-2</span></span> | <span data-ttu-id="5526f-142">1</span><span class="sxs-lookup"><span data-stu-id="5526f-142">1</span></span> |
| <span data-ttu-id="5526f-143">-5</span><span class="sxs-lookup"><span data-stu-id="5526f-143">-5</span></span> | <span data-ttu-id="5526f-144">2</span><span class="sxs-lookup"><span data-stu-id="5526f-144">2</span></span> | <span data-ttu-id="5526f-145">-2</span><span class="sxs-lookup"><span data-stu-id="5526f-145">-2</span></span> | <span data-ttu-id="5526f-146">-1</span><span class="sxs-lookup"><span data-stu-id="5526f-146">-1</span></span> |
| <span data-ttu-id="5526f-147">-5</span><span class="sxs-lookup"><span data-stu-id="5526f-147">-5</span></span> | <span data-ttu-id="5526f-148">-2</span><span class="sxs-lookup"><span data-stu-id="5526f-148">-2</span></span> | <span data-ttu-id="5526f-149">2</span><span class="sxs-lookup"><span data-stu-id="5526f-149">2</span></span> | <span data-ttu-id="5526f-150">-1</span><span class="sxs-lookup"><span data-stu-id="5526f-150">-1</span></span> |

<span data-ttu-id="5526f-151">큰 정수 나누기와 모듈러스 연산은 동일한 방식으로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-151">Big integer division and modulus operations work the same way.</span></span>

<span data-ttu-id="5526f-152">숫자 식이 지정 된 경우 단항 연산자를 사용 하 여 새 식을 만들 수 있습니다 `-` .</span><span class="sxs-lookup"><span data-stu-id="5526f-152">Given any numeric expression, you can form a new expression using the `-` unary operator.</span></span>
<span data-ttu-id="5526f-153">새 식은 구성 식과 동일한 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-153">The new expression is the same type as the constituent expression.</span></span>

<span data-ttu-id="5526f-154">정수 또는 큰 정수 식이 지정 된 경우 `~~~` (비트 보수) 단항 연산자를 사용 하 여 동일한 유형의 새 식을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-154">Given any integer or big integer expression, you can form a new expression of the same type using the `~~~` (bitwise complement) unary operator.</span></span>

## <a name="boolean-expressions"></a><span data-ttu-id="5526f-155">부울 식</span><span class="sxs-lookup"><span data-stu-id="5526f-155">Boolean Expressions</span></span>

<span data-ttu-id="5526f-156">두 `Bool` 리터럴 값은 `true` 및 `false` 입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-156">The two `Bool` literal values are `true` and `false`.</span></span>

<span data-ttu-id="5526f-157">동일한 기본 형식의 두 식이 지정 된 경우 `==` 및 `!=` 이항 연산자를 사용 하 여 식을 생성할 수 있습니다 `Bool` .</span><span class="sxs-lookup"><span data-stu-id="5526f-157">Given any two expressions of the same primitive type, the `==` and `!=` binary operators may be used to construct a `Bool` expression.</span></span>
<span data-ttu-id="5526f-158">식은 두 식이 같으면 true이 고, 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-158">The expression is true if the two expressions are equal and false if not.</span></span>

<span data-ttu-id="5526f-159">사용자 정의 형식의 값을 비교할 수 없습니다. 래핑 해제 된 값만 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-159">Values of user-defined types may not be compared, only their unwrapped values can be compared.</span></span> <span data-ttu-id="5526f-160">예를 들어 "래핑 해제" 연산자 `!` ( [의 Q# 형식 ](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)에 자세히 설명 되어 있음)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-160">For example, using the "unwrap" operator `!` (explained in detail at [Types in Q#](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),</span></span>

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

<span data-ttu-id="5526f-161">값에 대 한 같음 비교 `Qubit` 는 id 같음입니다. 즉, 두 식이 동일한의 비트를 식별 하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-161">Equality comparison for `Qubit` values is identity equality; that is, whether the two expressions identify the same qubit.</span></span>
<span data-ttu-id="5526f-162">이 비교로 두 개의 비트의 상태를 비교, 액세스, 측정 또는 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-162">The states of the two qubits are not compared, accessed, measured, or modified by this comparison.</span></span>

<span data-ttu-id="5526f-163">반올림 결과 때문에 값에 대 한 같음 비교가 `Double` 잘못 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-163">Equality comparison for `Double` values may be misleading due to rounding effects.</span></span>
<span data-ttu-id="5526f-164">`49.0 * (1.0/49.0) != 1.0`)을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-164">For example, `49.0 * (1.0/49.0) != 1.0`.</span></span>

<span data-ttu-id="5526f-165">두 숫자 식이 지정 된 경우 이항 연산자 `>` , `<` , 및를 `>=` `<=` 사용 하 여 첫 번째 식이 두 번째 식 보다 크거나 같고 보다 작거나 같은 경우 true 인 새 부울 식을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-165">Given any two numeric expressions, the binary operators `>`, `<`, `>=`, and `<=` may be used to construct a new Boolean expression that is true if the first expression is respectively greater than, less than, greater than or equal to, or less than or equal to the second expression.</span></span>

<span data-ttu-id="5526f-166">두 `and` 식이 모두 true 이면 이항 연산자를 사용 하 여 두 식이 모두 true 인 경우 true 인 새 부울 식을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-166">Given any two Boolean expressions, use the `and` binary operator to construct a new Boolean expression that is true if both of the two expressions are true.</span></span> <span data-ttu-id="5526f-167">마찬가지로 연산자를 사용 하면 `or` 두 식 중 하나가 true 인 경우 true 인 식이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-167">Likewise, using the `or` operator creates an expression that is true if either of the two expressions is true.</span></span>

<span data-ttu-id="5526f-168">부울 식이 지정 된 `not` 경우 단항 연산자를 사용 하 여 구성 식이 false 인 경우 true 인 새 부울 식을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-168">Given any Boolean expression, the `not` unary operator may be used to construct a new Boolean expression that is true if the constituent expression is false.</span></span>

## <a name="string-expressions"></a><span data-ttu-id="5526f-169">문자열 식</span><span class="sxs-lookup"><span data-stu-id="5526f-169">String expressions</span></span>

<span data-ttu-id="5526f-170">Q#`fail`문 ( [제어 흐름](xref:microsoft.quantum.guide.controlflow#fail-statement)에 설명) 및 표준 함수에 문자열을 사용할 수 있습니다 [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) .</span><span class="sxs-lookup"><span data-stu-id="5526f-170">Q# allows strings to be used in the `fail` statement (explained in [Control Flow](xref:microsoft.quantum.guide.controlflow#fail-statement)) and in the [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) standard function.</span></span> <span data-ttu-id="5526f-171">후자의 특정 동작은 사용 된 시뮬레이터에 따라 다르며 일반적으로 프로그램 중 호출 될 때 호스트 콘솔에 메시지를 기록 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="5526f-171">The specific behavior of the latter depends on the simulator used but typically writes a message to the host console when called during a Q# program.</span></span>

<span data-ttu-id="5526f-172">의 문자열 Q# 은 리터럴 또는 보간된 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-172">Strings in Q# are either literals or interpolated strings.</span></span>

<span data-ttu-id="5526f-173">문자열 리터럴은 대부분의 언어에서 간단한 문자열 리터럴과 유사 합니다. 큰따옴표 안의 유니코드 문자 시퀀스 `" "` 입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-173">String literals are similar to simple string literals in most languages: a sequence of Unicode characters enclosed in double-quotes `" "`.</span></span>
<span data-ttu-id="5526f-174">문자열 내에서 백슬래시 문자를 사용 하 여 `\` 큰따옴표 문자 ()를 이스케이프 하거나, 줄 바꿈 문자 () `\"` `\n` , 캐리지 리턴 ( `\r` ) 또는 탭 ()을 삽입 `\t` 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-174">Inside of a string, use the backslash character `\` to escape a double-quote character (`\"`), or to insert a new-line ( `\n` ), a carriage return (`\r`), or a tab (`\t`).</span></span>
<span data-ttu-id="5526f-175">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-175">For example:</span></span>

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a><span data-ttu-id="5526f-176">보간된 문자열</span><span class="sxs-lookup"><span data-stu-id="5526f-176">Interpolated strings</span></span>

<span data-ttu-id="5526f-177">Q#문자열 보간 구문은 c # 구문의 하위 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-177">The Q# syntax for string interpolations is a subset of the C# syntax.</span></span> <span data-ttu-id="5526f-178">다음은 관련 된 주요 사항입니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="5526f-178">Following are the key points as they pertain to Q#:</span></span>

* <span data-ttu-id="5526f-179">문자열 리터럴을 보간된 문자열로 식별하려면 `$` 기호를 사용하여 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-179">To identify a string literal as an interpolated string, prepend it with the `$` symbol.</span></span> <span data-ttu-id="5526f-180">`$` `"` 문자열 리터럴을 시작 하는와 사이에 공백이 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-180">There can be no white space between the `$` and the `"` that starts a string literal.</span></span>

* <span data-ttu-id="5526f-181">다음은 함수를 사용 하 여 [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) 다른 식과 함께 측정 결과를 콘솔에 쓰는 기본적인 예입니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="5526f-181">The following is a basic example using the [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) function to write the result of a measurement to the console, alongside other Q# expressions.</span></span>

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```

* <span data-ttu-id="5526f-182">모든 유효한 Q# 식은 보간된 문자열에 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-182">Any valid Q# expression may appear in an interpolated string.</span></span>

* <span data-ttu-id="5526f-183">보간된 문자열 내부의 식은 Q# c # 구문이 아니라 구문을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-183">Expressions inside of an interpolated string follow Q# syntax, not C# syntax.</span></span> <span data-ttu-id="5526f-184">가장 주목할 만한 차이점은 Q# 가 축 자 (여러 줄) 보간된 문자열을 지원 하지 않는다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-184">The most notable distinction is that Q# does not support verbatim (multi-line) interpolated strings.</span></span>

<span data-ttu-id="5526f-185">C # 구문에 대 한 자세한 내용은 [*보간된 문자열*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5526f-185">For more details about the C# syntax, see [*Interpolated Strings*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span></span>

## <a name="range-expressions"></a><span data-ttu-id="5526f-186">범위 식</span><span class="sxs-lookup"><span data-stu-id="5526f-186">Range Expressions</span></span>

<span data-ttu-id="5526f-187">3 개의 식, 및가 지정 된 경우이 `Int` `start` 식은를 `step` `stop` `start .. step .. stop` `start` `start+step` `start+step+step` 전달할 때까지 첫 번째 요소가이 고, 두 번째 요소가이 고, 세 번째 요소가 인 범위 식입니다 `stop` .</span><span class="sxs-lookup"><span data-stu-id="5526f-187">Given any three `Int` expressions `start`, `step`, and `stop`, the expression `start .. step .. stop` is a range expression whose first element is `start`, second element is `start+step`, third element is `start+step+step`, and so on, until you pass `stop`.</span></span>
<span data-ttu-id="5526f-188">예를 들어 `step` 가 양수이 고 인 경우 범위는 비어 있을 수 있습니다 `stop < start` .</span><span class="sxs-lookup"><span data-stu-id="5526f-188">A range may be empty if, for example, `step` is positive and `stop < start`.</span></span>

<span data-ttu-id="5526f-189">범위는 양쪽 끝에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-189">The range is inclusive at both ends.</span></span> <span data-ttu-id="5526f-190">즉, `start` 와 `stop` 의 차이가의 정수 배수가 면 `step` 범위의 마지막 요소는가 됩니다 `stop` .</span><span class="sxs-lookup"><span data-stu-id="5526f-190">That is, if the difference between `start` and `stop` is an integer multiple of `step`, the last element of the range will be `stop`.</span></span>

<span data-ttu-id="5526f-191">두 식 및가 지정 된 `Int` `start` `stop` 경우 식은와 `start .. stop` 같은 범위 식입니다 `start .. 1 .. stop` .</span><span class="sxs-lookup"><span data-stu-id="5526f-191">Given any two `Int` expressions `start` and `stop`, the expression `start .. stop` is a range expression that is equal to `start .. 1 .. stop`.</span></span>
<span data-ttu-id="5526f-192">`step`가 보다 작은 경우에도 암시는 + 1입니다 .이 `stop` `start` 경우 범위는 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-192">Note that the implied `step` is +1 even if `stop` is less than `start`; in such a case, the range is empty.</span></span>

<span data-ttu-id="5526f-193">몇 가지 예제 범위는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-193">Some example ranges are:</span></span>

- <span data-ttu-id="5526f-194">`1..3` 은 1, 2, 3의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-194">`1..3` is the range 1, 2, 3.</span></span>
- <span data-ttu-id="5526f-195">`2..2..5` 는 범위 2, 4입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-195">`2..2..5` is the range 2, 4.</span></span>
- <span data-ttu-id="5526f-196">`2..2..6` 는 2, 4, 6 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-196">`2..2..6` is the range 2, 4, 6.</span></span>
- <span data-ttu-id="5526f-197">`6..-2..2` 는 6, 4, 2 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-197">`6..-2..2` is the range 6, 4, 2.</span></span>
- <span data-ttu-id="5526f-198">`2..1` 는 빈 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-198">`2..1` is the empty range.</span></span>
- <span data-ttu-id="5526f-199">`2..6..7` 는 범위 2입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-199">`2..6..7` is the range 2.</span></span>
- <span data-ttu-id="5526f-200">`2..2..1` 는 빈 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-200">`2..2..1` is the empty range.</span></span>
- <span data-ttu-id="5526f-201">`1..-1..2` 는 빈 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-201">`1..-1..2` is the empty range.</span></span>

## <a name="qubit-expressions"></a><span data-ttu-id="5526f-202">Bit 식</span><span class="sxs-lookup"><span data-stu-id="5526f-202">Qubit Expressions</span></span>

<span data-ttu-id="5526f-203">유일한 `Qubit` 식은 `Qubit` 배열의 배열 요소 또는 값에 바인딩되는 기호입니다 `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="5526f-203">The only `Qubit` expressions are symbols that are bound to `Qubit` values or array elements of `Qubit` arrays.</span></span>
<span data-ttu-id="5526f-204">`Qubit`리터럴이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-204">There are no `Qubit` literals.</span></span>

## <a name="pauli-expressions"></a><span data-ttu-id="5526f-205">Pauli 식</span><span class="sxs-lookup"><span data-stu-id="5526f-205">Pauli Expressions</span></span>

<span data-ttu-id="5526f-206">,, 및의 네 가지 `Pauli` 값은 `PauliI` `PauliX` `PauliY` `PauliZ` 모두 유효한 `Pauli` 식입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-206">The four `Pauli` values, `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, are all valid `Pauli` expressions.</span></span>

<span data-ttu-id="5526f-207">그 외에도 유일한 `Pauli` 식은 `Pauli` 배열의 배열 요소 또는 값에 바인딩되는 기호입니다 `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="5526f-207">Other than that, the only `Pauli` expressions are symbols that are bound to `Pauli` values or array elements of `Pauli` arrays.</span></span>

## <a name="result-expressions"></a><span data-ttu-id="5526f-208">결과 식</span><span class="sxs-lookup"><span data-stu-id="5526f-208">Result Expressions</span></span>

<span data-ttu-id="5526f-209">두 `Result` 값 및는 `One` `Zero` 유효한 `Result` 식입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-209">The two `Result` values, `One` and `Zero`, are valid `Result` expressions.</span></span>

<span data-ttu-id="5526f-210">그 외에도 유일한 `Result` 식은 `Result` 배열의 배열 요소 또는 값에 바인딩되는 기호입니다 `Result` .</span><span class="sxs-lookup"><span data-stu-id="5526f-210">Other than that, the only `Result` expressions are symbols that are bound to `Result` values or array elements of `Result` arrays.</span></span>
<span data-ttu-id="5526f-211">특히는 `One` 정수와 동일 하지 않으며 `1` 두 요소 사이에 직접 변환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-211">In particular, note that `One` is not the same as the integer `1`, and there is no direct conversion between them.</span></span>
<span data-ttu-id="5526f-212">및의 경우에도 마찬가지입니다 `Zero` `0` .</span><span class="sxs-lookup"><span data-stu-id="5526f-212">The same is true for `Zero` and `0`.</span></span>

## <a name="tuple-expressions"></a><span data-ttu-id="5526f-213">튜플 식</span><span class="sxs-lookup"><span data-stu-id="5526f-213">Tuple Expressions</span></span>

<span data-ttu-id="5526f-214">튜플 리터럴은 괄호로 묶은 적절 한 형식의 요소 식의 시퀀스입니다 (쉼표로 구분).</span><span class="sxs-lookup"><span data-stu-id="5526f-214">A tuple literal is a sequence of element expressions of the appropriate type, separated by commas, enclosed in parentheses.</span></span>
<span data-ttu-id="5526f-215">예를 들어 `(1, One)` 은 `(Int, Result)` 식입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-215">For example, `(1, One)` is an `(Int, Result)` expression.</span></span>

<span data-ttu-id="5526f-216">리터럴 이외의 튜플 식은 튜플 값에 바인딩된 기호, 튜플 배열의 배열 요소 및 튜플을 반환 하는 호출 가능 호출입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-216">Other than literals, the only tuple expressions are symbols that are bound to tuple values, array elements of tuple arrays, and callable invocations that return tuples.</span></span>

## <a name="user-defined-type-expressions"></a><span data-ttu-id="5526f-217">User-Defined 형식 식</span><span class="sxs-lookup"><span data-stu-id="5526f-217">User-Defined Type Expressions</span></span>

<span data-ttu-id="5526f-218">사용자 정의 형식의 리터럴은 형식 이름과 해당 형식의 기본 튜플 형식의 튜플 리터럴로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-218">A literal of a user-defined type consists of the type name followed by a tuple literal of the type’s base tuple type.</span></span>
<span data-ttu-id="5526f-219">예를 들어 `IntPair` 가을 기반으로 하는 사용자 정의 형식인 경우는 `(Int, Int)` `IntPair(2, 3)` 해당 형식의 유효한 리터럴입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-219">For example, if `IntPair` is a user-defined type based on `(Int, Int)`, then `IntPair(2, 3)` is a valid literal of that type.</span></span>

<span data-ttu-id="5526f-220">리터럴 외에 사용자 정의 형식의 유일한 식은 해당 형식의 값에 바인딩된 기호, 해당 형식의 배열 요소, 해당 형식을 반환 하는 호출 가능 호출입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-220">Other than literals, the only expressions of a user-defined type are symbols that are bound to values of that type, array elements of arrays of that type, and callable invocations that return that type.</span></span>

## <a name="unwrap-expressions"></a><span data-ttu-id="5526f-221">래핑 해제 식</span><span class="sxs-lookup"><span data-stu-id="5526f-221">Unwrap Expressions</span></span>

<span data-ttu-id="5526f-222">에서 Q# 래핑 해제 연산자는 후행 느낌표 `!` 입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-222">In Q#, the unwrap operator is a trailing exclamation mark `!`.</span></span>
<span data-ttu-id="5526f-223">예를 들어 `IntPair` 이 기본 형식의 사용자 정의 형식이 `(Int, Int)` 고 `s` 값이 인 변수인 경우는 `IntPair(2, 3)` `s!` `(2, 3)` 입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-223">For example, if `IntPair` is a user-defined type with the underlying type `(Int, Int)` and `s` is a variable with value `IntPair(2, 3)`, then `s!` is `(2, 3)`.</span></span>

<span data-ttu-id="5526f-224">다른 사용자 정의 형식과 관련 하 여 정의 된 사용자 정의 형식의 경우 래핑 해제 연산자를 반복할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-224">For user-defined types defined in terms of other user-defined types, you can repeat the unwrap operator.</span></span> <span data-ttu-id="5526f-225">예를 들어는 `s!!` 이중 래핑 해제 된 값을 `s` 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-225">For example, `s!!` indicates the doubly-unwrapped value of `s`.</span></span>
<span data-ttu-id="5526f-226">따라서 `WrappedPair` 가 기본 형식의 사용자 정의 형식이 `IntPair` 고 `t` 가 값이 포함 된 변수인 경우는 `WrappedPair(IntPair(1,2))` `t!!` `(1,2)` 입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-226">Thus, if `WrappedPair` is a user-defined type with underlying type `IntPair`, and `t` is a variable with value `WrappedPair(IntPair(1,2))`, then `t!!` is `(1,2)`.</span></span>

<span data-ttu-id="5526f-227">`!`연산자는 `[]` 배열 인덱싱 및 조각화를 위해 이외의 다른 모든 연산자 보다 우선 순위가 높습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-227">The `!` operator has higher precedence than all other operators other than `[]` for array indexing and slicing.</span></span>
<span data-ttu-id="5526f-228">`!` 및 `[]` bind 메서드에 액세스할. 즉, `a[i]![3]` `((a[i])!)[3]` `i` 의 번째 요소를 가져와 래핑 해제 한 `a` 다음 래핑 해제 된 값 (배열 이어야 함)의 세 번째 요소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-228">`!` and `[]` bind positionally; that is, `a[i]![3]` is read as `((a[i])!)[3]`: take the `i`th element of `a`, unwrap it, and then get the 3rd element of the unwrapped value (which must be an array).</span></span>

<span data-ttu-id="5526f-229">연산자의 우선 순위에는 `!` 명확 하지 않을 수 있는 영향이 하나 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-229">The precedence of the `!` operator has one impact that might not be obvious.</span></span>
<span data-ttu-id="5526f-230">함수 또는 작업에서 래핑 해제 되는 값을 반환 하는 경우 인수 튜플이 래핑 되지 않고 호출에 바인딩되도록 함수 또는 작업 호출을 괄호로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-230">If a function or operation returns a value that then gets unwrapped, the function or operation call must be enclosed in parentheses so that the argument tuple binds to the call rather than to the unwrap.</span></span>
<span data-ttu-id="5526f-231">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-231">For example:</span></span>

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a><span data-ttu-id="5526f-232">배열 식</span><span class="sxs-lookup"><span data-stu-id="5526f-232">Array Expressions</span></span>

<span data-ttu-id="5526f-233">배열 리터럴은 쉼표로 구분 된 하나 이상의 요소 식의 시퀀스로 서 대괄호로 묶여 `[]` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-233">An array literal is a sequence of one or more element expressions, separated by commas, enclosed in square brackets `[]`.</span></span>
<span data-ttu-id="5526f-234">모든 요소는 동일한 형식과 호환 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-234">All elements must be compatible with the same type.</span></span>

<span data-ttu-id="5526f-235">동일한 형식의 두 배열이 지정 된 경우 이항 연산자를 사용 `+` 하 여 두 배열의 연결 인 새 배열을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-235">Given two arrays of the same type, use the binary `+` operator to form a new array that is the concatenation of the two arrays.</span></span>
<span data-ttu-id="5526f-236">예: `[1,2,3] + [4,5,6]` = `[1,2,3,4,5,6]`.</span><span class="sxs-lookup"><span data-stu-id="5526f-236">For example, `[1,2,3] + [4,5,6]` = `[1,2,3,4,5,6]`.</span></span>

### <a name="array-creation"></a><span data-ttu-id="5526f-237">배열 만들기</span><span class="sxs-lookup"><span data-stu-id="5526f-237">Array Creation</span></span>

<span data-ttu-id="5526f-238">형식 및 식이 지정 된 `Int` 경우 연산자를 사용 `new` 하 여 지정 된 크기의 새 배열을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-238">Given a type and an `Int` expression, use the `new` operator to allocate a new array of the given size.</span></span>
<span data-ttu-id="5526f-239">예를 들어는 `new Int[i + 1]` 요소로 새 `Int` 배열을 할당 `i + 1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-239">For example, `new Int[i + 1]` allocates a new `Int` array with `i + 1` elements.</span></span>

<span data-ttu-id="5526f-240">와 같은 빈 배열 리터럴은 `[]` 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-240">Empty array literals, such as `[]`, are not allowed.</span></span>
<span data-ttu-id="5526f-241">대신를 사용 하 여 길이가 0 인 배열을 만들 수 있습니다 `new T[0]` . 여기서 `T` 은 적절 한 형식에 대 한 자리 표시자입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-241">Instead, you can create an array of length zero by using `new T[0]`, where `T` is a placeholder for a suitable type.</span></span>

<span data-ttu-id="5526f-242">새 배열의 요소는 형식 종속 기본값으로 초기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-242">The elements of a new array initialize to a type-dependent default value.</span></span>
<span data-ttu-id="5526f-243">대부분의 경우이 값은 0의 변형입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-243">In most cases, this is some variation of zero.</span></span>

<span data-ttu-id="5526f-244">엔터티를 참조 하는 callables 및 callables의 경우 적절 한 기본값이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-244">For qubits and callables, which are references to entities, there is no reasonable default value.</span></span>
<span data-ttu-id="5526f-245">따라서 이러한 형식의 경우 기본값은 c #, Java 등의 언어에서 null 참조와 비슷하게 런타임 오류를 발생 시 키 지 않고 사용할 수 없는 잘못 된 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-245">Thus, for these types, the default is an invalid reference that you cannot use without causing a runtime error, similar to a null reference in languages such as C# or Java.</span></span>
<span data-ttu-id="5526f-246">요소를 안전 하 게 사용 하려면 기본값이 아닌 값으로 valbits 또는 callables을 포함 하는 배열을 초기화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-246">Arrays containing qubits or callables must be initialized with non-default values before you can use their elements safely.</span></span> <span data-ttu-id="5526f-247">적절 한 초기화 루틴은를 참조 하십시오 <xref:Microsoft.Quantum.Arrays> .</span><span class="sxs-lookup"><span data-stu-id="5526f-247">For suitable initialization routines, see <xref:Microsoft.Quantum.Arrays>.</span></span>

<span data-ttu-id="5526f-248">각 형식에 대 한 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-248">The default values for each type are:</span></span>

<span data-ttu-id="5526f-249">Type</span><span class="sxs-lookup"><span data-stu-id="5526f-249">Type</span></span> | <span data-ttu-id="5526f-250">기본값</span><span class="sxs-lookup"><span data-stu-id="5526f-250">Default</span></span>
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | <span data-ttu-id="5526f-251">_invalid qubit_</span><span class="sxs-lookup"><span data-stu-id="5526f-251">_invalid qubit_</span></span>
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | <span data-ttu-id="5526f-252">빈 범위 `1..1..0`</span><span class="sxs-lookup"><span data-stu-id="5526f-252">The empty range, `1..1..0`</span></span>
 `Callable` | <span data-ttu-id="5526f-253">_invalid callable_</span><span class="sxs-lookup"><span data-stu-id="5526f-253">_invalid callable_</span></span>
 `Array['T]` | `'T[0]`

<span data-ttu-id="5526f-254">튜플 형식은 요소를 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-254">Tuple types initialize element-by-element.</span></span>


### <a name="array-elements"></a><span data-ttu-id="5526f-255">배열 요소</span><span class="sxs-lookup"><span data-stu-id="5526f-255">Array Elements</span></span>

<span data-ttu-id="5526f-256">배열 식과 식이 지정 된 `Int` 경우 배열 요소 연산자를 사용 하 여 새 식을 형성 `[]` 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-256">Given an array expression and an `Int` expression, form a new expression using the array element operator `[]`.</span></span>
<span data-ttu-id="5526f-257">새 식은 배열의 요소 형식과 동일한 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-257">The new expression is the same type as the element type of the array.</span></span>
<span data-ttu-id="5526f-258">예를 들어 `a` 가 형식의 배열에 바인딩된 경우 `Double` `a[4]` 은 `Double` 식입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-258">For example, if `a` is bound to an array of type `Double`, then `a[4]` is a `Double` expression.</span></span>

<span data-ttu-id="5526f-259">배열 식이 단순 식별자가 아닌 경우 요소를 선택 하려면 괄호로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-259">If the array expression is not a simple identifier, you must enclose it in parentheses to select an element.</span></span>
<span data-ttu-id="5526f-260">예를 들어 `a` 및 `b` 가 모두 형식의 배열인 경우 `Int` 연결의 요소는 다음과 같이 표현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-260">For example, if `a` and `b` are both arrays of type `Int`, an element from the concatenation is expressed as:</span></span>

```qsharp
(a + b)[13]
```

<span data-ttu-id="5526f-261">의 모든 배열은 Q# 0부터 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-261">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="5526f-262">즉, 배열의 첫 번째 요소는 `a` 항상 `a[0]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-262">That is, the first element of an array `a` is always `a[0]`.</span></span>


### <a name="array-slices"></a><span data-ttu-id="5526f-263">배열 조각</span><span class="sxs-lookup"><span data-stu-id="5526f-263">Array Slices</span></span>

<span data-ttu-id="5526f-264">배열 식과 식이 지정 된 `Range` 경우 배열 조각 연산자를 사용 하 여 새 식을 형성 `[ ]` 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-264">Given an array expression and a `Range` expression, form a new expression using the array slice operator `[ ]`.</span></span>
<span data-ttu-id="5526f-265">새 식은 배열과 동일한 형식이 고,의 요소로 인덱싱된 배열 항목 `Range` 을에 정의 된 순서 대로 포함 합니다 `Range` .</span><span class="sxs-lookup"><span data-stu-id="5526f-265">The new expression is the same type as the array and contains the array items indexed by the elements of the `Range`, in the order defined by the `Range`.</span></span>
<span data-ttu-id="5526f-266">예를 들어 `a` 가 형식의 배열에 바인딩된 경우는 `Double` `a[3..-1..0]` `Double[]` 의 처음 4 개 요소를 포함 하는 식이 며 `a` 에 표시 `a` 되는 순서는 반대입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-266">For example, if `a` is bound to an array of type `Double`, then `a[3..-1..0]` is a `Double[]` expression that contains the first four elements of `a` but in the reverse order as they appear in `a`.</span></span>

<span data-ttu-id="5526f-267">`Range`이 비어 있으면 결과 배열 조각의 길이가 0이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-267">If the `Range` is empty, then the resulting array slice is zero length.</span></span>

<span data-ttu-id="5526f-268">참조 하는 배열 요소와 마찬가지로 배열 식이 단순 식별자가 아닌 경우이를 괄호로 묶어 조각화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-268">Just as with referencing array elements, if the array expression is not a simple identifier, you must enclose it in parentheses to slice it.</span></span>
<span data-ttu-id="5526f-269">예를 들어 `a` 및 `b` 가 모두 형식의 배열인 경우 `Int` 연결의 조각이 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-269">For example, if `a` and `b` are both arrays of type `Int`, a slice from the concatenation is expressed as:</span></span>

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a><span data-ttu-id="5526f-270">유추 된 시작/끝 값</span><span class="sxs-lookup"><span data-stu-id="5526f-270">Inferred start/end values</span></span>

<span data-ttu-id="5526f-271">[0.8 릴리스부터](xref:microsoft.quantum.relnotes)는 범위 조각화를 위한 상황별 식을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-271">Starting with our [0.8 release](xref:microsoft.quantum.relnotes), we support contextual expressions for range slicing.</span></span> <span data-ttu-id="5526f-272">특히 범위 조각화 식의 컨텍스트에서 범위 시작 값과 끝 값을 생략할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-272">In particular, you may omit range start and end values in the context of a range slicing expression.</span></span> <span data-ttu-id="5526f-273">이 경우 컴파일러는 다음 규칙을 적용 하 여 범위에 대 한 의도 된 구분 기호를 유추 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-273">In that case, the compiler applies the following rules to infer the intended delimiters for the range:</span></span>

* <span data-ttu-id="5526f-274">Range *start* 값을 생략 하면 유추 된 시작 값이</span><span class="sxs-lookup"><span data-stu-id="5526f-274">If the range *start* value is omitted, then the inferred start value</span></span>
  * <span data-ttu-id="5526f-275">지정 된 단계가 없거나 지정 된 단계가 양수인 경우는 0입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-275">is zero if no step is specified or the specified step is positive.</span></span>  
  * <span data-ttu-id="5526f-276">지정 된 단계가 음수인 경우 분리 된 배열의 길이에서 1을 뺀 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-276">is the length of the sliced array minus one if the specified step is negative.</span></span>

* <span data-ttu-id="5526f-277">범위 *끝* 값이 생략 된 경우에는 유추 된 끝 값이</span><span class="sxs-lookup"><span data-stu-id="5526f-277">If the range *end* value is omitted, then the inferred end value</span></span>
  * <span data-ttu-id="5526f-278">지정 된 단계가 없거나 지정 된 단계가 양수인 경우 분리 된 배열의 길이가 1을 뺀 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-278">is the length of the sliced array minus one if no step is specified or the specified step is positive.</span></span>
  * <span data-ttu-id="5526f-279">지정 된 단계가 음수 이면 0이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-279">is zero if the specified step is negative.</span></span>

<span data-ttu-id="5526f-280">예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-280">Some examples are:</span></span>

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

### <a name="copy-and-update-expressions"></a><span data-ttu-id="5526f-281">복사 및 업데이트 식</span><span class="sxs-lookup"><span data-stu-id="5526f-281">Copy-and-Update Expressions</span></span>

<span data-ttu-id="5526f-282">모든 형식이 값 형식이 기 때문에 (예를 Q# 들어, 모든 형식이 특별 한 역할을 수행 하는 경우) 값이 기호에 바인딩되거나 기호가 바인딩 되었을 때 공식적으로 "copy"가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-282">Since all Q# types are value types (with the qubits taking a somewhat special role), formally a "copy" is created when a value is bound to a symbol or when a symbol is rebound.</span></span> <span data-ttu-id="5526f-283">즉,의 동작은 Q# 할당 연산자를 사용 하 여 복사본을 만든 경우와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-283">That is to say, the behavior of Q# is the same as if a copy were created using an assignment operator.</span></span> 

<span data-ttu-id="5526f-284">물론 실제로는 관련 된 부분만 필요에 따라 다시 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-284">Of course, in practice, only the relevant pieces are recreated as needed.</span></span> <span data-ttu-id="5526f-285">이는 배열 항목을 업데이트할 수 없기 때문에 배열을 복사 하는 방법에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-285">This affects how you copy arrays because it is not possible to update array items.</span></span> <span data-ttu-id="5526f-286">기존 배열을 수정 하려면 *복사 및 업데이트* 메커니즘을 활용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-286">To modify an existing array requires leveraging a *copy-and-update* mechanism.</span></span>

<span data-ttu-id="5526f-287">및 연산자를 사용 하는 *복사 및 업데이트* 식을 통해 기존 배열에서 새 배열을 만들 수 있습니다 `w/` `<-` .</span><span class="sxs-lookup"><span data-stu-id="5526f-287">You can create a new array from an existing array via *copy-and-update* expressions, which use the operators `w/` and `<-`.</span></span>
<span data-ttu-id="5526f-288">복사 및 업데이트 식은 `expression1 w/ expression2 <- expression3` 다음 형식의 식입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-288">A copy-and-update expression is an expression of the form `expression1 w/ expression2 <- expression3`, where</span></span>

* <span data-ttu-id="5526f-289">`expression1``T[]`일부 형식의 경우 형식 이어야 합니다 `T` .</span><span class="sxs-lookup"><span data-stu-id="5526f-289">`expression1` must be type `T[]` for some type `T`.</span></span>
* <span data-ttu-id="5526f-290">`expression2` 에서 수정 하기 위해 지정 된 배열의 인덱스를 정의 `expression1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-290">`expression2` defines which indices in the array specified in `expression1` to modify.</span></span> <span data-ttu-id="5526f-291">`expression2` 형식 또는 형식 중 하나 여야 합니다 `Int` `Range` .</span><span class="sxs-lookup"><span data-stu-id="5526f-291">`expression2` must be either type `Int` or type `Range`.</span></span>
* <span data-ttu-id="5526f-292">`expression3` 에 `expression1` 지정 된 인덱스에 따라의 요소를 업데이트 하는 데 사용 되는 값입니다 `expression2` .</span><span class="sxs-lookup"><span data-stu-id="5526f-292">`expression3` is the value(s) used to update elements in `expression1`, based on the indices specified in `expression2`.</span></span> <span data-ttu-id="5526f-293">`expression2`가 형식이 면 `Int` 은 `expression3` 형식 이어야 합니다 `T` .</span><span class="sxs-lookup"><span data-stu-id="5526f-293">If `expression2` is type `Int`, `expression3` must be type `T`.</span></span> <span data-ttu-id="5526f-294">`expression2`가 형식이 면 `Range` 은 `expression3` 형식 이어야 합니다 `T[]` .</span><span class="sxs-lookup"><span data-stu-id="5526f-294">If `expression2` is type `Range`, `expression3` must be type `T[]`.</span></span>

<span data-ttu-id="5526f-295">예를 들어, 복사 및 업데이트 식은에서로 지정 된 요소를 제외 하 고 `arr w/ idx <- value` 모든 요소가의 해당 요소로 설정 된 새 배열을 생성 `arr` `idx` 합니다 .이 요소는의 값으로 설정 됩니다 `value` .</span><span class="sxs-lookup"><span data-stu-id="5526f-295">For example, the copy-and-update expression `arr w/ idx <- value` constructs a new array with all elements set to the corresponding elements in `arr`, except for the element(s) specified by `idx`, which is set to the value(s) in `value`.</span></span> 

<span data-ttu-id="5526f-296">지정 된에 `arr` 배열이 포함 된 `[0,1,2,3]` 경우</span><span class="sxs-lookup"><span data-stu-id="5526f-296">Given `arr` contains the array `[0,1,2,3]`, then</span></span> 

- <span data-ttu-id="5526f-297">`arr w/ 0 <- 10` 는 배열 `[10,1,2,3]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-297">`arr w/ 0 <- 10` is the array `[10,1,2,3]`.</span></span>
- <span data-ttu-id="5526f-298">`arr w/ 2 <- 10` 는 배열 `[0,1,10,3]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-298">`arr w/ 2 <- 10` is the array `[0,1,10,3]`.</span></span>
- <span data-ttu-id="5526f-299">`arr w/ 0..2..3 <- [10,12]` 는 배열 `[10,1,12,3]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-299">`arr w/ 0..2..3 <- [10,12]` is the array `[10,1,12,3]`.</span></span>

#### <a name="copy-and-update-expressions-for-named-items"></a><span data-ttu-id="5526f-300">명명 된 항목에 대 한 복사 및 업데이트 식</span><span class="sxs-lookup"><span data-stu-id="5526f-300">Copy-and-update expressions for named items</span></span>

<span data-ttu-id="5526f-301">사용자 정의 형식에 명명 된 항목에 대 한 유사한 식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-301">Similar expressions exist for named items in user-defined types.</span></span> 

<span data-ttu-id="5526f-302">예를 들어 다음 형식을 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-302">For example, consider the type</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="5526f-303">에 `c` 형식의 값이 포함 된 경우 `Complex(1., -1.)` `c w/ Re <- 0.` 는 `Complex` 로 계산 되는 형식의 식입니다 `Complex(0., -1.)` .</span><span class="sxs-lookup"><span data-stu-id="5526f-303">If `c` contains the value of type `Complex(1., -1.)`, then `c w/ Re <- 0.` is an expression of type `Complex` that evaluates to `Complex(0., -1.)`.</span></span>

### <a name="jagged-arrays"></a><span data-ttu-id="5526f-304">가변 배열</span><span class="sxs-lookup"><span data-stu-id="5526f-304">Jagged Arrays</span></span>

<span data-ttu-id="5526f-305">"배열의 배열"이 라고도 하는 가변 배열은 요소가 배열인 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-305">A jagged array, sometimes called an "array of arrays," is an array whose elements are arrays.</span></span>
<span data-ttu-id="5526f-306">가변 배열의 요소는 크기가 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-306">The elements of a jagged array can be of different sizes.</span></span>
<span data-ttu-id="5526f-307">다음 예에서는 곱하기 테이블을 나타내는 가변 배열을 선언 하 고 초기화 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-307">The following example shows how to declare and initialize a jagged array representing a multiplication table.</span></span>

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

### <a name="arrays-of-callables"></a><span data-ttu-id="5526f-308">Callables 배열</span><span class="sxs-lookup"><span data-stu-id="5526f-308">Arrays of callables</span></span> 

<span data-ttu-id="5526f-309">Callables 배열을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-309">You can also create an array of callables.</span></span>

* <span data-ttu-id="5526f-310">공통 요소 형식이 작업 또는 함수 형식이 면 모든 요소에 동일한 입력 및 출력 형식이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-310">If the common element type is an operation or function type, all of the elements must have the same input and output types.</span></span>
* <span data-ttu-id="5526f-311">배열의 요소 형식은 모든 요소에서 지원 되는 모든 [함수](xref:microsoft.quantum.guide.operationsfunctions) 을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-311">The element type of the array supports any [functors](xref:microsoft.quantum.guide.operationsfunctions) that are supported by all of the elements.</span></span>
<span data-ttu-id="5526f-312">예를 들어, `Op1` 및 all이 작업 이지만를 지원 하 고,를 지원 하며,를 지원 합니다 `Op2` `Op3` `Qubit[] => Unit` `Op1` `Adjoint` `Op2` `Controlled` `Op3` .</span><span class="sxs-lookup"><span data-stu-id="5526f-312">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[] => Unit` operations, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>
  * <span data-ttu-id="5526f-313">`[Op1, Op2]` 는 작업의 배열입니다 `(Qubit[] => Unit)` .</span><span class="sxs-lookup"><span data-stu-id="5526f-313">`[Op1, Op2]` is an array of `(Qubit[] => Unit)` operations.</span></span>
  * <span data-ttu-id="5526f-314">`[Op1, Op3]` 는 작업의 배열입니다 `(Qubit[] => Unit is Adj)` .</span><span class="sxs-lookup"><span data-stu-id="5526f-314">`[Op1, Op3]` is an array of `(Qubit[] => Unit is Adj)` operations.</span></span>
  * <span data-ttu-id="5526f-315">`[Op2, Op3]` 는 작업의 배열입니다 `(Qubit[] => Unit is Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="5526f-315">`[Op2, Op3]` is an array of `(Qubit[] => Unit is Ctl)` operations.</span></span>

<span data-ttu-id="5526f-316">그러나 작업과 `(Qubit[] => Unit is Adj)`  `(Qubit[] => Unit is Ctl)` 의 공통 기본 형식은 이지만 `(Qubit[] => Unit)` 이러한 작업의 *배열은* 공통 기본 형식을 공유 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-316">However, while the operations `(Qubit[] => Unit is Adj)` and  `(Qubit[] => Unit is Ctl)` have the common base type of `(Qubit[] => Unit)`, *arrays* of these operations do not share a common base type.</span></span>

<span data-ttu-id="5526f-317">예를 들어는 `[[Op1], [Op2]]` 호환 되지 않는 두 배열 형식 및의 배열을 만들려고 하기 때문에 현재 오류를 발생 `(Qubit[] => Unit is Adj)[]` 시킵니다 `(Qubit[] => Unit is Ctl)[]` .</span><span class="sxs-lookup"><span data-stu-id="5526f-317">For example, `[[Op1], [Op2]]` would currently raise an error because it attempts to create an array of the two incompatible array types `(Qubit[] => Unit is Adj)[]` and `(Qubit[] => Unit is Ctl)[]`.</span></span>

<span data-ttu-id="5526f-318">Callables에 대 한 자세한 내용은이 페이지의 [호출 가능 식](#callable-expressions) 또는 [의 Q# 작업 및 함수 ](xref:microsoft.quantum.guide.operationsfunctions)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5526f-318">For more information on callables, see [Callable expressions](#callable-expressions)  on this page or [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="5526f-319">조건 식</span><span class="sxs-lookup"><span data-stu-id="5526f-319">Conditional Expressions</span></span>

<span data-ttu-id="5526f-320">동일한 형식 및 부울 식의 두 식이 지정 된 경우 물음표, 및 세로 막대를 사용 하 여 조건식을 형성 `?` `|` 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-320">Given two expressions of the same type and a Boolean expression, form a conditional expression using the question mark, `?`, and the vertical bar `|`.</span></span> <span data-ttu-id="5526f-321">`a==b ? c | d`조건 식의 값은이 true 이면이 `c` 고, `a==b` `d` false 이면입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-321">Given `a==b ? c | d`, the value of the conditional expression is `c` if `a==b` is true and `d` if it is false.</span></span>

### <a name="conditional-expressions-with-callables"></a><span data-ttu-id="5526f-322">Callables 사용 조건 식</span><span class="sxs-lookup"><span data-stu-id="5526f-322">Conditional expressions with callables</span></span>

<span data-ttu-id="5526f-323">조건식은 동일한 입력 및 출력을 포함 하는 작업으로 계산 될 수 있지만 다른 함수을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-323">Conditional expressions may evaluate to operations that have the same inputs and outputs but support different functors.</span></span> <span data-ttu-id="5526f-324">이 경우 조건식의 형식은 두 식에서 지원 되는 모든 함수를 지 원하는 입력 및 출력을 사용 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-324">In this case, the type of the conditional expression is an operation with inputs and outputs that support any functors supported by both expressions.</span></span>
<span data-ttu-id="5526f-325">예를 들어, `Op1` `Op2` 및 `Op3` 모두가 이지만,를 `Qubit[]=>Unit` `Op1` 지원 하 `Adjoint` `Op2` `Controlled` 고 `Op3` 를 지원 하며를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-325">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[]=>Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="5526f-326">`flag ? Op1 | Op2` 은 `(Qubit[] => Unit)` 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-326">`flag ? Op1 | Op2` is a `(Qubit[] => Unit)` operation.</span></span>
- <span data-ttu-id="5526f-327">`flag ? Op1 | Op3` 은 `(Qubit[] => Unit is Adj)` 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-327">`flag ? Op1 | Op3` is a `(Qubit[] => Unit is Adj)` operation.</span></span>
- <span data-ttu-id="5526f-328">`flag ? Op2 | Op3` 은 `(Qubit[] => Unit is Ctl)` 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-328">`flag ? Op2 | Op3` is a `(Qubit[] => Unit is Ctl)` operation.</span></span>

<span data-ttu-id="5526f-329">두 가지 가능한 결과 식 중 하나에 함수 또는 작업 호출이 포함 된 경우 해당 호출은 호출 값인 경우에만 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-329">If either of the two possible result expressions include a function or operation call, that call only takes place if that result is the one that is the value of the call.</span></span> <span data-ttu-id="5526f-330">예를 들어의 경우 `a==b ? C(qs) | D(qs)` `a==b` 이 true 이면 `C` 작업이 호출 되 고 false 이면 작업만 `D` 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-330">For example, in the case `a==b ? C(qs) | D(qs)`, if `a==b` is true, then the `C` operation is invoked, and if it is false then only the `D` operation is invoked.</span></span> <span data-ttu-id="5526f-331">이 방법은 다른 언어의 *단락* 와 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-331">This approach is similar to *short-circuiting* in other languages.</span></span>

## <a name="callable-expressions"></a><span data-ttu-id="5526f-332">호출 가능 식</span><span class="sxs-lookup"><span data-stu-id="5526f-332">Callable Expressions</span></span>

<span data-ttu-id="5526f-333">호출 가능 리터럴은 컴파일 범위에서 정의 된 작업 또는 함수의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-333">A callable literal is the name of an operation or function defined in the compilation scope.</span></span> <span data-ttu-id="5526f-334">예를 들어 `X` 는 표준 라이브러리 작업을 참조 하는 작업 리터럴이 며 `X` `Message` 은 표준 라이브러리 함수를 참조 하는 함수 리터럴입니다 `Message` .</span><span class="sxs-lookup"><span data-stu-id="5526f-334">For example, `X` is an operation literal that refers to the standard library `X` operation, and `Message` is a function literal that refers to the standard library `Message` function.</span></span>

<span data-ttu-id="5526f-335">작업에서 함수를 지 원하는 경우 `Adjoint` `Adjoint op` 는 연산 식입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-335">If an operation supports the `Adjoint` functor, then `Adjoint op` is an operation expression.</span></span>
<span data-ttu-id="5526f-336">마찬가지로 작업에서 함수를 지 원하는 경우 `Controlled` `Controlled op` 는 연산 식입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-336">Similarly, if the operation supports the `Controlled` functor, then `Controlled op` is an operation expression.</span></span>
<span data-ttu-id="5526f-337">이러한 식의 형식에 대 한 자세한 내용은 [호출 작업 특수화](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="5526f-337">For more information about the types of these expressions, see [Calling operation specializations](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).</span></span>

<span data-ttu-id="5526f-338">함수 ( `Adjoint` 및 `Controlled` )는를 사용 하 여 래핑 해제 연산자와 배열 인덱싱을 제외 하 고 다른 모든 연산자 보다 더 가깝게 바인딩합니다 `!` `[ ]` .</span><span class="sxs-lookup"><span data-stu-id="5526f-338">Functors (`Adjoint` and `Controlled`) bind more closely than all other operators, except for the unwrap operator `!` and array indexing with `[ ]`.</span></span>
<span data-ttu-id="5526f-339">따라서 다음은 작업에서 사용 되는 함수를 지원 한다고 가정 하 고 모두 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-339">Thus, the following are all valid, assuming that the operations support the functors used:</span></span>

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a><span data-ttu-id="5526f-340">형식 매개 변수가 있는 호출 가능 식</span><span class="sxs-lookup"><span data-stu-id="5526f-340">Type-parameterized callable expressions</span></span>

<span data-ttu-id="5526f-341">예를 들어 호출 가능 리터럴을 값으로 사용 하 여 변수에 할당 하거나 다른 호출 가능 클래스에 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-341">You can use a callable literal as a value, for example, to assign it to a variable or pass it to another callable.</span></span> <span data-ttu-id="5526f-342">이 경우 호출 가능에 [형식 매개 변수가](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables)있는 경우 매개 변수를 호출 가능 값의 일부로 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-342">In this case, if the callable has [type parameters](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), you must provide the parameters as part of the callable value.</span></span>

<span data-ttu-id="5526f-343">호출 가능 값은 지정 되지 않은 형식 매개 변수를 가질 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-343">A callable value cannot have any unspecified type parameters.</span></span> <span data-ttu-id="5526f-344">예를 들어 `Fun` 가 시그니처를 사용 하는 함수인 경우입니다 `'T1->Unit` .</span><span class="sxs-lookup"><span data-stu-id="5526f-344">For example, if `Fun` is a function with the signature `'T1->Unit`:</span></span>

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomeOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a><span data-ttu-id="5526f-345">호출 가능 호출 식</span><span class="sxs-lookup"><span data-stu-id="5526f-345">Callable Invocation Expressions</span></span>

<span data-ttu-id="5526f-346">호출 가능 식 (작업 또는 함수) 및 호출 가능 시그니처의 입력 형식 튜플 식이 지정 된 경우 호출 가능 식에 튜플 식을 추가 하 여 *호출 식을* 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-346">Given a callable expression (operation or function) and a tuple expression of the input type of the callable's signature, you can form an *invocation expression* by appending the tuple expression to the callable expression.</span></span>
<span data-ttu-id="5526f-347">호출 식의 형식은 호출 가능 시그니처의 출력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-347">The type of the invocation expression is the output type of the callable's signature.</span></span>

<span data-ttu-id="5526f-348">예를 들어 `Op` 가 서명이 포함 된 작업 인 경우 `((Int, Qubit) => Double)` `Op(3, qubit1)` 는 형식의 식입니다 `Double` .</span><span class="sxs-lookup"><span data-stu-id="5526f-348">For example, if `Op` is an operation with the signature `((Int, Qubit) => Double)`, `Op(3, qubit1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="5526f-349">마찬가지로 `Sin` 가 서명이 포함 된 함수인 경우 `(Double -> Double)` `Sin(0.1)` 는 형식의 식입니다 `Double` .</span><span class="sxs-lookup"><span data-stu-id="5526f-349">Similarly, if `Sin` is a function with the signature `(Double -> Double)`, `Sin(0.1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="5526f-350">마지막으로 `Builder` 가 시그니처를 사용 하는 함수인 경우 `(Int -> (Int -> Int))` `Builder(3)` 는에서로의 함수입니다 `Int` `Int` .</span><span class="sxs-lookup"><span data-stu-id="5526f-350">Finally, if `Builder` is a function with the signature `(Int -> (Int -> Int))`, then `Builder(3)` is a function from `Int` to `Int`.</span></span>

<span data-ttu-id="5526f-351">호출 가능 값 식의 결과를 호출 하려면 호출 가능 식 주위에 괄호 쌍을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-351">Invoking the result of a callable-valued expression requires an extra pair of parentheses around the callable expression.</span></span>
<span data-ttu-id="5526f-352">따라서 이전 단락에서 호출 결과를 호출 하려면 `Builder` 올바른 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-352">Thus, to invoke the result of calling `Builder` from the previous paragraph, the correct syntax is:</span></span>

```qsharp
(Builder(3))(2)
```

<span data-ttu-id="5526f-353">[형식 매개 변수가 있는](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) 호출 가능 식을 호출 하는 경우 `< >` 호출 가능 식 뒤에 꺾쇠 괄호 내에서 실제 형식 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-353">When invoking a [type-parameterized](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) callable, you can specify the actual type parameters within angle brackets `< >` after the callable expression.</span></span>
<span data-ttu-id="5526f-354">컴파일러가 실제 형식을 유추 하므로 일반적으로이 작업은 필요 하지 않습니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="5526f-354">This action is usually unnecessary as the Q# compiler infers the actual types.</span></span>
<span data-ttu-id="5526f-355">그러나 형식 매개 변수가 있는 인수를 지정 하지 *않은 상태로 두면* [부분 응용 프로그램](xref:microsoft.quantum.guide.operationsfunctions#partial-application) 에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-355">However, it *is* required for [partial application](xref:microsoft.quantum.guide.operationsfunctions#partial-application) if a type-parameterized argument is left unspecified.</span></span>
<span data-ttu-id="5526f-356">또한 다른 함수를 사용 하는 작업을 호출할 수 있도록 지 원하는 경우에도 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-356">It is also useful when passing operations with different functor supports to a callable.</span></span>

<span data-ttu-id="5526f-357">예를 들어,에 시그니처가 있고,에 시그니처가 있고,가 첫 번째 인수로를 사용 하 여를 호출 하 고,를 `Func` `('T1, 'T2, 'T1) -> 'T2` 세 번째 `Op1` `Op2` `(Qubit[] => Unit is Adj)` `Op3` `(Qubit[] => Unit)` 인수로 호출 하 `Func` `Op1` `Op2` `Op3` 는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-357">For example, if `Func` has signature `('T1, 'T2, 'T1) -> 'T2`, `Op1` and `Op2` have signature `(Qubit[] => Unit is Adj)`, and `Op3` has signature `(Qubit[] => Unit)`, to invoke `Func` with `Op1` as the first argument, `Op2` as the second, and `Op3` as the third:</span></span>

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

<span data-ttu-id="5526f-358">및에 다른 형식이 있으므로 형식 사양이 필요 합니다 `Op3` `Op1` . 따라서 컴파일러는 사양을 사용 하지 않고이를 모호 하 게 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-358">The type specification is required because `Op3` and `Op1` have different types, so the compiler will treat this as ambiguous without the specification.</span></span>


## <a name="operator-precedence"></a><span data-ttu-id="5526f-359">연산자 우선 순위</span><span class="sxs-lookup"><span data-stu-id="5526f-359">Operator Precedence</span></span>

* <span data-ttu-id="5526f-360">모든 이항 연산자는를 제외 하 고 오른쪽 결합성이 `^` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-360">All binary operators are right-associative, except for `^`.</span></span>

* <span data-ttu-id="5526f-361">대괄호, `[ ]` 배열 조각화 및 인덱싱의 경우 모든 연산자 앞에 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-361">Brackets, `[ ]`, for array slicing and indexing, bind before any operator.</span></span>

* <span data-ttu-id="5526f-362">함수 `Adjoint` 및는 `Controlled` 배열 인덱싱 후 다른 모든 연산자 앞에 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-362">The functors `Adjoint` and `Controlled` bind after array indexing but before all other operators.</span></span>

* <span data-ttu-id="5526f-363">연산 및 함수 호출에 대 한 괄호는 모든 연산자 앞에, 배열 인덱싱 및 함수 후에도 바인딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="5526f-363">Parentheses for operation and function invocation also bind before any operator but after array indexing and functors.</span></span>

<span data-ttu-id="5526f-364">Q# 우선 순위 순으로 최고에서 최저 순으로 연산자.</span><span class="sxs-lookup"><span data-stu-id="5526f-364">Q# operators in order of precedence, from highest to lowest:</span></span>

<span data-ttu-id="5526f-365">연산자</span><span class="sxs-lookup"><span data-stu-id="5526f-365">Operator</span></span> | <span data-ttu-id="5526f-366">숫자</span><span class="sxs-lookup"><span data-stu-id="5526f-366">Arity</span></span> | <span data-ttu-id="5526f-367">Description</span><span class="sxs-lookup"><span data-stu-id="5526f-367">Description</span></span> | <span data-ttu-id="5526f-368">피연산자 형식</span><span class="sxs-lookup"><span data-stu-id="5526f-368">Operand Types</span></span>
---------|----------|---------|---------------
 <span data-ttu-id="5526f-369">붙이지 `!`</span><span class="sxs-lookup"><span data-stu-id="5526f-369">trailing `!`</span></span> | <span data-ttu-id="5526f-370">단항</span><span class="sxs-lookup"><span data-stu-id="5526f-370">Unary</span></span> | <span data-ttu-id="5526f-371">래핑 취소</span><span class="sxs-lookup"><span data-stu-id="5526f-371">Unwrap</span></span> | <span data-ttu-id="5526f-372">사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="5526f-372">Any user-defined type</span></span>
 <span data-ttu-id="5526f-373">`-`, `~~~`, `not`</span><span class="sxs-lookup"><span data-stu-id="5526f-373">`-`, `~~~`, `not`</span></span> | <span data-ttu-id="5526f-374">단항</span><span class="sxs-lookup"><span data-stu-id="5526f-374">Unary</span></span> | <span data-ttu-id="5526f-375">숫자 음수, 비트 보수, 논리 부정</span><span class="sxs-lookup"><span data-stu-id="5526f-375">Numeric negative, bitwise complement, logical negation</span></span> | <span data-ttu-id="5526f-376">`Int`,의 경우,,의 경우,의 경우 `BigInt` `Double` `-` `Int` `BigInt` `~~~` `Bool``not`</span><span class="sxs-lookup"><span data-stu-id="5526f-376">`Int`, `BigInt` or `Double` for `-`, `Int` or `BigInt` for `~~~`, `Bool` for `not`</span></span>
 `^` | <span data-ttu-id="5526f-377">이진</span><span class="sxs-lookup"><span data-stu-id="5526f-377">Binary</span></span> | <span data-ttu-id="5526f-378">정수 거듭제곱</span><span class="sxs-lookup"><span data-stu-id="5526f-378">Integer power</span></span> | <span data-ttu-id="5526f-379">`Int`또는 기준의 경우 지 수의 경우입니다. `BigInt` `Int`</span><span class="sxs-lookup"><span data-stu-id="5526f-379">`Int` or `BigInt` for the base, `Int` for the exponent</span></span>
 <span data-ttu-id="5526f-380">`/`, `*`, `%`</span><span class="sxs-lookup"><span data-stu-id="5526f-380">`/`, `*`, `%`</span></span> | <span data-ttu-id="5526f-381">이진</span><span class="sxs-lookup"><span data-stu-id="5526f-381">Binary</span></span> | <span data-ttu-id="5526f-382">나누기, 곱하기, 정수 모듈러스</span><span class="sxs-lookup"><span data-stu-id="5526f-382">Division, multiplication, integer modulus</span></span> | <span data-ttu-id="5526f-383">`Int`,,, 또는 `BigInt` `Double` `/` `*` `Int` `BigInt` 의 경우 `%`</span><span class="sxs-lookup"><span data-stu-id="5526f-383">`Int`, `BigInt` or `Double` for `/` and `*`, `Int` or `BigInt` for `%`</span></span>
 <span data-ttu-id="5526f-384">`+`, `-`</span><span class="sxs-lookup"><span data-stu-id="5526f-384">`+`, `-`</span></span> | <span data-ttu-id="5526f-385">이진</span><span class="sxs-lookup"><span data-stu-id="5526f-385">Binary</span></span> | <span data-ttu-id="5526f-386">더하기 또는 문자열 및 배열 연결, 빼기</span><span class="sxs-lookup"><span data-stu-id="5526f-386">Addition or string and array concatenation, subtraction</span></span> | <span data-ttu-id="5526f-387">`Int`,, `BigInt` 또는 `Double` `String` 에 대 한 배열 형식입니다. `+`</span><span class="sxs-lookup"><span data-stu-id="5526f-387">`Int`, `BigInt` or `Double`, additionally `String` or any array type for `+`</span></span>
 <span data-ttu-id="5526f-388">`<<<`, `>>>`</span><span class="sxs-lookup"><span data-stu-id="5526f-388">`<<<`, `>>>`</span></span> | <span data-ttu-id="5526f-389">이진</span><span class="sxs-lookup"><span data-stu-id="5526f-389">Binary</span></span> | <span data-ttu-id="5526f-390">왼쪽 시프트, 오른쪽 시프트</span><span class="sxs-lookup"><span data-stu-id="5526f-390">Left shift, right shift</span></span> | <span data-ttu-id="5526f-391">`Int` 또는 `BigInt`</span><span class="sxs-lookup"><span data-stu-id="5526f-391">`Int` or `BigInt`</span></span>
 <span data-ttu-id="5526f-392">`<`, `<=`, `>`, `>=`</span><span class="sxs-lookup"><span data-stu-id="5526f-392">`<`, `<=`, `>`, `>=`</span></span> | <span data-ttu-id="5526f-393">이진</span><span class="sxs-lookup"><span data-stu-id="5526f-393">Binary</span></span> | <span data-ttu-id="5526f-394">보다 작음, 작거나 같음, 보다 큼, 보다 큼, 크거나 같음 비교</span><span class="sxs-lookup"><span data-stu-id="5526f-394">Less-than, less-than-or-equal, greater-than, greater-than-or-equal comparisons</span></span> | <span data-ttu-id="5526f-395">`Int`, `BigInt` 또는 `Double`</span><span class="sxs-lookup"><span data-stu-id="5526f-395">`Int`, `BigInt` or `Double`</span></span>
 <span data-ttu-id="5526f-396">`==`, `!=`</span><span class="sxs-lookup"><span data-stu-id="5526f-396">`==`, `!=`</span></span> | <span data-ttu-id="5526f-397">이진</span><span class="sxs-lookup"><span data-stu-id="5526f-397">Binary</span></span> | <span data-ttu-id="5526f-398">같음, 같지 않음 비교</span><span class="sxs-lookup"><span data-stu-id="5526f-398">equal, not-equal comparisons</span></span> | <span data-ttu-id="5526f-399">모든 기본 형식</span><span class="sxs-lookup"><span data-stu-id="5526f-399">any primitive type</span></span>
 `&&&` | <span data-ttu-id="5526f-400">이진</span><span class="sxs-lookup"><span data-stu-id="5526f-400">Binary</span></span> | <span data-ttu-id="5526f-401">비트 AND</span><span class="sxs-lookup"><span data-stu-id="5526f-401">Bitwise AND</span></span> | <span data-ttu-id="5526f-402">`Int` 또는 `BigInt`</span><span class="sxs-lookup"><span data-stu-id="5526f-402">`Int` or `BigInt`</span></span>
 `^^^` | <span data-ttu-id="5526f-403">이진</span><span class="sxs-lookup"><span data-stu-id="5526f-403">Binary</span></span> | <span data-ttu-id="5526f-404">비트 XOR</span><span class="sxs-lookup"><span data-stu-id="5526f-404">Bitwise XOR</span></span> | <span data-ttu-id="5526f-405">`Int` 또는 `BigInt`</span><span class="sxs-lookup"><span data-stu-id="5526f-405">`Int` or `BigInt`</span></span>
 <code>\|\|\|</code> | <span data-ttu-id="5526f-406">이진</span><span class="sxs-lookup"><span data-stu-id="5526f-406">Binary</span></span> | <span data-ttu-id="5526f-407">비트 OR</span><span class="sxs-lookup"><span data-stu-id="5526f-407">Bitwise OR</span></span> | <span data-ttu-id="5526f-408">`Int` 또는 `BigInt`</span><span class="sxs-lookup"><span data-stu-id="5526f-408">`Int` or `BigInt`</span></span>
 `and` | <span data-ttu-id="5526f-409">이진</span><span class="sxs-lookup"><span data-stu-id="5526f-409">Binary</span></span> | <span data-ttu-id="5526f-410">논리적 AND</span><span class="sxs-lookup"><span data-stu-id="5526f-410">Logical AND</span></span> | `Bool`
 `or` | <span data-ttu-id="5526f-411">이진</span><span class="sxs-lookup"><span data-stu-id="5526f-411">Binary</span></span> | <span data-ttu-id="5526f-412">논리적 OR</span><span class="sxs-lookup"><span data-stu-id="5526f-412">Logical OR</span></span> | `Bool`
 `..` | <span data-ttu-id="5526f-413">Binary/삼항</span><span class="sxs-lookup"><span data-stu-id="5526f-413">Binary/Ternary</span></span> | <span data-ttu-id="5526f-414">Range 연산자</span><span class="sxs-lookup"><span data-stu-id="5526f-414">Range operator</span></span> | `Int`
 <span data-ttu-id="5526f-415">`?` `|`</span><span class="sxs-lookup"><span data-stu-id="5526f-415">`?` `|`</span></span> | <span data-ttu-id="5526f-416">진</span><span class="sxs-lookup"><span data-stu-id="5526f-416">Ternary</span></span> | <span data-ttu-id="5526f-417">조건부</span><span class="sxs-lookup"><span data-stu-id="5526f-417">Conditional</span></span> | <span data-ttu-id="5526f-418">`Bool` 왼쪽의 경우</span><span class="sxs-lookup"><span data-stu-id="5526f-418">`Bool` for the left-hand-side</span></span>
<span data-ttu-id="5526f-419">`w/` `<-`</span><span class="sxs-lookup"><span data-stu-id="5526f-419">`w/` `<-`</span></span> | <span data-ttu-id="5526f-420">진</span><span class="sxs-lookup"><span data-stu-id="5526f-420">Ternary</span></span> | <span data-ttu-id="5526f-421">복사 및 업데이트</span><span class="sxs-lookup"><span data-stu-id="5526f-421">Copy-and-update</span></span> | <span data-ttu-id="5526f-422">[복사 및 업데이트 식](#copy-and-update-expressions) 참조</span><span class="sxs-lookup"><span data-stu-id="5526f-422">See [Copy-and-update expressions](#copy-and-update-expressions)</span></span>

## <a name="next-steps"></a><span data-ttu-id="5526f-423">다음 단계</span><span class="sxs-lookup"><span data-stu-id="5526f-423">Next steps</span></span>

<span data-ttu-id="5526f-424">이제에서 식 작업을 수행할 수 있으므로의 Q# [작업 및 Q# 함수로](xref:microsoft.quantum.guide.operationsfunctions) 이동 하 여 작업 및 함수를 정의 하 고 호출 하는 방법을 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="5526f-424">Now that you can work with expressions in Q#, move on to [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions) to learn how to define and call operations and functions.</span></span>
