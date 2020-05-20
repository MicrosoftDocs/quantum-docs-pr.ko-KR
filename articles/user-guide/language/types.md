---
title: Q#의 형식
description: 'Q # 프로그래밍 언어에 사용 되는 다양 한 형식에 대해 알아봅니다.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
ms.openlocfilehash: 4a551ee90a0abb6e42953cf04c7f5a8ca3573f26
ms.sourcegitcommit: 682a4a5f5dd23ca58a4addf62aea4086bb308552
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/19/2020
ms.locfileid: "83609144"
---
# <a name="types-in-q"></a><span data-ttu-id="eea72-103">Q#의 형식</span><span class="sxs-lookup"><span data-stu-id="eea72-103">Types in Q#</span></span>

<span data-ttu-id="eea72-104">이 페이지에서는 Q # 형식 모델을 지정 하 고 형식을 지정 하 고 작업 하는 구문을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-104">This page lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>
<span data-ttu-id="eea72-105">다음 페이지 [형식 식](xref:microsoft.quantum.guide.expressions)에서는 이러한 형식의 식을 만들고 작동 하는 방법에 대해 자세히 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-105">The next page, [Type Expressions](xref:microsoft.quantum.guide.expressions), details how to create and operate on expressions of these types.</span></span>

<span data-ttu-id="eea72-106">Q #은 *강력한* 형식의 언어 이므로 이러한 형식을 신중히 사용 하면 컴파일러가 컴파일 시간에 Q # 프로그램에 대 한 강력한 보증을 제공 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-106">We note that Q# is a *strongly-typed* language, such that careful use of these types can help the compiler to provide strong guarantees about Q# programs at compile time.</span></span>
<span data-ttu-id="eea72-107">가장 강력한 보증을 제공 하기 위해 해당 변환을 표현 하는 함수에 대 한 호출을 사용 하 여 Q #의 형식 간 변환이 명시적 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-107">In order to provide the strongest guarantees possible, conversions between types in Q# must be explicit using calls to functions which express that conversion.</span></span> <span data-ttu-id="eea72-108">이러한 여러 함수는 네임 스페이스의 일부로 제공 됩니다 <xref:microsoft.quantum.convert> .</span><span class="sxs-lookup"><span data-stu-id="eea72-108">A variety of such functions are provided as a part of the <xref:microsoft.quantum.convert> namespace.</span></span>
<span data-ttu-id="eea72-109">반면에 호환 되는 형식으로의 수동 캐스팅은 암시적으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-109">Upcasts to compatible types on the other hand happen implicitly.</span></span> 

<span data-ttu-id="eea72-110">Q #에서는 직접 사용할 수 있는 기본 형식과 다른 형식에서 새 형식을 생성 하는 다양 한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-110">Q# provides both primitive types, which can be used directly, and a variety of ways to produce new types from other types.</span></span>
<span data-ttu-id="eea72-111">여기서는이 섹션의 나머지 부분에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-111">We describe each in the rest of this section.</span></span>

## <a name="primitive-types"></a><span data-ttu-id="eea72-112">기본 유형</span><span class="sxs-lookup"><span data-stu-id="eea72-112">Primitive Types</span></span>

<span data-ttu-id="eea72-113">Q # 언어는 다른 형식을 구성할 수 있는 몇 가지 *기본 형식을*제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-113">The Q# language provides several *primitive types*, from which other types can be constructed:</span></span>

- <span data-ttu-id="eea72-114">`Int`형식은 64 비트 부호 있는 정수를 나타냅니다 (예: `2` ,,) `107` . `-5`</span><span class="sxs-lookup"><span data-stu-id="eea72-114">The `Int` type represents a 64-bit signed integer, e.g.: `2`, `107`, `-5`.</span></span>
- <span data-ttu-id="eea72-115">`BigInt`형식은 임의 크기의 부호 있는 정수를 나타냅니다 (예: `2L` ,,). `107L` `-5L`</span><span class="sxs-lookup"><span data-stu-id="eea72-115">The `BigInt` type represents a signed integer of arbitrary size, e.g. `2L`, `107L`, `-5L`.</span></span>
   <span data-ttu-id="eea72-116">이 형식은 .NET을 기반으로 합니다.<xref:System.Numerics.BigInteger></span><span class="sxs-lookup"><span data-stu-id="eea72-116">This type is based on the .NET <xref:System.Numerics.BigInteger></span></span>
   <span data-ttu-id="eea72-117">입력할.</span><span class="sxs-lookup"><span data-stu-id="eea72-117">type.</span></span>
