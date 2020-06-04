---
title: 'Q의 변수 #'
description: 채우기 설명
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.variables
ms.openlocfilehash: 456c05d4ca66a747e0cc514a30c6bbb33610f481
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327784"
---
# <a name="variables-in-q"></a><span data-ttu-id="24ece-103">Q의 변수 #</span><span class="sxs-lookup"><span data-stu-id="24ece-103">Variables in Q#</span></span>

<span data-ttu-id="24ece-104">Q #은 변경 불가능 한 기호 또는 식에 바인딩된/할당 된 "변수"를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-104">Q# distinguishes between mutable and immutable symbols, or "variables", which are bound/assigned to expressions.</span></span>
<span data-ttu-id="24ece-105">일반적으로 컴파일러에서 더 많은 최적화를 수행할 수 있기 때문에 변경할 수 없는 기호를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-105">In general, the use of immutable symbols is encouraged because it allows the compiler to perform more optimizations.</span></span>

<span data-ttu-id="24ece-106">바인딩의 왼쪽은 기호 튜플 및 식의 오른쪽으로 구성 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-106">The left-hand-side of a binding consists of a symbol tuple, and the right hand side of an expression.</span></span>

## <a name="immutable-variables"></a><span data-ttu-id="24ece-107">변경할 수 없는 변수</span><span class="sxs-lookup"><span data-stu-id="24ece-107">Immutable Variables</span></span>

<span data-ttu-id="24ece-108">Q #의 모든 형식 값은 키워드를 사용 하 여 작업 또는 함수 내에서 다시 사용 하기 위해 변수에 할당할 수 있습니다 `let` .</span><span class="sxs-lookup"><span data-stu-id="24ece-108">A value of any type in Q# can be assigned to a variable for reuse within an operation or function by using the `let` keyword.</span></span>

<span data-ttu-id="24ece-109">변경할 수 없는 바인딩은 키워드로 구성 된 `let` 다음에는 기호 또는 기호 튜플, 등호 `=` , 기호를 바인딩할 식, 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-109">An immutable binding consists of the keyword `let`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>

<span data-ttu-id="24ece-110">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-110">For instance:</span></span>

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

<span data-ttu-id="24ece-111">이렇게 하면 특정 형식의 Pauli 연산자가 변수 이름 (또는 "symbol")에 할당 `measurementOperator` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-111">This assigns a particular array of Pauli operators to the variable name (or "symbol"), `measurementOperator`.</span></span>

> [!NOTE]
> <span data-ttu-id="24ece-112">문의 오른쪽에 있는 식이 `let` 명확 하 고 형식이 컴파일러에서 유추 되기 때문에 새 변수의 형식을 명시적으로 지정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-112">We did not need to explicitly specify the type of our new variable, as the expression on the right-hand side of the `let` statement is unambiguous and the type is inferred by the compiler.</span></span> 

<span data-ttu-id="24ece-113">을 사용 하 여 정의 된 변수 `let` 는 *변경할*수 없습니다. 즉, 정의 된 후에는 더 이상 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-113">Variables defined using `let` are *immutable*, meaning that once it has been defined, it can no longer be changed in any way.</span></span>
<span data-ttu-id="24ece-114">이렇게 하면 작업의 변형을 적용 하기 위해 다시 정렬할 변수에 적용 되는 기존 논리의 최적화를 비롯 하 여 여러 가지 유용한 최적화를 수행할 수 있습니다 `Adjoint` .</span><span class="sxs-lookup"><span data-stu-id="24ece-114">This allows for several beneficial optimizations, including optimization of the classical logic acting on variables to be reordered for applying the `Adjoint` variant of an operation.</span></span>

## <a name="mutable-variables"></a><span data-ttu-id="24ece-115">변경 가능한 변수</span><span class="sxs-lookup"><span data-stu-id="24ece-115">Mutable Variables</span></span>

<span data-ttu-id="24ece-116">를 사용 하 여 변수를 만드는 대신 키워드를 `let` `mutable` 사용 하 여 처음 생성 된 후에 다시 바인딩할 *수* 있는 변경 가능한 변수를 만듭니다 `set` .</span><span class="sxs-lookup"><span data-stu-id="24ece-116">As an alternative to creating a variable with `let`, the `mutable` keyword will create a mutable variable that *can* be re-bound after it is initially created by using the `set` keyword.</span></span>

