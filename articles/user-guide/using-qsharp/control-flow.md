---
title: 'Q의 제어 흐름 #'
description: 루프, 조건 등
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
ms.openlocfilehash: 1f1b641563fe35879abeee32b4f0aeeb7001b1a0
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84326543"
---
# <a name="control-flow-in-q"></a><span data-ttu-id="fa42d-103">Q의 제어 흐름 #</span><span class="sxs-lookup"><span data-stu-id="fa42d-103">Control Flow in Q#</span></span>

<span data-ttu-id="fa42d-104">작업 또는 함수 내에서 각 문은 순서 대로 실행 되며 가장 일반적인 명령적 언어와 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-104">Within an operation or function, each statement executes in order, similar to most common imperative classical languages.</span></span>
<span data-ttu-id="fa42d-105">그러나이 제어 흐름은 다음과 같은 세 가지 방법으로 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-105">This flow of control can be modified, however, in three distinct ways:</span></span>

- <span data-ttu-id="fa42d-106">`if`할당문</span><span class="sxs-lookup"><span data-stu-id="fa42d-106">`if` statements</span></span>
- <span data-ttu-id="fa42d-107">`for`하며</span><span class="sxs-lookup"><span data-stu-id="fa42d-107">`for` loops</span></span>
- <span data-ttu-id="fa42d-108">`repeat`-`until`하며</span><span class="sxs-lookup"><span data-stu-id="fa42d-108">`repeat`-`until` loops</span></span>