- <span data-ttu-id="eea72-118">`Double`형식은 배정밀도 부동 소수점 숫자를 나타냅니다 (예: `0.0` , `-1.3` ,). `4e-7`</span><span class="sxs-lookup"><span data-stu-id="eea72-118">The `Double` type represents a double-precision floating-point number, e.g.: `0.0`, `-1.3`, `4e-7`.</span></span>
- <span data-ttu-id="eea72-119">`Bool`형식은 또는 일 수 있는 부울 값을 나타냅니다 `true` `false` .</span><span class="sxs-lookup"><span data-stu-id="eea72-119">The `Bool` type represents a Boolean value which can either be `true` or `false`.</span></span>
- <span data-ttu-id="eea72-120">`Range`형식은에 의해 표시 되는 정수 시퀀스를 나타냅니다 `start..step..stop` . 여기서 단계는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-120">The `Range` type represents a sequence of integers, denoted by `start..step..stop`, where denoting the step is optional.</span></span> 
   <span data-ttu-id="eea72-121">이는에 `start .. stop` 해당 하 `start..1..stop` 고, 예를 들어은 `1..2..7` $ \{ 1, 3, 5, 7 $ 시퀀스를 나타냅니다. \}</span><span class="sxs-lookup"><span data-stu-id="eea72-121">That is `start .. stop` corresponds to `start..1..stop`, and e.g. `1..2..7` represents the sequence $\{1, 3, 5, 7\}$.</span></span>
- <span data-ttu-id="eea72-122">`String`형식은 사용자가 만든 후 불투명 한 유니코드 문자 시퀀스입니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-122">The `String` type is a sequence of Unicode characters that is opaque to the user once created.</span></span>
  <span data-ttu-id="eea72-123">이 형식은 오류 또는 진단 이벤트의 경우 메시지를 기존 호스트에 보고 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-123">This type is used to report messages to a classical host in the case of an error or diagnostic event.</span></span>
- <span data-ttu-id="eea72-124">`Unit`형식은 하나의 값만 허용 하는 형식입니다 `()` .</span><span class="sxs-lookup"><span data-stu-id="eea72-124">The `Unit` type is the type that allows only one value `()`.</span></span> 
  <span data-ttu-id="eea72-125">이 형식은 Q # 함수 또는 연산이 정보를 반환 하지 않음을 나타내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-125">This type is used to indicate that Q# function or operation returns no information.</span></span> 
- <span data-ttu-id="eea72-126">`Qubit`형식은 퀀텀 비트 또는 비트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-126">The `Qubit` type represents a quantum bit or qubit.</span></span>
   <span data-ttu-id="eea72-127">`Qubit`는 사용자에 게 불투명 합니다. 다른 작업에 전달 하는 것 외에도 가능한 유일한 작업은 id (같음)를 테스트 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-127">`Qubit`s are opaque to the user; the only operation possible with them, other than passing them to another operation, is to test for identity (equality).</span></span>
   <span data-ttu-id="eea72-128">궁극적으로에 대 한 작업 `Qubit` 은 퀀텀 프로세서 (또는 시뮬레이션)에서 내장 명령을 호출 하 여 구현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-128">Ultimately, actions on `Qubit`s are implemented by calling intrinsic instructions on a quantum processor (or a simulation thereof).</span></span>
- <span data-ttu-id="eea72-129">`Pauli`형식은 4 개의 단일 기능 비트 Pauli 연산자 중 하나를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-129">The `Pauli` type represents one of the four single-qubit Pauli operators.</span></span>
   <span data-ttu-id="eea72-130">이 형식은 회전의 기본 연산을 나타내는 데 사용 되며 측정할 관찰 가능 개체를 지정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-130">This type is used to denote the base operation for rotations and to specify the observable being measured.</span></span>
   <span data-ttu-id="eea72-131">이는 네 가지 가능한 값 `PauliI` , 즉 `PauliX` `PauliY` 형식의 상수인,, 및를 `PauliZ` 포함 하는 열거형 형식입니다 `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="eea72-131">This is an enumerated type that has four possible values: `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, which are constants of type `Pauli`.</span></span>
- <span data-ttu-id="eea72-132">`Result`형식은 측정 결과를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-132">The `Result` type represents the result of a measurement.</span></span>
   <span data-ttu-id="eea72-133">이는 두 가지 가능한 값인 및 (형식의 상수인)를 사용 하는 열거형 형식입니다 `One` `Zero` `Result` .</span><span class="sxs-lookup"><span data-stu-id="eea72-133">This is an enumerated type with two possible values: `One` and `Zero`, which are constants of type `Result`.</span></span>
   <span data-ttu-id="eea72-134">`Zero`+ 1 eigenvalue를 측정 했음을 나타냅니다. `One`-1 eigenvalue를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-134">`Zero` indicates that the +1 eigenvalue was measured; `One` indicates the -1 eigenvalue.</span></span>

<span data-ttu-id="eea72-135">상수 `true` ,,,,,, `false` 및는 `PauliI` `PauliX` `PauliY` `PauliZ` `One` `Zero` Q #의 모든 예약 된 기호입니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-135">The constants `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`, and `Zero` are all reserved symbols in Q#.</span></span>

## <a name="array-types"></a><span data-ttu-id="eea72-136">배열 형식</span><span class="sxs-lookup"><span data-stu-id="eea72-136">Array Types</span></span>