<span data-ttu-id="24ece-117">문의 일부로 선언 되 고 바인딩된 기호는 `mutable` 코드에서 나중에 다른 값에 다시 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-117">Symbols declared and bound as part of a `mutable` statement may be rebound to a different value later in the code.</span></span> <span data-ttu-id="24ece-118">기호를 코드에서 나중에 다시 바인딩하는 경우 해당 형식은 변경 되지 않으며 새로 바인딩된 값은 해당 형식과 호환 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-118">If a symbol is rebound later in the code, its type does not change, and the newly bound value needs to be compatible with that type.</span></span>

### <a name="rebinding-of-mutable-symbols"></a><span data-ttu-id="24ece-119">변경 가능한 기호 리바인딩</span><span class="sxs-lookup"><span data-stu-id="24ece-119">Rebinding of Mutable Symbols</span></span>

<span data-ttu-id="24ece-120">문을 사용 하 여 변경할 수 있는 변수를 바인딩할 수 있습니다 `set` .</span><span class="sxs-lookup"><span data-stu-id="24ece-120">A mutable variable may be rebound using a `set` statement.</span></span>
<span data-ttu-id="24ece-121">이러한 리바인딩은 키워드로 구성 된 `set` 후 기호 또는 기호 튜플, 등호 `=` , 기호를에 다시 바인딩하는 식, 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-121">Such a rebinding consists of the keyword `set`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to rebind the symbol(s) to, and a terminating semicolon.</span></span>

<span data-ttu-id="24ece-122">여기에서 몇 가지 가능한 리바인딩 문 기술 예제를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-122">Here, we provide some possible examples of rebinding statement techniques</span></span>

### <a name="apply-and-reassign-statements"></a><span data-ttu-id="24ece-123">적용 및 재할당 문</span><span class="sxs-lookup"><span data-stu-id="24ece-123">Apply-and-Reassign Statements</span></span>

<span data-ttu-id="24ece-124">`set` *적용 및 재할당* 문으로 제공 되는 특정 종류의 문은 오른쪽이 이항 연산자의 응용 프로그램으로 구성 되 고 결과가 연산자의 왼쪽 인수에 다시 바인딩 되는 경우 연결 하는 편리한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-124">A particular kind of `set`-statement we refer to as an *apply-and-reassign* statement provides a convenient way of concatenation if the right hand side consists of the application of a binary operator and the result is to be rebound to the left argument to the operator.</span></span> <span data-ttu-id="24ece-125">예제:</span><span class="sxs-lookup"><span data-stu-id="24ece-125">For example,</span></span>
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
<span data-ttu-id="24ece-126">`counter`루프의 각 반복에서 카운터의 값을 증가 시킵니다 `for` .</span><span class="sxs-lookup"><span data-stu-id="24ece-126">increments the value of the counter `counter` in each iteration of the `for` loop.</span></span> <span data-ttu-id="24ece-127">위의 코드는와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-127">The code above is equivalent to</span></span> 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```

<span data-ttu-id="24ece-128">왼쪽의 형식이 식 형식과 일치 하는 모든 이항 연산자에 대해 비슷한 문을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-128">Similar statements are available for all binary operators in which the type of the left-hand-side matches the expression type.</span></span> <span data-ttu-id="24ece-129">예를 들어 값을 누적 하는 편리한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-129">This provides for example a convenient way to accumulate values.</span></span>

<span data-ttu-id="24ece-130">예를 들어, 다음과 같은 경우에는 `qubits` 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-130">For example, supposing `qubits` is a regsiter of qubits:</span></span>
```qsharp
mutable results = new Result[0];   // results is an empty array of type Result[]
for (q in qubits) {
    set results += [M(q)];         // concatenate the outcome from measuring q to the existing array
    // ...
}
...                                // results contains the measurement outcomes from the whole register
```

### <a name="update-and-reassign-statements"></a><span data-ttu-id="24ece-131">업데이트 및 재할당 문</span><span class="sxs-lookup"><span data-stu-id="24ece-131">Update-and-Reassign Statements</span></span>

<span data-ttu-id="24ece-132">오른쪽에 [복사 및 업데이트 식](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) 에 대 한 유사한 연결이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-132">A similar concatenation exists for [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) on the right-hand-side.</span></span>
<span data-ttu-id="24ece-133">마찬가지로, 사용자 정의 형식의 *명명 된 항목* 뿐만 아니라 *배열 항목*에 대해 *업데이트 및 재할당* 문이 존재 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-133">Correspondingly, *update-and-reassign* statements exist for *named items* in user-defined types as well as for *array items*.</span></span>  

