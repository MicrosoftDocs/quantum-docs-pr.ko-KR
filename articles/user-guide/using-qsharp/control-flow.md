---
title: 제어 흐름Q#
description: 루프, 조건 등
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
no-loc:
- Q#
- $$v
ms.openlocfilehash: fc619d64bfebfc27d7feac6dafb2dd4cf22825d6
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867950"
---
# <a name="control-flow-in-no-locq"></a><span data-ttu-id="64f82-103">제어 흐름Q#</span><span class="sxs-lookup"><span data-stu-id="64f82-103">Control flow in Q#</span></span>

<span data-ttu-id="64f82-104">작업 또는 함수 내에서 각 문은 다른 일반적인 명령적 언어와 비슷하게 순서 대로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-104">Within an operation or function, each statement runs in order, similar to other common imperative classical languages.</span></span>
<span data-ttu-id="64f82-105">그러나 다음과 같은 세 가지 방법으로 제어 흐름을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-105">However, you can modify the flow of control in three distinct ways:</span></span>

* <span data-ttu-id="64f82-106">`if`할당문</span><span class="sxs-lookup"><span data-stu-id="64f82-106">`if` statements</span></span>
* <span data-ttu-id="64f82-107">`for`하며</span><span class="sxs-lookup"><span data-stu-id="64f82-107">`for` loops</span></span>
* <span data-ttu-id="64f82-108">`repeat-until-success`하며</span><span class="sxs-lookup"><span data-stu-id="64f82-108">`repeat-until-success` loops</span></span>