<span data-ttu-id="eea72-137">유효한 Q # 형식이 지정 된 경우 `'T` 형식의 값 배열을 나타내는 형식이 있습니다 `'T` .</span><span class="sxs-lookup"><span data-stu-id="eea72-137">Given any valid Q# type `'T`, there is a type that represents an array of values of type `'T`.</span></span>
<span data-ttu-id="eea72-138">이 배열 형식은 ( `'T[]` 예: 또는)로 표현 `Qubit[]` 됩니다 `Int[][]` .</span><span class="sxs-lookup"><span data-stu-id="eea72-138">This array type is represented as `'T[]`; for example, `Qubit[]` or `Int[][]`.</span></span>
<span data-ttu-id="eea72-139">예를 들어, 정수 컬렉션은로 표시 되는 `Int[]` 반면 값 배열의 배열은로 표시 됩니다 `(Bool, Pauli)` `(Bool, Pauli)[][]` .</span><span class="sxs-lookup"><span data-stu-id="eea72-139">For instance, a collection of integers is denoted `Int[]`, while an array of arrays of `(Bool, Pauli)` values is denoted `(Bool, Pauli)[][]`.</span></span>

<span data-ttu-id="eea72-140">두 번째 예제에서이는 사각형 2 차원 배열이 아니라 잠재적으로 가변 배열 배열을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-140">In the second example, note that this represents a potentially jagged array of arrays, and not a rectangular two-dimensional array.</span></span>
<span data-ttu-id="eea72-141">Q #에서는 사각형 다차원 배열에 대 한 지원을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-141">Q# does not provide support for rectangular multi-dimensional arrays.</span></span>

<span data-ttu-id="eea72-142">에서와 같이 배열의 요소 주위에 대괄호를 사용 하 여 Q # 소스 코드에서 배열 값을 작성할 수 있습니다 `[PauliI, PauliX, PauliY, PauliZ]` .</span><span class="sxs-lookup"><span data-stu-id="eea72-142">An array value can be written in Q# source code by using square brackets around the elements of an array, as in `[PauliI, PauliX, PauliY, PauliZ]`.</span></span>
<span data-ttu-id="eea72-143">배열 리터럴의 형식은 배열의 모든 항목에 대 한 공통 기본 형식에 의해 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-143">The type of an array literal is determined by the common base type of all items in the array.</span></span> 

> [!WARNING]
> <span data-ttu-id="eea72-144">배열을 만든 후에는 배열의 요소를 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-144">The elements of an array cannot be changed after the array has been created.</span></span>
> <span data-ttu-id="eea72-145">[업데이트 및 재할당 문](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) 및/또는 [복사 및 업데이트 식은](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) 수정 된 배열을 생성 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-145">[Update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) and/or [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) can be used to construct a modified array.</span></span>

<span data-ttu-id="eea72-146">또는 키워드를 사용 하 여 크기에서 배열을 만들 수 있습니다 `new` .</span><span class="sxs-lookup"><span data-stu-id="eea72-146">Alternatively, an array can be created from its size using the `new` keyword:</span></span>

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

<span data-ttu-id="eea72-147">두 경우 모두 배열이 생성 된 후에는 핵심 함수를 `Length` 사용 하 여 요소 수를으로 가져올 수 있습니다 `Int` .</span><span class="sxs-lookup"><span data-stu-id="eea72-147">In either case, once an array has been constructed, the core function `Length` can be used to obtain the number of elements as an `Int`.</span></span>
<span data-ttu-id="eea72-148">배열에는 대괄호를 사용 하 여 첨자 (형식 또는 형식이 있는 첨자 포함)를 사용 하 여 `Int` `Range` 단일 요소나 배열 요소의 하위 집합을 포함 하는 새 배열을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-148">Arrays can be subscripted using square brackets, with subscripts either having type `Int` or type `Range`, to obtain either single elements or new arrays containing a subset of the elements of an array.</span></span>
<span data-ttu-id="eea72-149">배열의 첨자는 0부터 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-149">The subscripts of arrays are zero-based:</span></span>

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a><span data-ttu-id="eea72-150">튜플 형식</span><span class="sxs-lookup"><span data-stu-id="eea72-150">Tuple Types</span></span>

<span data-ttu-id="eea72-151">0 개 이상의 다른 형식, `T0` , ...,이 지정 된 경우 `T1` `Tn` 새 *튜플 형식을* 로 나타낼 수 있습니다 `(T0, T1, ..., Tn)` .</span><span class="sxs-lookup"><span data-stu-id="eea72-151">Given zero or more different types `T0`, `T1`, ..., `Tn`, we can denote a new  *tuple type* as `(T0, T1, ..., Tn)`.</span></span>
<span data-ttu-id="eea72-152">에서와 같이 새 튜플 형식을 생성 하는 데 사용 되는 형식은 튜플이 될 수 있습니다 `(Int, (Qubit, Qubit))` .</span><span class="sxs-lookup"><span data-stu-id="eea72-152">The types used to construct a new tuple type can themselves be tuples, as in `(Int, (Qubit, Qubit))`.</span></span>
<span data-ttu-id="eea72-153">그러나 이러한 중첩은 항상 유한 하지만 튜플 형식은 어떤 경우에도 자체적으로 포함 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-153">Such nesting is always finite, however, as tuple types cannot under any circumstances contain themselves.</span></span>

<span data-ttu-id="eea72-154">새 튜플 형식의 값은 튜플의 각 형식에서 값의 시퀀스로 구성 된 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-154">Values of the new tuple type are tuples formed by sequences of values from each type in the tuple.</span></span>
<span data-ttu-id="eea72-155">예를 들어 `(3, false)` 은 튜플 형식인 형식의 튜플입니다 `(Int, Bool)` .</span><span class="sxs-lookup"><span data-stu-id="eea72-155">For instance, `(3, false)` is a tuple whose type is the tuple type `(Int, Bool)`.</span></span>
<span data-ttu-id="eea72-156">튜플, 배열의 튜플, 하위 튜플 튜플 등의 배열을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-156">It is possible to create arrays of tuples, tuples of arrays, tuples of sub-tuples, etc.</span></span>