```qsharp
newtype Complex = (Re : Double, Im : Double);

function ComplexSum(reals : Double[], ims : Double[]) : Complex[] {
    mutable res = Complex(0.,0.);

    for (r in reals) {
        set res w/= Re <- res::Re + r; // update-and-reassign statement
    }
    for (i in ims) {
        set res w/= Im <- res::Im + i; // update-and-reassign statement
    }
    return res;
}
```

<span data-ttu-id="24ece-134">배열의 경우 [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) 표준 라이브러리는 일반적인 배열 초기화 및 조작 요구에 필요한 도구를 제공 하므로 첫 번째 위치의 배열 항목을 업데이트 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-134">In the case of arrays, [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) in our standard libraries provides the necessary tools for many common array initialization and manipulation needs, and thus help avoid having to update array items in the first place.</span></span> 

<span data-ttu-id="24ece-135">필요에 따라 업데이트 및 재할당 문이 대안을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-135">Update-and-reassign statements provide an alternative if needed:</span></span>

```qsharp
operation GenerateRandomInts(max : Int, nSamples : Int) : Int[] {
    mutable samples = new Double[0];
    for (i in 1 .. nSamples) {
        set samples += [RandomInt(max)];
    }
    return samples;
}

operation SampleUniformDistrbution(nSamples : Int, nSteps : Int) : Double[] {
    let normalization = 1. / IntAsDouble(nSteps);
    mutable samples = GenerateRandomInts(nSteps, nSamples);
    
    for (i in IndexRange(samples) {
        let value = IntAsDouble(samples[i]);
        set samples w/= i <- normalization * value; // update-and-reassign statement
    }
}

```

<span data-ttu-id="24ece-136">예를 들어에서 제공 하는 배열에 대해 라이브러리 도구를 사용 하 여, 예를 들어, [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) Paulis의 인덱스는 `i` 지정 된 값을 사용 하 고 다른 모든 항목은 Id 인 paulis의 배열을 반환 하는 함수를 쉽게 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-136">Using the library tools for arrays provided in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays), we can, for example, easily define a function that returns an array of Paulis where the Pauli at index `i` takes the given value and all other entries are the identity.</span></span>