<span data-ttu-id="fa42d-109">후자는 [아래](#repeat-until-success-loop)에서 자세히 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-109">We defer discussion of the latter to further [below](#repeat-until-success-loop).</span></span>
<span data-ttu-id="fa42d-110">`if`그러나 및 `for` 제어 흐름 구문은 대부분의 일반적인 프로그래밍 언어에 대해 친숙 하 게 진행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-110">The `if` and `for` control flow constructs, however, proceed in a familiar sense to most classical programming languages.</span></span>

<span data-ttu-id="fa42d-111">중요 한 `for` `if` 것은 특수화가 자동 생성 되는 작업에 루프 및 문을 사용할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-111">Importantly, `for` loops and `if` statements can even be used in operations for which specializations are auto-generated.</span></span> <span data-ttu-id="fa42d-112">이 경우 루프의 adjoint는 `for` 방향을 바꾸고 각 반복의 adjoint를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-112">In that case the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="fa42d-113">이는 "신발 및 socks" 원칙을 따릅니다. 즉, socks에 배치를 취소 한 다음 신발로 전환 하려면 축구 전환에 대 한 실행을 취소 하 고 socks에 배치를 실행 취소 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-113">This follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span>
<span data-ttu-id="fa42d-114">계속 해 서 신발를 decidedly 하는 동안 시도 하 고 socks를 사용 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-114">It works decidedly less well to try and take your socks off while you're still wearing your shoes!</span></span>

## <a name="if-else-if-else"></a><span data-ttu-id="fa42d-115">If, Else-if, Else</span><span class="sxs-lookup"><span data-stu-id="fa42d-115">If, Else-if, Else</span></span>

<span data-ttu-id="fa42d-116">`if`문은 조건부 실행을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-116">The `if` statement supports conditional execution.</span></span>
<span data-ttu-id="fa42d-117">키워드 `if` , 여는 괄호 `(` , 부울 식, 닫는 괄호 `)` 및 문 블록 ( _then_ 블록)으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-117">It consists of the keyword `if`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="fa42d-118">그 다음에는 각각 키워드 `elif` , 여는 괄호 `(` , 부울 식, 닫는 괄호 `)` 및 문 블록 ( _else if_ 블록)으로 구성 된 여러 개의 else if 절이 올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-118">This may be followed by any number of else-if clauses, each of which consists of the keyword `elif`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="fa42d-119">마지막으로, `else` 다른 문 블록 ( _else_ 블록) 뒤에 오는 키워드로 구성 된 else 절을 사용 하 여 문을 선택적으로 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-119">Finally, the statement may optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>

<span data-ttu-id="fa42d-120">`if`조건이 평가 되 고 true 이면 then 블록이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-120">The `if` condition is evaluated, and if it is true, the then block is executed.</span></span>
<span data-ttu-id="fa42d-121">조건이 false 이면 첫 번째 else 조건이 평가 됩니다. true 이면 else 블록을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-121">If the condition is false, then the first else-if condition is evaluated; if it is true, that else-if block is executed.</span></span>
<span data-ttu-id="fa42d-122">그렇지 않으면 두 번째 else if 블록이 테스트 되 고, 세 번째는 조건이 true 인 절이 발생 하거나 else if 절이 더 이상 없을 때까지 테스트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-122">Otherwise, the second else-if block is tested, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="fa42d-123">원래 if 조건과 모든 else if 절이 false 이면 else 블록이 제공 된 경우 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-123">If the original if condition and all else-if clauses evaluate to false, the else block is executed if one was provided.</span></span>

<span data-ttu-id="fa42d-124">실행 되는 블록은 자체 범위에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-124">Note that whichever block is executed is executed in its own scope.</span></span>
<span data-ttu-id="fa42d-125">`if`, 또는 블록 내부에서 만들어진 바인딩은 `elif` `else` 끝 뒤에 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-125">Bindings made inside of an `if`, `elif`, or `else` block are not visible after its end.</span></span>

<span data-ttu-id="fa42d-126">예제:</span><span class="sxs-lookup"><span data-stu-id="fa42d-126">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
<span data-ttu-id="fa42d-127">또는</span><span class="sxs-lookup"><span data-stu-id="fa42d-127">or</span></span>
```qsharp
if (i == 1) {
    X(target);
    let n = 1;
} elif (i == 2) {
    Y(target);
    let m = n + 1; // would cause an error, because n is no longer bound
} else {
    Z(target);
}
```

## <a name="for-loop"></a><span data-ttu-id="fa42d-128">For 루프</span><span class="sxs-lookup"><span data-stu-id="fa42d-128">For Loop</span></span>

<span data-ttu-id="fa42d-129">`for`문은 정수 범위 또는 배열에 대 한 반복을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-129">The `for` statement supports iteration over an integer range or over an array.</span></span>
<span data-ttu-id="fa42d-130">문은 키워드, `for` 여는 괄호 `(` , 기호 또는 기호 튜플, 키워드 `in` , 형식 `Range` 또는 배열의 식, 닫는 괄호 `)` 및 문 블록으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-130">The statement consists of the keyword `for`, an open parenthesis `(`, followed by a symbol or symbol tuple, the keyword `in`, an expression of type `Range` or array, a close parenthesis `)`, and a statement block.</span></span>

<span data-ttu-id="fa42d-131">문 블록 (루프의 본문)은 범위 또는 배열의 각 값에 바인딩된 정의 된 기호 (루프 변수)를 사용 하 여 반복적으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-131">The statement block (the body of the loop) is executed repeatedly, with the defined symbol(s) (the loop variable(s)) bound to each value in the range or array.</span></span>
<span data-ttu-id="fa42d-132">범위 식이 빈 범위 또는 배열로 계산 되는 경우 본문은 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-132">Note that if the range expression evaluates to an empty range or array, the body will not be executed at all.</span></span>
<span data-ttu-id="fa42d-133">식은 루프를 시작 하기 전에 완전히 계산 되며 루프가 실행 되는 동안에는 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-133">The expression is fully evaluated before entering the loop, and will not change while the loop is executing.</span></span>

<span data-ttu-id="fa42d-134">루프 변수는 루프 본문에 대 한 각 입구에 바인딩되고 본문의 끝에서 바인딩되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-134">The loop variable is bound at each entrance to the loop body, and unbound at the end of the body.</span></span>
<span data-ttu-id="fa42d-135">특히 for 루프가 완료 된 후 루프 변수가 바인딩되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-135">In particular, the loop variable is not bound after the for loop is completed.</span></span>
<span data-ttu-id="fa42d-136">선언 된 기호의 바인딩은 변경할 수 없으며 다른 변수 바인딩과 동일한 규칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-136">The binding of the declared symbol(s) is immutable and follows the same rules as other variable bindings.</span></span> 

<span data-ttu-id="fa42d-137">몇 가지 예를 들어, 다음은 형식에 대 한 `qubits` 레지스터입니다. `Qubit[]`</span><span class="sxs-lookup"><span data-stu-id="fa42d-137">For some examples, supposing `qubits` is a register of qubits (i.e. of type `Qubit[]`),</span></span> 

```qsharp
// ...
for (qubit in qubits) {  // iterate over each qubit value in the array qubits
    H(qubit);
}
// 'qubit' is no longer bound

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {  // iterates over the integers in the Range 0 .. (Length(qubits) - 1)
    set results w/= index <- (index, M(qubits[index])); // measure each qubit, updates the tuple value in the results array that at index 
}

mutable accumulated = 0;
for ((index, measured) in results) { // iterates over the tuple values in results
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```
<span data-ttu-id="fa42d-138">끝에는 산술 시프트 왼쪽 이항 연산자를 사용 했습니다 .이에 대 한 `<<<` 세부 정보는 [숫자 식](xref:microsoft.quantum.guide.expressions#numeric-expressions) 에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-138">Note that at the end we utilized the arithmetic-shift-left binary operator, `<<<`, details of which can be found at [Numeric Expressions](xref:microsoft.quantum.guide.expressions#numeric-expressions)</span></span>


## <a name="repeat-until-success-loop"></a><span data-ttu-id="fa42d-139">반복-성공 루프</span><span class="sxs-lookup"><span data-stu-id="fa42d-139">Repeat-Until-Success Loop</span></span>

<span data-ttu-id="fa42d-140">Q # 언어를 사용 하면 기존 제어 흐름을 사용 하 여 다양 한 비트 측정 결과에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-140">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="fa42d-141">이 기능을 사용 하면 unitaries을 구현 하기 위한 계산 비용을 줄일 수 있는 강력한 확률 가젯을 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-141">This capability in turn enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="fa42d-142">예를 들어 Q #에서 쉽게 구현할 수 있습니다 (RUS ( *-성공-성공* ) 패턴 이라고 함).</span><span class="sxs-lookup"><span data-stu-id="fa42d-142">As an example, it is easy to implement so-called *Repeat-Until-Success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="fa42d-143">이러한 RUS 패턴은 기본 게이트 측면에서 비용이 *저렴 한* 확률 프로그램 이지만 실제 실행 및 가능한 여러 가지 branchings의 실제 인터리브에 따라 실질적인 비용이 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-143">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates, but for which the true cost depends on an actual run and an actual interleaving of various possible branchings.</span></span>

<span data-ttu-id="fa42d-144">반복-성공 (RUS) 패턴을 용이 하 게 하기 위해 Q #에서 구문을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-144">To facilitate Repeat-Until-Success (RUS) patterns, Q# supports the constructs</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

<span data-ttu-id="fa42d-145">여기서 `expression` 는 형식의 값으로 계산 되는 유효한 식입니다 `Bool` .</span><span class="sxs-lookup"><span data-stu-id="fa42d-145">where `expression` is any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="fa42d-146">루프 본문이 실행 된 후 조건이 평가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-146">The loop body is executed, and then the condition is evaluated.</span></span>
<span data-ttu-id="fa42d-147">조건이 true 이면 문이 완료 된 것입니다. 그렇지 않으면 픽스업이 실행 되 고 문이 루프 본문부터 다시 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-147">If the condition is true, then the statement is completed; otherwise, the fixup is executed, and the statement is re-executed starting with the loop body.</span></span>

<span data-ttu-id="fa42d-148">반복/until 루프의 세 부분 (본문, 테스트 및 픽스업)은 *각 반복에 대해*단일 범위로 처리 되므로 본문에 바인딩된 기호는 테스트 및 픽스업에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-148">All three portions of a repeat/until loop (the body, the test, and the fixup) are treated as a single scope *for each repetition*, so symbols that are bound in the body are available in the test and in the fixup.</span></span>
<span data-ttu-id="fa42d-149">그러나 픽스업 실행을 완료 하면 문 범위가 끝나기 때문에 본문 또는 픽스업 중에 만든 기호 바인딩을 후속 반복에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-149">However completing the execution of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="fa42d-150">또한 `fixup` 문은 종종 유용 하지만 항상 필요한 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-150">Further, the `fixup` statement is often useful but not always necessary.</span></span>
<span data-ttu-id="fa42d-151">필요 하지 않은 경우 구문은</span><span class="sxs-lookup"><span data-stu-id="fa42d-151">In cases that it is not needed, the construct</span></span>
```qsharp
repeat {
    // do stuff
}
until (expression);
```
<span data-ttu-id="fa42d-152">유효한 RUS 패턴 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-152">is also a valid RUS pattern.</span></span>

<span data-ttu-id="fa42d-153">이 페이지의 맨 아래에는 [RUS 루프의 몇 가지 예가 나와](#repeat-until-success-examples)있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-153">At the bottom of this page we present some [examples of RUS loops](#repeat-until-success-examples).</span></span>

> [!TIP]   
> <span data-ttu-id="fa42d-154">함수 내에서-success 루프를 사용 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="fa42d-154">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="fa42d-155">함수에서 루프를 통해 해당 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-155">The corresponding functionality is provided by while loops in functions.</span></span> 

## <a name="while-loop"></a><span data-ttu-id="fa42d-156">While 루프</span><span class="sxs-lookup"><span data-stu-id="fa42d-156">While Loop</span></span>

<span data-ttu-id="fa42d-157">반복-성공 패턴에는 퀀텀 별 connotation가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-157">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="fa42d-158">이러한 클래스는 특정 퀀텀 알고리즘 클래스에서 널리 사용 되므로 Q #에서 전용 언어 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-158">They are widely used in particular classes of quantum algorithms -- hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="fa42d-159">그러나 조건에 따라 중단 되 고 해당 실행 길이는 컴파일 시간에 알 수 없는 루프는 퀀텀 런타임에서 특히 주의 해 서 처리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-159">However, loops that break based on a condition and whose execution length is thus unknown at compile time need to be handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="fa42d-160">반면에 함수 내에서의 사용은 기존 (비 퀀텀) 하드웨어에서 실행 되는 코드만 포함 하기 때문에 문제가 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-160">Their use within functions on the other hand is unproblematic, since these only contain code that will be executed on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="fa42d-161">따라서 Q #은 함수 내 에서만 while 루프를 사용할 수 있도록 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-161">Q# therefore supports to use of while loops within functions only.</span></span> <span data-ttu-id="fa42d-162">`while`문은 키워드, 여는 `while` 괄호 `(` , 조건 (예: 부울 식), 닫는 괄호 `)` 및 문 블록으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-162">A `while` statement consists of the keyword `while`, an open parenthesis `(`, a condition (i.e. a Boolean expression), a close parenthesis `)`, and a statement block.</span></span>
<span data-ttu-id="fa42d-163">문 블록 (루프의 본문)은 조건이로 확인 되 면 실행 됩니다 `true` .</span><span class="sxs-lookup"><span data-stu-id="fa42d-163">The statement block (the body of the loop) is executed as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```


## <a name="return-statement"></a><span data-ttu-id="fa42d-164">Return 문</span><span class="sxs-lookup"><span data-stu-id="fa42d-164">Return Statement</span></span>

<span data-ttu-id="fa42d-165">Return 문은 작업 또는 함수의 실행을 종료 하 고 호출자에 게 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-165">The return statement ends execution of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="fa42d-166">키워드와 `return` 해당 형식의 식, 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-166">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="fa42d-167">빈 튜플을 반환 하는 호출 가능에는 `()` return 문이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-167">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
<span data-ttu-id="fa42d-168">초기 종료를 사용 하는 경우 `return ()` 이 경우를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-168">If an early exit is desired, `return ()` may be used in this case.</span></span>
<span data-ttu-id="fa42d-169">다른 형식을 반환 하는 callables에는 최종 return 문이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-169">Callables that return any other type require a final return statement.</span></span>

<span data-ttu-id="fa42d-170">작업 내에는 최대 개수의 return 문이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-170">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="fa42d-171">문이 블록 내의 return 문 뒤에 오는 경우 컴파일러는 경고를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-171">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

<span data-ttu-id="fa42d-172">예제:</span><span class="sxs-lookup"><span data-stu-id="fa42d-172">For example,</span></span>
```qsharp
return 1;
```
<span data-ttu-id="fa42d-173">또는</span><span class="sxs-lookup"><span data-stu-id="fa42d-173">or</span></span>
```qsharp
return ();
```
<span data-ttu-id="fa42d-174">또는</span><span class="sxs-lookup"><span data-stu-id="fa42d-174">or</span></span>
```qsharp
return (results, qubits);
```

## <a name="fail-statement"></a><span data-ttu-id="fa42d-175">Fail 문</span><span class="sxs-lookup"><span data-stu-id="fa42d-175">Fail Statement</span></span>

<span data-ttu-id="fa42d-176">Fail 문은 작업 실행을 종료 하 고 호출자에 게 오류 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-176">The fail statement ends execution of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="fa42d-177">키워드 `fail` 와 문자열 및 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-177">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="fa42d-178">문자열은 오류 메시지로 기존 드라이버에 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-178">The string is returned to the classical driver as the error message.</span></span>

<span data-ttu-id="fa42d-179">작업 내의 실패 문 수에 대 한 제한은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-179">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="fa42d-180">문이 블록 내의 fail 문 뒤에 오는 경우 컴파일러는 경고를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-180">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="fa42d-181">예제:</span><span class="sxs-lookup"><span data-stu-id="fa42d-181">For example,</span></span>
```qsharp
fail $"Impossible state reached";
```
<span data-ttu-id="fa42d-182">또는 [보간된 문자열](xref:microsoft.quantum.guide.expressions#interpolated-strings)을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="fa42d-182">or, using [interpolated strings](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span></span>
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a><span data-ttu-id="fa42d-183">반복-성공-성공 예</span><span class="sxs-lookup"><span data-stu-id="fa42d-183">Repeat-Until-Success Examples</span></span>

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a><span data-ttu-id="fa42d-184">무리 축에 대 한 단일 고 비트 회전에 대 한 RUS 패턴</span><span class="sxs-lookup"><span data-stu-id="fa42d-184">RUS pattern for single qubit rotation about an irrational axis</span></span> 

<span data-ttu-id="fa42d-185">일반적인 사용 사례에서 다음 Q # 연산은 Bloch 구의 $ (I + 2i Z)/\sqrt $의 무리 축을 중심으로 회전을 구현 {5} 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-185">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="fa42d-186">이 작업은 알려진 RUS 패턴을 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-186">This is accomplished by using a known RUS pattern:</span></span>

```qsharp
operation ApplyVRotationUsingRUS(qubit : Qubit) : Unit {
    using (controls = Qubit[2]) {
        ApplyToEachA(H, controls);
        mutable finished = false;
        repeat {
            Controlled X(controls, qubit);
            S(qubit);
            Controlled X(controls, qubit);
            Z(qubit);
        }
        until (finished)
        fixup {
            if (MeasureIfAllQubitsAreZero(controls, PauliX)) {
                set finished = true;
            }
        }
    }
}
```

### <a name="rus-loop-with-mutable-variable-in-scope"></a><span data-ttu-id="fa42d-187">범위에서 변경 가능한 변수가 있는 RUS 루프</span><span class="sxs-lookup"><span data-stu-id="fa42d-187">RUS loop with mutable variable in scope</span></span>

<span data-ttu-id="fa42d-188">이 예에서는 `finished` 전체 반복-픽스업 루프의 범위에 있고 루프 전에 초기화 되 고 픽스업 단계에서 업데이트 되는 변경 가능한 변수를 사용 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-188">This example shows the use of a mutable variable `finished` which is in scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

```qsharp
mutable iter = 1;
repeat {
    ProbabilisticCircuit(qubits);
    let success = ComputeSuccessIndicator(qubits);
}
until (success || iter > maxIter)
fixup {
    iter += 1;
    ComputeCorrection(qubits);
}
```

### <a name="rus-without-fixup"></a><span data-ttu-id="fa42d-189">RUS (없음)`fixup`</span><span class="sxs-lookup"><span data-stu-id="fa42d-189">RUS without `fixup`</span></span>

<span data-ttu-id="fa42d-190">예를 들어 다음 코드는 {5} 및 게이트를 사용 하 여 $V _3 = (\boldone + 2 i Z)/\sqrt $ 중요 한 회전 게이트를 구현 하는 확률 회로입니다 `H` `T` .</span><span class="sxs-lookup"><span data-stu-id="fa42d-190">For example, the following code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the `H` and `T` gates.</span></span>
<span data-ttu-id="fa42d-191">루프는 평균에서 $ \frac {8} {5} $ 반복을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-191">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="fa42d-192">자세한 내용은 [*반복-성공--성공: 단일 기능 비트 unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick 및 svore, 2014)의 비결 정적 분해를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fa42d-192">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for more details.</span></span>

```qsharp
using (qubit = Qubit()) {
    repeat {
        H(qubit);
        T(qubit);
        CNOT(target, qubit);
        H(qubit);
        Adjoint T(qubit);
        H(qubit);
        T(qubit);
        H(qubit);
        CNOT(target, qubit);
        T(qubit);
        Z(target);
        H(qubit);
        let result = M(qubit);
    } until (result == Zero);
}
```

### <a name="rus-to-prepare-a-quantum-state"></a><span data-ttu-id="fa42d-193">퀀텀 상태를 준비 하기 위한 RUS</span><span class="sxs-lookup"><span data-stu-id="fa42d-193">RUS to prepare a quantum state</span></span>

<span data-ttu-id="fa42d-194">마지막으로 {1} $ \ket{+} $ 상태에서 시작 하 여 퀀텀 상태 $ \frac {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $를 준비 하는 RUS 패턴의 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-194">Finally, we show an example of a RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>
<span data-ttu-id="fa42d-195">[표준 라이브러리와 함께 제공 되는 단위 테스트 샘플](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs)도 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fa42d-195">See also the [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+> state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+> state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+> state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+> state on the auxiliary qubit
            // is 3/4.
            AssertProb(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+> in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+> state.
            if (outcome == One) {
                Z(auxiliary);
                X(target);
                H(target);
            }
        }
        // Return the auxiliary qubit back to the Zero state.
        H(auxiliary);
    }
}
```

<span data-ttu-id="fa42d-196">이 작업에 표시 되는 주목할 만한 프로그래밍 기능은 `fixup` 퀀텀 작업을 포함 하는 루프의 더 복잡 한 부분이 며, `AssertProb` 문을 사용 하 여 프로그램의 지정 된 특정 지점에서 퀀텀 상태를 측정 하는 확률을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-196">Notable programmatic features shown in this operation are a more complex `fixup` part of the loop, which involves quantum operations, and the use of `AssertProb` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>
<span data-ttu-id="fa42d-197">및 작업에 대 한 자세한 내용은 [테스트 및 디버깅](xref:microsoft.quantum.guide.testingdebugging) 을 참조 하세요 [`Assert`](xref:microsoft.quantum.intrinsic.assert) [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) .</span><span class="sxs-lookup"><span data-stu-id="fa42d-197">See also [Testing and debugging](xref:microsoft.quantum.guide.testingdebugging) for more information about the [`Assert`](xref:microsoft.quantum.intrinsic.assert) and [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) operations.</span></span>


## <a name="next-steps"></a><span data-ttu-id="fa42d-198">다음 단계</span><span class="sxs-lookup"><span data-stu-id="fa42d-198">Next steps</span></span>

<span data-ttu-id="fa42d-199">Q #에서 [테스트 및 디버깅](xref:microsoft.quantum.guide.testingdebugging) 에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="fa42d-199">Learn about [Testing and Debugging](xref:microsoft.quantum.guide.testingdebugging) in Q#.</span></span>