<span data-ttu-id="eea72-157">Q # 0.3를 사용 하 여 `Unit` 은 빈 튜플 *형식의* 이름입니다. `()` 은 빈 튜플 *값*에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-157">As of Q# 0.3, `Unit` is the name of the *type* of the empty tuple; `()` is used for the empty tuple *value*.</span></span>

<span data-ttu-id="eea72-158">튜플 인스턴스는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-158">Tuple instances are immutable.</span></span>
<span data-ttu-id="eea72-159">Q #에서는 생성 된 튜플의 콘텐츠를 변경 하는 메커니즘을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-159">Q# does not provide a mechanism to change the contents of a tuple once created.</span></span>

<span data-ttu-id="eea72-160">튜플은 값을 단일 값으로 수집 하 여 보다 쉽게 전달할 수 있도록 Q # 전체에서 사용 되는 강력한 개념입니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-160">Tuples are a powerful concept used throughout Q# to collect values together into a single value, making it easier to pass them around.</span></span>
<span data-ttu-id="eea72-161">특히 튜플 표기법을 사용 하면 모든 작업 및 호출 가능에서 정확히 하나의 입력을 사용 하 고 정확히 하나의 출력을 반환 하도록 표현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-161">In particular, using tuple notation, we can express that every operation and callable takes exactly one input and returns exactly one output.</span></span>

### <a name="singleton-tuple-equivalence"></a><span data-ttu-id="eea72-162">단일 튜플 동등성</span><span class="sxs-lookup"><span data-stu-id="eea72-162">Singleton Tuple Equivalence</span></span>

<span data-ttu-id="eea72-163">또는와 같은 singleton (단일 요소) 튜플을 만들 수 있습니다 `('T1)` `(5)` `([1,2,3])` .</span><span class="sxs-lookup"><span data-stu-id="eea72-163">It is possible to create a singleton (single-element) tuple, `('T1)`, such as `(5)` or `([1,2,3])`.</span></span>
<span data-ttu-id="eea72-164">그러나 Q #은 singleton 튜플을 포함 된 형식의 값과 완전히 동일 하 게 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-164">However, Q# treats a singleton tuple as completely equivalent to a value of the enclosed type.</span></span>
<span data-ttu-id="eea72-165">즉,과 사이에 차이가 없으며,과 사이에 차이가 없습니다 `5` `(5)` `5` `(((5)))` `(5, (6))` `(5, 6)` .</span><span class="sxs-lookup"><span data-stu-id="eea72-165">That is, there is no difference between `5` and `(5)`, or between `5` and `(((5)))`, or between `(5, (6))` and `(5, 6)`.</span></span>
<span data-ttu-id="eea72-166">쓰기를 위해 작성 하는 것은 올바르지만 `(5)+3` `5+3` 두 식이 모두로 계산 됩니다 `8` .</span><span class="sxs-lookup"><span data-stu-id="eea72-166">It is just as valid to write `(5)+3` as to write `5+3`, and both expressions will evaluate to `8`.</span></span>

<span data-ttu-id="eea72-167">이러한 동등성은 할당 및 식을 비롯 한 모든 용도에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-167">This equivalence applies for all purposes, including assignment and expressions.</span></span>
<span data-ttu-id="eea72-168">식이 지정 된 경우 괄호로 묶인 동일한 식이 동일한 형식의 식입니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-168">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="eea72-169">예를 들어,은 식 이며는 `(7)` `Int` `([1,2,3])` s 형식의 식이고는 `Int` `((1,2))` 형식이 인 식입니다 `(Int, Int)` .</span><span class="sxs-lookup"><span data-stu-id="eea72-169">For instance, `(7)` is an `Int` expression, `([1,2,3])` is an expression of type array of `Int`s, and `((1,2))` is an expression with type `(Int, Int)`.</span></span>

<span data-ttu-id="eea72-170">특히이는 입력 튜플 또는 출력 튜플 형식이 하나의 필드를 갖는 작업 또는 함수가 단일 인수를 사용 하거나 단일 값을 반환 하는 것으로 간주할 수 있음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-170">In particular, this means that an operation or function whose input tuple or output tuple type has one field can be thought of as taking a single argument or returning a single value.</span></span>

<span data-ttu-id="eea72-171">이 속성은 _단일 튜플 동치_로 참조 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-171">We refer to this property as _singleton tuple equivalence_.</span></span>


## <a name="user-defined-types"></a><span data-ttu-id="eea72-172">사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="eea72-172">User-Defined Types</span></span>

<span data-ttu-id="eea72-173">사용자 정의 형식 선언은 키워드로 구성 된 `newtype` 다음 사용자 정의 형식 이름, `=` , 유효한 형식 사양 및 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-173">A user-defined type declaration consists of the keyword `newtype`, followed by the name of the user-defined type, an `=`, a valid type specification, and a terminating semicolon.</span></span>