<span data-ttu-id="24ece-137">다음은 이러한 함수의 두 가지 정의 이며, 두 번째는 이러한 함수의 정의를 활용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-137">Here are two definitions of such a function, with the second taking advantage of the tools at our disposal.</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    mutable pauliArray = new Pauli[length];             // initialize pauliArray of given length
    for (index in 0 .. length - 1) {                    // iterate over the integers in the length range
        set pauliArray w/= index <-                     // change the value at index to input pauli or PauliI
            index == location ? pauli | PauliI;         // cond. expression evaluating to pauli or PauliI dep. on whether index==location
    }    
    return pauliArray;
}
```

<span data-ttu-id="24ece-138">배열의 각 인덱스를 반복 하 고 조건부로 설정 하는 대신 `PauliI` `Pauli` 에서를 사용 하 여의 `ConstantArray` [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) 배열을 만든 `PauliI` 다음 인덱스에서 특정 값을 변경 하는 복사 및 업데이트 식을 반환 하면 됩니다 `location` .</span><span class="sxs-lookup"><span data-stu-id="24ece-138">Instead of iterating over each index in the array, and conditionally setting it to `PauliI` or `Pauli`, we can instead use `ConstantArray` from [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) to create an array of `PauliI`'s, and then simply returning a copy-and-update expression in which we've changed the specifc value at index `location`:</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

## <a name="tuple-deconstruction"></a><span data-ttu-id="24ece-139">튜플 분해</span><span class="sxs-lookup"><span data-stu-id="24ece-139">Tuple Deconstruction</span></span>

<span data-ttu-id="24ece-140">단일 변수, 및---키워드를 할당 하는 것 외에 `let` `mutable` `set` 도 (아래 설명 참조)와 같은 다른 바인딩 구문을 사용 하 여 [튜플 형식의](xref:microsoft.quantum.guide.types#tuple-types)콘텐츠를 압축 풀기---수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-140">In addition to assigning a single variable, the `let` and `mutable` keywords---or in fact any other binding construct, such as `set` (described below)---also allow for unpacking the contents of a [tuple type](xref:microsoft.quantum.guide.types#tuple-types).</span></span>
<span data-ttu-id="24ece-141">이 폼의 할당은 해당 튜플의 요소를 *분해할* 하는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-141">An assignment of this form is said to *deconstruct* the elements of that tuple.</span></span>

<span data-ttu-id="24ece-142">바인딩의 오른쪽이 튜플이 면 할당 시 해당 튜플을 분해 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-142">If the right-hand side of the binding is a tuple, then that tuple may be deconstructed upon assignment.</span></span>
<span data-ttu-id="24ece-143">이러한 분해에는 중첩 된 튜플이 포함 될 수 있으며, 모든 전체 또는 부분 분해은 오른쪽에 있는 튜플의 모양이 기호 튜플의 셰이프와 호환 되는 한 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-143">Such deconstructions may involve nested tuples, and any full or partial deconstruction is valid as long as the shape of the tuple on the right hand side is compatible with the shape of the symbol tuple.</span></span>

<span data-ttu-id="24ece-144">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-144">For example:</span></span>

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

## <a name="binding-scopes"></a><span data-ttu-id="24ece-145">바인딩 범위</span><span class="sxs-lookup"><span data-stu-id="24ece-145">Binding Scopes</span></span>

<span data-ttu-id="24ece-146">일반적으로 기호 바인딩은 범위를 벗어난 것으로,에서 발생 하는 문 블록의 끝에서 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-146">In general, symbol bindings go out of scope and become inoperative at the end of the statement block they occur in.</span></span>
<span data-ttu-id="24ece-147">이 규칙에는 두 가지 예외가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-147">There are two exceptions to this rule:</span></span>

- <span data-ttu-id="24ece-148">루프의 루프 변수 바인딩은 `for` for 루프 본문의 범위 내에 있지만 루프가 끝난 후에는 범위 내에 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-148">The binding of the loop variable of a `for` loop is in scope for the body of the for loop, but not after the end of the loop.</span></span>
- <span data-ttu-id="24ece-149">루프의 세 부분 `repeat` / `until` (본문, 테스트 및 픽스업)은 모두 단일 범위로 처리 되므로 본문에 바인딩된 기호는 테스트 및 픽스업에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-149">All three portions of a `repeat`/`until` loop (the body, the test, and the fixup) are treated as a single scope, so symbols that are bound in the body are available in the test and in the fixup.</span></span>

<span data-ttu-id="24ece-150">두 가지 유형의 루프 모두 루프를 통과 하는 각은 자체 범위에서 실행 되므로 이전 패스의 바인딩은 이후 단계에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-150">For both types of loops, each pass through the loop executes in its own scope, so bindings from an earlier pass are not available in a later pass.</span></span>
<span data-ttu-id="24ece-151">이러한 루프에 대 한 자세한 내용은 [제어 흐름](xref:microsoft.quantum.guide.controlflow)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-151">Details on these loops can be found at [Control Flow](xref:microsoft.quantum.guide.controlflow).</span></span>

<span data-ttu-id="24ece-152">외부 블록의 기호 바인딩은 내부 블록에 의해 상속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-152">Symbol bindings from outer blocks are inherited by inner blocks.</span></span>
<span data-ttu-id="24ece-153">기호는 블록 당 한 번만 바인딩할 수 있습니다. 범위 내에 있는 다른 기호와 동일한 이름을 사용 하 여 기호를 정의할 수 없습니다 ("숨김" 없음).</span><span class="sxs-lookup"><span data-stu-id="24ece-153">A symbol may only be bound once per block; it is illegal to define a symbol with the same name as another symbol that is within scope (no "shadowing").</span></span>
<span data-ttu-id="24ece-154">다음 시퀀스는 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-154">The following sequences would be legal:</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

<span data-ttu-id="24ece-155">and</span><span class="sxs-lookup"><span data-stu-id="24ece-155">and</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
} else {
    ...
    let n = 8;
    ...             // n is 8
}
...                 // n is not bound to a value
```

<span data-ttu-id="24ece-156">그러나이는 올바르지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-156">But this would be illegal:</span></span>

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

<span data-ttu-id="24ece-157">다음과 같이 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-157">as would:</span></span>

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="next-steps"></a><span data-ttu-id="24ece-158">다음 단계</span><span class="sxs-lookup"><span data-stu-id="24ece-158">Next steps</span></span>

<span data-ttu-id="24ece-159">Q #의 이상 [비트 작업](xref:microsoft.quantum.guide.qubits) 에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="24ece-159">Learn about [Working With Qubits](xref:microsoft.quantum.guide.qubits) in Q#.</span></span>