<span data-ttu-id="64f82-109">`if`및 `for` 제어 흐름 구성은 대부분의 일반적인 프로그래밍 언어에 대해 친숙 하 게 진행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-109">The `if` and `for` control flow constructs proceed in a familiar sense to most classical programming languages.</span></span> <span data-ttu-id="64f82-110">[`Repeat-until-success`](#repeat-until-success-loop)루프는이 문서의 뒷부분에서 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-110">[`Repeat-until-success`](#repeat-until-success-loop) loops are discussed later in this article.</span></span>

<span data-ttu-id="64f82-111">중요 한 `for` `if` 것은 [특수화](xref:microsoft.quantum.guide.operationsfunctions) 가 자동 생성 되는 작업에 루프 및 문을 사용할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-111">Importantly, `for` loops and `if` statements can be used in operations for which [specializations](xref:microsoft.quantum.guide.operationsfunctions) are auto-generated.</span></span> <span data-ttu-id="64f82-112">이 시나리오에서 루프의 adjoint는 `for` 방향을 바꾸고 각 반복의 adjoint를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-112">In that scenario, the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="64f82-113">이 작업은 "신발 및 socks" 원칙을 따릅니다. 즉, socks에 배치를 취소 한 다음 신발로 전환 하려면 축구 전환에 대 한 실행을 취소 하 고 socks에 배치를 실행 취소 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-113">This action follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span> 

## <a name="if-else-if-else"></a><span data-ttu-id="64f82-114">If, Else-if, Else</span><span class="sxs-lookup"><span data-stu-id="64f82-114">If, Else-if, Else</span></span>

<span data-ttu-id="64f82-115">`if`문은 조건부 실행을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-115">The `if` statement supports conditional execution.</span></span>
<span data-ttu-id="64f82-116">키워드 `if` , 괄호 안의 부울 식, 문 블록 ( _then_ 블록)으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-116">It consists of the keyword `if`, a Boolean expression in parentheses, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="64f82-117">필요에 따라, 각각 키워드 `elif` , 괄호 안의 부울 식 및 문 블록 ( _else-if_ 블록)으로 구성 된 else 절을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-117">Optionally, any number of else-if clauses can follow, each of which consists of the keyword `elif`, a Boolean expression in parentheses, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="64f82-118">마지막으로, `else` 다른 문 블록 ( _else_ 블록) 뒤에 오는 키워드로 구성 된 else 절을 사용 하 여 문을 선택적으로 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-118">Finally, the statement can optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>

<span data-ttu-id="64f82-119">`if`조건이 평가 되 고 *true*인 경우 *에는* 블록이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-119">The `if` condition is evaluated, and if it is *true*, the *then* block is run.</span></span>
<span data-ttu-id="64f82-120">조건이 *false*이면 첫 번째 else 조건이 평가 됩니다. 해당 하는 경우 *else* 블록을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-120">If the condition is *false*, then the first else-if condition is evaluated; if that is true, then the *else-if* block is run.</span></span>
<span data-ttu-id="64f82-121">그렇지 않은 경우 두 번째 else if 블록은를 계산 하 고, 세 번째는 true 조건이 있는 절이 발견 되거나 else if 절이 없을 때까지 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-121">Otherwise, the second else-if block evaluates, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="64f82-122">원래 *if* 조건과 모든 else if 절이 *false*이면 *else* 블록이 실행 됩니다 (제공 된 경우).</span><span class="sxs-lookup"><span data-stu-id="64f82-122">If the original *if* condition and all the else-if clauses evaluate to *false*, the *else* block is run, if provided.</span></span>

<span data-ttu-id="64f82-123">실행 되는 블록이 무엇이 든 해당 범위 내에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-123">Note that whichever block runs, it runs within its own scope.</span></span>
<span data-ttu-id="64f82-124">`if`, 또는 블록 내부에서 만들어진 바인딩은 `elif` `else` 블록이 끝난 후에는 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-124">Bindings made inside of an `if`, `elif`, or `else` block are not visible after the block ends.</span></span>

<span data-ttu-id="64f82-125">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-125">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
<span data-ttu-id="64f82-126">또는</span><span class="sxs-lookup"><span data-stu-id="64f82-126">or</span></span>
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

## <a name="for-loop"></a><span data-ttu-id="64f82-127">For 루프</span><span class="sxs-lookup"><span data-stu-id="64f82-127">For loop</span></span>

<span data-ttu-id="64f82-128">`for`문은 정수 범위 또는 배열에 대 한 반복을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-128">The `for` statement supports iteration over an integer range or an array.</span></span>
<span data-ttu-id="64f82-129">문은 키워드로 구성 된 `for` 다음 기호 또는 기호 튜플, 키워드 `in` , 형식 `Range` 또는 배열의 식, 괄호 안에 있는 식 및 문 블록으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-129">The statement consists of the keyword `for`, followed by a symbol or symbol tuple, the keyword `in`, and an expression of type `Range` or array, all in parentheses, and a statement block.</span></span>

<span data-ttu-id="64f82-130">문 블록 (루프의 본문)은 범위 또는 배열의 각 값에 바인딩된 정의 된 기호 (루프 변수)를 사용 하 여 반복적으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-130">The statement block (the body of the loop) runs repeatedly, with the defined symbol (the loop variable) bound to each value in the range or array.</span></span>
<span data-ttu-id="64f82-131">범위 식이 빈 범위 또는 배열로 계산 되는 경우 본문은 전혀 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-131">Note that if the range expression evaluates to an empty range or array, the body does not run at all.</span></span>
<span data-ttu-id="64f82-132">루프를 시작 하기 전에 식이 완전히 계산 되며 루프가 실행 되는 동안에는 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-132">The expression is fully evaluated before entering the loop, and does not change while the loop is executing.</span></span>

<span data-ttu-id="64f82-133">루프 변수는 루프 본문에 대 한 각 입구에 바인딩되고 본문의 끝에서 바인딩되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-133">The loop variable is bound at each entrance to the loop body, and is unbound at the end of the body.</span></span>
<span data-ttu-id="64f82-134">For 루프가 완료 된 후 루프 변수가 바인딩되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-134">The loop variable is not bound after the for loop is completed.</span></span>
<span data-ttu-id="64f82-135">루프 변수의 바인딩은 변경할 수 없으며 다른 변수 바인딩과 동일한 규칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-135">The binding of the loop variable is immutable and follows the same rules as other variable bindings.</span></span> 

<span data-ttu-id="64f82-136">이 예제에서 `qubits` 는의 레지스터 (즉, 형식)입니다. `Qubit[]`</span><span class="sxs-lookup"><span data-stu-id="64f82-136">In these examples, `qubits` is a register of qubits (i.e. of type `Qubit[]`),</span></span> 

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

<span data-ttu-id="64f82-137">끝에는 산술 시프트 왼쪽 이항 연산자를 사용 했습니다 `<<<` .</span><span class="sxs-lookup"><span data-stu-id="64f82-137">Note that at the end, we utilized the arithmetic-shift-left binary operator, `<<<`.</span></span> <span data-ttu-id="64f82-138">자세한 내용은 [숫자 식](xref:microsoft.quantum.guide.expressions#numeric-expressions)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64f82-138">For more information, see [Numeric Expressions](xref:microsoft.quantum.guide.expressions#numeric-expressions).</span></span>

## <a name="repeat-until-success-loop"></a><span data-ttu-id="64f82-139">반복-성공 루프</span><span class="sxs-lookup"><span data-stu-id="64f82-139">Repeat-until-success loop</span></span>

<span data-ttu-id="64f82-140">이 Q# 언어를 사용 하면 기존 제어 흐름을 사용 하 여 다양 한 비트를 측정 한 결과에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-140">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="64f82-141">이 기능을 사용 하면 unitaries를 구현 하기 위한 계산 비용을 줄일 수 있는 강력한 확률 가젯을 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-141">This capability, in turn, enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="64f82-142">이에 대 한 예는의 RUS ( *-성공-성공* ) 패턴입니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="64f82-142">Examples of this are the *repeat-until-success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="64f82-143">이러한 RUS 패턴은 기본 게이트 측면에서 저렴 한 비용으로 *예상* 되는 확률 프로그램입니다. 발생 한 비용은 실제 실행 및 가능한 여러 branchings의 인터리빙에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-143">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates; the incurred cost depends on the actual run and the interleaving of the multiple possible branchings.</span></span>

<span data-ttu-id="64f82-144">성공-성공 (RUS) 패턴을 용이 하 게 하기 위해에서 Q# 구문을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-144">To facilitate repeat-until-success (RUS) patterns, Q# supports the constructs</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

<span data-ttu-id="64f82-145">여기서 `expression` 는 형식의 값으로 계산 되는 유효한 식입니다 `Bool` .</span><span class="sxs-lookup"><span data-stu-id="64f82-145">where `expression` is any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="64f82-146">루프 본문이 실행 된 후 조건이 평가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-146">The loop body runs, and then the condition is evaluated.</span></span>
<span data-ttu-id="64f82-147">조건이 true 이면 문이 완료 된 것입니다. 그렇지 않으면 픽스업이 실행 되 고 문이 루프 본문부터 다시 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-147">If the condition is true, then the statement is completed; otherwise, the fixup runs, and the statement runs again, starting with the loop body.</span></span>

<span data-ttu-id="64f82-148">RUS 루프의 세 부분 (본문, 테스트 및 수정)은 *각 반복에 대해*단일 범위로 처리 되므로 본문에 바인딩된 기호는 테스트와 픽스업에서 모두 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-148">All three portions of an RUS loop (the body, the test, and the fixup) are treated as a single scope *for each repetition*, so symbols that are bound in the body are available in both the test and the fixup.</span></span>
<span data-ttu-id="64f82-149">그러나 픽스업 실행을 완료 하면 문 범위가 끝나기 때문에 본문 또는 픽스업 중에 만든 기호 바인딩을 후속 반복에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-149">However, completing the execution of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="64f82-150">또한 `fixup` 문은 종종 유용 하지만 항상 필요한 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-150">Further, the `fixup` statement is often useful but not always necessary.</span></span>
<span data-ttu-id="64f82-151">필요 하지 않은 경우 구문은</span><span class="sxs-lookup"><span data-stu-id="64f82-151">In cases that it is not needed, the construct</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression);
```

<span data-ttu-id="64f82-152">유효한 RUS 패턴 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-152">is also a valid RUS pattern.</span></span>

<span data-ttu-id="64f82-153">더 많은 예제 및 세부 정보는이 문서의 [반복-성공 예](#repeat-until-success-examples) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64f82-153">For more examples and details, see [Repeat-until-success examples](#repeat-until-success-examples) in this article.</span></span>

> [!TIP]   
> <span data-ttu-id="64f82-154">함수 내에서-success 루프를 사용 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="64f82-154">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="64f82-155">*While* 루프를 사용 하 여 함수 내에 해당 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-155">Use *while* loops to provide the corresponding functionality inside functions.</span></span> 

## <a name="while-loop"></a><span data-ttu-id="64f82-156">While 루프</span><span class="sxs-lookup"><span data-stu-id="64f82-156">While loop</span></span>

<span data-ttu-id="64f82-157">반복-성공 패턴에는 퀀텀 별 connotation가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-157">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="64f82-158">이러한 클래스는 특정 퀀텀 알고리즘 클래스에서 널리 사용 되므로의 전용 언어 구문 Q# 입니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-158">They are widely used in particular classes of quantum algorithms - hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="64f82-159">그러나 조건에 따라 중단 되 고 해당 실행 길이는 컴파일 시간에 알 수 없는 루프는 퀀텀 런타임에서 특히 주의 해 서 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-159">However, loops that break based on a condition and whose execution length is thus unknown at compile-time, are handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="64f82-160">그러나 이러한 루프는 기존 (비 퀀텀) 하드웨어에서 실행 되는 코드만 포함 하므로 함수 내에서 사용 하는 것은 문제가 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-160">However, their use within functions is unproblematic since these loops only contain code that runs on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="64f82-161">Q#따라서는 함수 내 에서만 루프를 사용할 수 있도록 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-161">Q#, therefore, supports to use of while loops within functions only.</span></span> <span data-ttu-id="64f82-162">`while`문은 키워드 `while` , 괄호 안의 부울 식 및 문 블록으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-162">A `while` statement consists of the keyword `while`, a Boolean expression in parentheses, and a statement block.</span></span>
<span data-ttu-id="64f82-163">문 블록 (루프의 본문)은 조건이로 확인 되 면 실행 됩니다 `true` .</span><span class="sxs-lookup"><span data-stu-id="64f82-163">The statement block (the body of the loop) runs as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

## <a name="return-statement"></a><span data-ttu-id="64f82-164">Return 문</span><span class="sxs-lookup"><span data-stu-id="64f82-164">Return Statement</span></span>

<span data-ttu-id="64f82-165">Return 문은 작업 또는 함수의 실행을 종료 하 고 호출자에 게 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-165">The return statement ends the run of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="64f82-166">키워드와 `return` 해당 형식의 식, 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-166">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="64f82-167">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-167">For example,</span></span>
```qsharp
return 1;
```
<span data-ttu-id="64f82-168">또는</span><span class="sxs-lookup"><span data-stu-id="64f82-168">or</span></span>
```qsharp
return (results, qubits);
```

* <span data-ttu-id="64f82-169">빈 튜플을 반환 하는 호출 가능에는 `()` return 문이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-169">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
* <span data-ttu-id="64f82-170">작업 또는 함수에서 조기 종료를 지정 하려면를 사용 `return ();` 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-170">To specify an early exit from the operation or function, use `return ();`.</span></span>
<span data-ttu-id="64f82-171">다른 형식을 반환 하는 callables에는 최종 return 문이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-171">Callables that return any other type require a final return statement.</span></span>
* <span data-ttu-id="64f82-172">작업 내에는 최대 개수의 return 문이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-172">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="64f82-173">문이 블록 내의 return 문 뒤에 오는 경우 컴파일러는 경고를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-173">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

   
## <a name="fail-statement"></a><span data-ttu-id="64f82-174">Fail 문</span><span class="sxs-lookup"><span data-stu-id="64f82-174">Fail statement</span></span>

<span data-ttu-id="64f82-175">Fail 문은 작업 실행을 종료 하 고 호출자에 게 오류 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-175">The fail statement ends the run of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="64f82-176">키워드 `fail` 와 문자열 및 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-176">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="64f82-177">문은 오류 메시지로 기존 드라이버에 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-177">The statement returns the string to the classical driver as the error message.</span></span>

<span data-ttu-id="64f82-178">작업 내의 실패 문 수에 대 한 제한은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-178">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="64f82-179">문이 블록 내의 fail 문 뒤에 오는 경우 컴파일러는 경고를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-179">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="64f82-180">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-180">For example,</span></span>

```qsharp
fail $"Impossible state reached";
```
<span data-ttu-id="64f82-181">또는 [보간된 문자열](xref:microsoft.quantum.guide.expressions#interpolated-strings)을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="64f82-181">or, using [interpolated strings](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span></span>
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a><span data-ttu-id="64f82-182">반복-성공-성공 예</span><span class="sxs-lookup"><span data-stu-id="64f82-182">Repeat-until-success examples</span></span>

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a><span data-ttu-id="64f82-183">무리 축에 대 한 단일 비트 회전에 대 한 RUS 패턴</span><span class="sxs-lookup"><span data-stu-id="64f82-183">RUS pattern for single-qubit rotation about an irrational axis</span></span> 

<span data-ttu-id="64f82-184">일반적인 사용 사례에서 다음 Q# 작업은 Bloch 구의 $ (I + 2i Z)/\sqrt $의 무리 축을 중심으로 회전을 구현 {5} 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-184">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="64f82-185">구현에서는 알려진 RUS 패턴을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-185">The implementation uses a known RUS pattern:</span></span>

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

### <a name="rus-loop-with-a-mutable-variable-in-scope"></a><span data-ttu-id="64f82-186">범위에 변경 가능한 변수가 있는 RUS 루프</span><span class="sxs-lookup"><span data-stu-id="64f82-186">RUS loop with a mutable variable in scope</span></span>

<span data-ttu-id="64f82-187">이 예에서는 `finished` 전체 반복-픽스업 루프의 범위 내에 있고 루프 앞에서 초기화 되 고 픽스업 단계에서 업데이트 되는 변경 가능한 변수를 사용 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-187">This example shows the use of a mutable variable, `finished`, which is within the scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

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

### <a name="rus-without-fixup"></a><span data-ttu-id="64f82-188">RUS (없음)`fixup`</span><span class="sxs-lookup"><span data-stu-id="64f82-188">RUS without `fixup`</span></span>

<span data-ttu-id="64f82-189">이 예제에서는 픽스업 단계가 없는 RUS 루프를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-189">This example shows an RUS loop without the fixup step.</span></span> <span data-ttu-id="64f82-190">이 코드는 {5} 및 게이트를 사용 하 여 $V _3 = (\boldone + 2 i Z)/\sqrt $ 중요 한 회전 게이트를 구현 하는 확률 회로입니다 `H` `T` .</span><span class="sxs-lookup"><span data-stu-id="64f82-190">The code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the `H` and `T` gates.</span></span>
<span data-ttu-id="64f82-191">루프는 평균에서 $ \frac {8} {5} $ 반복을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-191">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="64f82-192">자세한 내용은 [*반복-성공--성공: 단일 기능 비트 unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick 및 svore, 2014)의 비결 정적 분해를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64f82-192">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for more details.</span></span>

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

### <a name="rus-to-prepare-a-quantum-state"></a><span data-ttu-id="64f82-193">퀀텀 상태를 준비 하기 위한 RUS</span><span class="sxs-lookup"><span data-stu-id="64f82-193">RUS to prepare a quantum state</span></span>

<span data-ttu-id="64f82-194">마지막으로, 다음은 {1} $ \ket{+} $ 상태에서 시작 하 여 퀀텀 상태 $ \frac {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $를 준비 하는 RUS 패턴의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-194">Finally, here is an example of an RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>

<span data-ttu-id="64f82-195">이 작업에 표시 되는 주목할 만한 프로그래밍 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-195">Notable programmatic features shown in this operation are:</span></span>

* <span data-ttu-id="64f82-196">`fixup`퀀텀 작업과 관련 된 루프의 더 복잡 한 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-196">A more complex `fixup` part of the loop, which involves quantum operations.</span></span> 
* <span data-ttu-id="64f82-197">`AssertMeasurementProbability`문을 사용 하 여 프로그램의 지정 된 특정 지점에서 퀀텀 상태를 측정 하는 확률을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f82-197">The use of `AssertMeasurementProbability` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>

<span data-ttu-id="64f82-198">및 작업에 대 한 자세한 내용은 [`AssertMeasurement`](xref:microsoft.quantum.diagnostics.assertmeasurement) [`AssertMeasurementProbability`](xref:microsoft.quantum.diagnostics.assertmeasurementprobability) [테스트 및 디버깅](xref:microsoft.quantum.guide.testingdebugging)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64f82-198">For more information about the [`AssertMeasurement`](xref:microsoft.quantum.diagnostics.assertmeasurement) and [`AssertMeasurementProbability`](xref:microsoft.quantum.diagnostics.assertmeasurementprobability) operations, see [Testing and debugging](xref:microsoft.quantum.guide.testingdebugging).</span></span>

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+> state.
            AssertMeasurementProbability(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+> state", 1e-10 );
            AssertMeasurementProbability(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+> state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+> state on the auxiliary qubit
            // is 3/4.
            AssertMeasurementProbability(
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

<span data-ttu-id="64f82-199">자세한 내용은 [표준 라이브러리와 함께 제공 되는 단위 테스트 샘플](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64f82-199">For more information, see [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

## <a name="next-steps"></a><span data-ttu-id="64f82-200">다음 단계</span><span class="sxs-lookup"><span data-stu-id="64f82-200">Next steps</span></span>

<span data-ttu-id="64f82-201">에서 [테스트 및 디버깅](xref:microsoft.quantum.guide.testingdebugging) 에 대해 알아봅니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="64f82-201">Learn about [Testing and Debugging](xref:microsoft.quantum.guide.testingdebugging) in Q#.</span></span>