<span data-ttu-id="eea72-174">다음은 그 예입니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-174">For example:</span></span>

```qsharp
newtype PairOfInts = (Int, Int);
```

<span data-ttu-id="eea72-175">각 Q # 소스 파일은 원하는 수의 사용자 정의 형식을 선언할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-175">Each Q# source file may declare any number of user-defined types.</span></span>
<span data-ttu-id="eea72-176">형식 이름은 네임 스페이스 내에서 고유 해야 하며 작업 및 함수 이름과 충돌 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-176">Type names must be unique within a namespace and may not conflict with operation and function names.</span></span>

<span data-ttu-id="eea72-177">사용자 정의 형식은 기본 형식이 동일한 경우에도 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-177">User-defined types are distinct even if the base types are identical.</span></span>
<span data-ttu-id="eea72-178">특히 기본 형식이 동일한 경우에도 두 사용자 정의 형식의 값 사이에 자동 변환이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-178">In particular, there is no automatic conversion between values of two user-defined types even if the underlying types are identical.</span></span>

### <a name="named-vs-anonymous-items"></a><span data-ttu-id="eea72-179">명명 된 항목과 익명 항목 비교</span><span class="sxs-lookup"><span data-stu-id="eea72-179">Named vs. anonymous items</span></span>

<span data-ttu-id="eea72-180">Q # 파일은 법적 형식의 단일 값을 포함 하는 새 명명 된 형식을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-180">A Q# file may define a new named type containing a single value of any legal type.</span></span>
<span data-ttu-id="eea72-181">모든 튜플 형식의 경우 `T` 문을 사용 하 여의 하위 형식인 새 사용자 정의 형식을 선언할 수 있습니다 `T` `newtype` .</span><span class="sxs-lookup"><span data-stu-id="eea72-181">For any tuple type `T`, we can declare a new user-defined type that is a subtype of `T` with the `newtype` statement.</span></span>
<span data-ttu-id="eea72-182">예를 @"microsoft.quantum.math" 들어 네임 스페이스에서 복소수는 사용자 정의 형식으로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-182">In the @"microsoft.quantum.math" namespace, for instance, complex numbers are defined as a user-defined type:</span></span>

```qsharp
newtype Complex = (Double, Double);
```
<span data-ttu-id="eea72-183">이 문은 형식의 익명 항목 두 개를 사용 하 여 새 형식을 만듭니다 `Double` .</span><span class="sxs-lookup"><span data-stu-id="eea72-183">This statement creates a new type with two anonymous items of type `Double`.</span></span>   

<span data-ttu-id="eea72-184">익명 항목 외에도 사용자 정의 형식은 Q # 버전 0.7 이상으로 *명명 된 항목* 을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-184">Aside from anonymous items, user-defined types also support *named items* as of Q# version 0.7 or higher.</span></span> <span data-ttu-id="eea72-185">예를 들어 `Re` 복소수의 실수 부분과 허수 부분을 나타내는 double의 이름을 to 항목으로 지정할 수 있습니다 `Im` .</span><span class="sxs-lookup"><span data-stu-id="eea72-185">For example, we could have named the to items `Re` for the double representing the real part of a complex number and `Im` for the imaginary part:</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="eea72-186">사용자 정의 형식에서 한 항목의 이름을 지정 하는 것은 모든 항목의 이름을 지정 해야 한다는 의미는 아닙니다. 명명 된 항목 및 명명 되지 않은 항목의 모든 조합이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-186">Naming one item in a user-defined type does not imply that all items need to be named - any combination of named and unnamed items is supported.</span></span> <span data-ttu-id="eea72-187">또한 내부 항목의 이름을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-187">Furthermore, inner items may also be named.</span></span>
<span data-ttu-id="eea72-188">`Nested`예를 들어 아래에 정의 된 형식에는 기본 형식이 있으며 `(Double, (Int, String))` ,이 형식은 형식의 항목에만 `Int` 이름이 지정 되 고 다른 모든 항목은 익명입니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-188">The type `Nested` as defined below for example has an underlying type `(Double, (Int, String))`, of which only the item of type `Int` is named and all other items are anonymous.</span></span> 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

<span data-ttu-id="eea72-189">명명 된 항목은 *액세스 연산자* 를 통해 직접 액세스할 수 있다는 장점이 있습니다 `::` .</span><span class="sxs-lookup"><span data-stu-id="eea72-189">Named items have the advantage that they can be accessed directly via the *access operator* `::`.</span></span> 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

<span data-ttu-id="eea72-190">잠재적으로 복잡 한 튜플 형식에 대 한 짧은 별칭을 제공 하는 것 외에도 이러한 형식을 정의 하면 특정 값의 의도를 문서화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-190">In addition to providing short aliases for potentially complicated tuple types, one significant advantage of defining such types is that they can document the intent of a particular value.</span></span>
<span data-ttu-id="eea72-191">의 예제로 돌아가면 `Complex` 2d 극좌표 형 좌표를 사용자 정의 형식으로 정의 했을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-191">Returning to the example of `Complex`, one could have also defined 2D polar coordinates as a user-defined type:</span></span>

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

<span data-ttu-id="eea72-192">및 둘 다 `Complex` 에 `Polar` 기본 형식이 있는 경우에도 `(Double, Double)` 두 형식이 모두 Q #에서 완전히 호환 되지 않으므로 극좌표를 사용 하 여 복잡 한 수학 함수를 실수로 호출 하는 위험을 최소화 하 고 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-192">Even though both `Complex` and `Polar` are both have an underlying type `(Double, Double)`, the two types are wholly incompatible in Q#, minimizing the risk of accidentally calling a complex math function with polar coordinates and vice versa.</span></span>
<span data-ttu-id="eea72-193">이러한 방식으로 사용자 정의 형식은 F #의 레코드와 비슷한 역할을 합니다 (예:).</span><span class="sxs-lookup"><span data-stu-id="eea72-193">In this way, user-defined types have a similar role as Records in F# for example.</span></span> 


#### <a name="access-anonymous-items-with-the-unwrap-operator"></a><span data-ttu-id="eea72-194">래핑 해제 연산자를 사용 하 여 익명 항목 액세스</span><span class="sxs-lookup"><span data-stu-id="eea72-194">Access anonymous items with the unwrap operator</span></span>

<span data-ttu-id="eea72-195">반면에 익명 항목에 액세스 하려면 후 위 연산자를 사용 하 여 래핑된 값을 먼저 추출 해야 합니다 `!` .</span><span class="sxs-lookup"><span data-stu-id="eea72-195">In order to access anonymous items on the other hand, the wrapped value first needs to be extracted using the postfix operator `!`.</span></span>
<span data-ttu-id="eea72-196">"래핑 해제" 연산자를 `!` 사용 하 여 사용자 정의 형식에 포함 된 값을 추출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-196">The "unwrap" operator, `!`, allows to extract the value contained in a user-defined type.</span></span>
<span data-ttu-id="eea72-197">이러한 "래핑 해제" 식의 형식은 사용자 정의 형식의 기본 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-197">The type of such an "unwrap" expression is the underlying type of the user-defined type.</span></span> 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

<span data-ttu-id="eea72-198">래핑 해제 연산자는 정확히 한 줄의의 래핑을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-198">The unwrap operator unwraps exactly one layer of wrapping.</span></span>
<span data-ttu-id="eea72-199">여러 래핑 연산자를 사용 하 여 곱하기 래핑된 값에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-199">Multiple unwrap operators may be used to access a multiply-wrapped value.</span></span>

<span data-ttu-id="eea72-200">예:</span><span class="sxs-lookup"><span data-stu-id="eea72-200">For instance:</span></span>

```qsharp
newtype WrappedInt = Int;
newtype DoublyWrappedInt = WrappedInt;

...
    let x = DoublyWrappedInt(WrappedInt(6));
    let y = x!;       // y is WrappedInt(6)
    let z = x!!;      // z is 6
    let a = x + 5;    // This is an error, a DoublyWrappedInt isn't an Int
    let b = x! + 5;   // Also an error
    let c = x!! + 5;  // This is valid, c will be 11
...
```

<span data-ttu-id="eea72-201">래핑 해제 연산자에 대 한 자세한 내용은 [Q #의 형식 식](xref:microsoft.quantum.guide.expressions)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-201">More details on the unwrap operator can be found at [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions).</span></span>

### <a name="creating-values-of-user-defined-types"></a><span data-ttu-id="eea72-202">사용자 정의 형식 값 만들기</span><span class="sxs-lookup"><span data-stu-id="eea72-202">Creating values of user-defined types</span></span>

<span data-ttu-id="eea72-203">사용자 정의 형식의 값은 해당 형식 생성자를 호출 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-203">Values of a user-defined type can be created by calling the corresponding type constructor:</span></span>

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

<span data-ttu-id="eea72-204">또는 [복사 및 업데이트 식을](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions)사용 하 여 기존 값에서 새 값을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-204">Alternatively, new values can be created from existing ones using [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span> <span data-ttu-id="eea72-205">배열의 경우와 같이 이러한 식은 지정 된 명명 된 항목을 제외 하 고 원래 식의 모든 항목 값을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-205">Like for arrays, such expressions copy all item values of the original expression, with the exception of the specified named items.</span></span> <span data-ttu-id="eea72-206">이러한 값은 식의 오른쪽에 정의 된 값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-206">For these the values are set to the ones defined on the right hand side of the expression.</span></span> <span data-ttu-id="eea72-207">예를 들어 [업데이트 및 재할당 문과](xref:microsoft.quantum.guide.variables#update-and-reassign-statements)같이 배열 항목에 사용할 수 있는 다른 모든 언어 구문은 사용자 정의 형식의 명명 된 항목에도 존재 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-207">Any other language constructs, like for example [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), that are available for array items exist for named-items in user-defined types as well.</span></span>

```qsharp
newtype ComplexArray = (Count : Int, Data : Complex[]);

function AsComplexArray (data : Double[]) : ComplexArray {

    mutable res = ComplexArray(0, new Complex[0]);
    for (item in data) {
        set res w/= Data <- res::Data + [Complex(item, 0.)]; // update-and-reassign statement
    }
    return res w/ Count <- Length(res::Data); // returning a copy-and-update expression
}
```

<span data-ttu-id="eea72-208">사용자 정의 형식은 다른 모든 형식을 사용할 수 있는 모든 위치에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-208">User-defined types may be used anywhere any other type may be used.</span></span>
<span data-ttu-id="eea72-209">특히 사용자 정의 형식의 배열을 정의 하 고 사용자 정의 형식을 튜플 형식의 요소로 포함 하는 것이 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-209">In particular, it is possible to define an array of a user-defined type and to include a user-defined type as an element of a tuple type.</span></span>

<span data-ttu-id="eea72-210">참고로 재귀 형식 구조를 만들 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-210">Note is not possible to create recursive type structures.</span></span>
<span data-ttu-id="eea72-211">즉, 사용자 정의 형식을 정의 하는 형식은 사용자 정의 형식의 요소를 포함 하는 튜플 형식이 아닐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-211">That is, the type that defines a user-defined type may not be a tuple type that includes an element of the user-defined type.</span></span>
<span data-ttu-id="eea72-212">보다 일반적으로 사용자 정의 형식에는 순환 종속성이 있을 수 없으므로 다음과 같은 형식 정의 집합이 잘못 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-212">More generally, user-defined types may not have cyclic dependencies on each other, so the following set of type definitions would be illegal:</span></span>

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```


## <a name="operation-and-function-types"></a><span data-ttu-id="eea72-213">작업 및 함수 형식</span><span class="sxs-lookup"><span data-stu-id="eea72-213">Operation and Function Types</span></span>

<span data-ttu-id="eea72-214">호출할 수 있는 기본 형식은 또는로 작성 됩니다 `('Tinput => 'Tresult)` `('Tinput -> 'Tresult)` `'Tinput` . 여기서 및 `'Tresult` 는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-214">The basic type for any callable is written as `('Tinput => 'Tresult)` or `('Tinput -> 'Tresult)`, where both `'Tinput` and `'Tresult` are types.</span></span>
<span data-ttu-id="eea72-215">이를 호출 가능의 *서명* 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-215">These are called the *signature* of the callable.</span></span>

<span data-ttu-id="eea72-216">모든 Q # callables은 단일 값을 입력으로 사용 하 고 단일 값을 출력으로 반환 하는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-216">All Q# callables are considered to take a single value as input and return a single value as output.</span></span>
<span data-ttu-id="eea72-217">입력 값과 출력 값 모두 튜플이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-217">Both the input and output values may be tuples.</span></span>
<span data-ttu-id="eea72-218">결과가 반환 되지 않는 callables `Unit` 입니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-218">Callables that have no result return `Unit`.</span></span>
<span data-ttu-id="eea72-219">입력이 없는 callables은 빈 튜플을 입력으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-219">Callables that have no input take the empty tuple as input.</span></span>

> [!NOTE]
> <span data-ttu-id="eea72-220">를 사용 하는 첫 번째 폼은 `=>` 작업에 사용 되 고 두 번째 폼은 함수에 사용 됩니다 `->` .</span><span class="sxs-lookup"><span data-stu-id="eea72-220">The first form, with `=>`, is used for operations; the second form, with `->`, for functions.</span></span>
> <span data-ttu-id="eea72-221">예를 들어는 `((Qubit, Pauli) => Result)` 가능한 단일 수준 비트 측정 작업의 시그니처를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-221">For example, `((Qubit, Pauli) => Result)` represents the signature for a possible single-qubit measurement operation.</span></span>
<span data-ttu-id="eea72-222">*함수* 형식은 해당 시그니처로 완전히 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-222">*Function* types are completely specified by their signature.</span></span>
<span data-ttu-id="eea72-223">예를 들어, 각도의 사인을 계산 하는 함수는 형식을 갖습니다 `(Double -> Double)` .</span><span class="sxs-lookup"><span data-stu-id="eea72-223">For example, a function that computes the sine of an angle would have type `(Double -> Double)`.</span></span>

<span data-ttu-id="eea72-224">*작업---있지만*함수는 작업 유형의 일부로 표시 되는 특정 추가 특성을 포함---.</span><span class="sxs-lookup"><span data-stu-id="eea72-224">*Operations*---but not functions---have certain additional characteristics that are expressed as part of the operation type.</span></span> <span data-ttu-id="eea72-225">이러한 특성에는 작업에서 지 원하는 *함수* 에 대 한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-225">Such characteristics include information about what *functors* the operation supports.</span></span>
<span data-ttu-id="eea72-226">예를 들어 다른 조건 화 된의 상태에서 작업 실행을 사용할 수 있는 경우 함수를 지원 해야 합니다 `Controlled` . 작업에 역이 있으면 함수를 지원 해야 합니다 `Adjoint` .</span><span class="sxs-lookup"><span data-stu-id="eea72-226">For example, if execution of the operation can be conditioned on the state of other qubits, it should support the `Controlled` functor; if the operation has an inverse, it should support the `Adjoint` functor.</span></span> <span data-ttu-id="eea72-227">함수 및 작업에 대 한 자세한 내용은 [Q #의 작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions)를 참조 하세요. 여기서는 작업 서명을 변경 하는 방법에 대해서만 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-227">Functors and operations are discussed in detail at [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions), but here we simply discuss how this alters the operation signature.</span></span>

<span data-ttu-id="eea72-228">`Controlled`작업 형식에서 and/or 함수를 지원 하려면 `Adjoint` 해당 특성을 나타내는 주석을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-228">In order to require support for the `Controlled` and/or `Adjoint` functor in an operation type, we need to add an annotation indicating the corresponding characteristics.</span></span>
<span data-ttu-id="eea72-229">주석 `is Ctl` (예:)은 작업을---제어할 수 있음을 나타냅니다. 즉 `(Qubit => Unit is Ctl)` , 다른 조건 화 된의 상태에 따라 실행이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-229">An annotation `is Ctl` (e.g. `(Qubit => Unit is Ctl)`) indicates that the operation is controllable---that is, it's execution conditioned on the state of another qubit or qubits.</span></span> <span data-ttu-id="eea72-230">마찬가지로, `is Adj` 작업에 adjoint가 있거나 단순히 작업을 연속적으로 적용 하 고 해당 adjoint를 상태에서 상태로 유지 하는 "반전"이 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-230">Similarly, `is Adj` indicates that the operation has an adjoint; or simply, it can be "inverted" such that successively applying an operation and then its adjoint to a state leaves the state unchanged.</span></span> 

<span data-ttu-id="eea72-231">해당 형식의 작업에서 및 함수를 둘 다 지원 하도록 요구 하려는 경우 `Adjoint` `Controlled` 이를로 표현할 수 있습니다 `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="eea72-231">If we want to require that an operation of that type supports both the `Adjoint` and `Controlled` functor we can express this as `(Qubit => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="eea72-232">예를 들어 기본 제공 Pauli 작업에는 <xref:microsoft.quantum.intrinsic.x> 형식이 `(Qubit => Unit is Adj + Ctl)` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-232">For example, the built-in Pauli <xref:microsoft.quantum.intrinsic.x> operation has type `(Qubit => Unit is Adj + Ctl)`.</span></span> 

<span data-ttu-id="eea72-233">함수을 지원 하지 않는 작업 형식은 입력 및 출력 형식 만으로 지정 되 고 추가 주석은 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-233">An operation type that does not support any functors is specified by its input and output type alone, with no additional annotation.</span></span>

### <a name="type-parameterized-functions-and-operations"></a><span data-ttu-id="eea72-234">형식 매개 변수화 된 함수 및 작업</span><span class="sxs-lookup"><span data-stu-id="eea72-234">Type-Parameterized Functions and Operations</span></span>

<span data-ttu-id="eea72-235">호출 가능 형식에는 형식 매개 변수가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-235">Callable types may contain type parameters.</span></span>
<span data-ttu-id="eea72-236">형식 매개 변수는 작은따옴표가 접두사로 붙는 기호로 표시 됩니다. 예를 들어 `'A` 은 올바른 형식 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-236">Type parameters are indicated by a symbol prefixed by a single quote; for example, `'A` is a legal type parameter.</span></span>
<span data-ttu-id="eea72-237">형식 매개 변수가 있는 callables을 정의 하는 방법에 대 한 자세한 내용은 [Q # 페이지의 작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) 에 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-237">Details on defining type-parameterized callables are provided on the [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) page.</span></span>

<span data-ttu-id="eea72-238">단일 서명에서 형식 매개 변수가 두 번 이상 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-238">A type parameter may appear more than once in a single signature.</span></span>
<span data-ttu-id="eea72-239">예를 들어, 배열의 각 요소에 다른 함수를 적용 하 고 수집 된 결과를 반환 하는 함수는 시그니처를 가집니다 `(('A[], 'A->'A) -> 'A[])` .</span><span class="sxs-lookup"><span data-stu-id="eea72-239">For example, a function that applies another function to each element of an array and returns the collected results would have signature `(('A[], 'A->'A) -> 'A[])`.</span></span>
<span data-ttu-id="eea72-240">마찬가지로 두 작업의 컴퍼지션을 반환 하는 함수에는 서명이 있을 수 있습니다 `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .</span><span class="sxs-lookup"><span data-stu-id="eea72-240">Similarly, a function that returns the composition of two operations might have signature `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span></span>

<span data-ttu-id="eea72-241">형식이 매개 변수가 있는 호출 가능 매개 변수를 호출 하는 경우 동일한 형식 매개 변수를 갖는 모든 인수는 동일한 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-241">When invoking a type-parameterized callable, all arguments that have the same type parameter must be of the same type.</span></span>

<span data-ttu-id="eea72-242">Q #에서는 형식 매개 변수를 대체할 수 있는 가능한 형식을 제한 하는 메커니즘을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-242">Q# does not provide a mechanism for constraining the possible types that might be substituted for a type parameter.</span></span>

## <a name="whats-next"></a><span data-ttu-id="eea72-243">다음 단계</span><span class="sxs-lookup"><span data-stu-id="eea72-243">What's Next?</span></span>
<span data-ttu-id="eea72-244">Q # 언어를 구성 하는 모든 형식을 살펴보았으므로 이제 [q #의 형식 식](xref:microsoft.quantum.guide.expressions) 으로 이동 하 여 이러한 다양 한 형식의 식을 만들고 조작 하는 방법을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea72-244">Now that you've seen all the types which comprise the Q# language, you can head to [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions) to see how to create and manipulate expressions of these various types.</span></span>


