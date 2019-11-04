---
title: 'Q # 형식 모델 | Microsoft Docs'
description: 'Q # 형식 모델'
author: QuantumWriter
uid: microsoft.quantum.language.type-model
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4e251053d1b8306bf8956314d8099e95c56bce55
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2019
ms.locfileid: "73184749"
---
# <a name="the-type-model"></a><span data-ttu-id="87275-103">형식 모델</span><span class="sxs-lookup"><span data-stu-id="87275-103">The Type Model</span></span>

<span data-ttu-id="87275-104">이 섹션에서는 Q # 형식 모델을 설명 하 고 형식을 지정 하 고 사용 하는 구문을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-104">This section lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>
<span data-ttu-id="87275-105">Q #은 *강력한* 형식의 언어 이므로 이러한 형식을 신중히 사용 하면 컴파일러가 컴파일 시간에 Q # 프로그램에 대 한 강력한 보증을 제공 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-105">We note that Q# is a *strongly-typed* language, such that careful use of these types can help the compiler to provide strong guarantees about Q# programs at compile time.</span></span>

<span data-ttu-id="87275-106">가장 강력한 보증을 제공 하기 위해 해당 변환을 표현 하는 함수에 대 한 호출을 사용 하 여 Q #의 형식 간 변환이 명시적 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-106">In order to provide the strongest guarantees possible, conversions between types in Q# must be explicit using calls to functions which express that conversion.</span></span> <span data-ttu-id="87275-107">이러한 여러 함수는 <xref:microsoft.quantum.convert> 네임 스페이스의 일부로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-107">A variety of such functions are provided as a part of the <xref:microsoft.quantum.convert> namespace.</span></span>
<span data-ttu-id="87275-108">반면에 호환 되는 형식으로의 수동 캐스팅은 암시적으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-108">Upcasts to compatible types on the other hand happen implicitly.</span></span> 

<span data-ttu-id="87275-109">Q #에서는 직접 사용할 수 있는 기본 형식과 다른 형식에서 새 형식을 생성 하는 다양 한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-109">Q# provides both primitive types, which can be used directly, and a variety of ways to produce new types from other types.</span></span>
<span data-ttu-id="87275-110">여기서는이 섹션의 나머지 부분에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-110">We describe each in the rest of this section.</span></span>

## <a name="primitive-types"></a><span data-ttu-id="87275-111">기본 유형</span><span class="sxs-lookup"><span data-stu-id="87275-111">Primitive Types</span></span>

<span data-ttu-id="87275-112">Q # 언어는 다른 형식을 구성할 수 있는 몇 가지 *기본 형식을*제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-112">The Q# language provides several *primitive types*, from which other types can be constructed:</span></span>

- <span data-ttu-id="87275-113">`Int` 형식은 64 비트 부호 있는 정수를 나타냅니다 (예: `2`, `107`, `-5`).</span><span class="sxs-lookup"><span data-stu-id="87275-113">The `Int` type represents a 64-bit signed integer, e.g.: `2`, `107`, `-5`.</span></span>
- <span data-ttu-id="87275-114">`BigInt` 형식은 임의 크기의 부호 있는 정수 (예: `2L`, `107L`, `-5L`)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87275-114">The `BigInt` type represents a signed integer of arbitrary size, e.g. `2L`, `107L`, `-5L`.</span></span>
   <span data-ttu-id="87275-115">이 형식은 .NET <xref:System.Numerics.BigInteger>을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-115">This type is based on the .NET <xref:System.Numerics.BigInteger></span></span>
   <span data-ttu-id="87275-116">입력할.</span><span class="sxs-lookup"><span data-stu-id="87275-116">type.</span></span>
- <span data-ttu-id="87275-117">`Double` 형식은 배정밀도 부동 소수점 숫자를 나타냅니다 (예: `0.0`, `-1.3`, `4e-7`).</span><span class="sxs-lookup"><span data-stu-id="87275-117">The `Double` type represents a double-precision floating-point number, e.g.: `0.0`, `-1.3`, `4e-7`.</span></span>
- <span data-ttu-id="87275-118">`Bool` 형식은 `true` 하거나 `false`수 있는 부울 값을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87275-118">The `Bool` type represents a Boolean value which can either be `true` or `false`.</span></span>
- <span data-ttu-id="87275-119">`Qubit` 형식은 퀀텀 비트 또는 비트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87275-119">The `Qubit` type represents a quantum bit or qubit.</span></span>
   <span data-ttu-id="87275-120">`Qubit`은 사용자에 게 불투명 합니다. 다른 작업에 전달 하는 것 외에도 가능한 유일한 작업은 id (같음)를 테스트 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-120">`Qubit`s are opaque to the user; the only operation possible with them, other than passing them to another operation, is to test for identity (equality).</span></span>
   <span data-ttu-id="87275-121">궁극적으로 `Qubit`s에 대 한 작업은 퀀텀 프로세서 또는 시뮬레이션에 대 한 기본 지침을 호출 하 여 구현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-121">Ultimately, actions on `Qubit`s are implemented by calling intrinsic instructions on a quantum processor (or a simulation thereof).</span></span>
- <span data-ttu-id="87275-122">`Pauli` 형식은 4 개의 단일 기능 비트 Pauli 연산자 중 하나를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87275-122">The `Pauli` type represents one of the four single-qubit Pauli operators.</span></span>
   <span data-ttu-id="87275-123">이 형식은 회전의 기본 연산을 나타내는 데 사용 되며 측정할 관찰 가능 개체를 지정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-123">This type is used to denote the base operation for rotations and to specify the observable being measured.</span></span>
   <span data-ttu-id="87275-124">이는 `PauliI`, `PauliX`, `PauliY`및 `PauliZ`의 네 가지 가능한 값이 있는 열거 형식으로, `Pauli`형식의 상수입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-124">This is an enumerated type that has four possible values: `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, which are constants of type `Pauli`.</span></span>
- <span data-ttu-id="87275-125">`Result` 형식은 측정 결과를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87275-125">The `Result` type represents the result of a measurement.</span></span>
   <span data-ttu-id="87275-126">이는 두 가지 가능한 값인 `One`와 `Zero``Result`형식의 상수인 열거형 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-126">This is an enumerated type with two possible values: `One` and `Zero`, which are constants of type `Result`.</span></span>
   <span data-ttu-id="87275-127">`Zero` + 1 eigenvalue를 측정 했음을 나타냅니다. `One`-1 eigenvalue를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87275-127">`Zero` indicates that the +1 eigenvalue was measured; `One` indicates the -1 eigenvalue.</span></span>
- <span data-ttu-id="87275-128">`Range` 형식은 `start..step..stop`으로 표시 되는 정수 시퀀스를 나타냅니다. 여기서 단계는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-128">The `Range` type represents a sequence of integers, denoted by `start..step..stop`, where denoting the step is options.</span></span> 
   <span data-ttu-id="87275-129">이는 `start .. stop` `start..1..stop`에 해당 하며, 예를 들어 `1..2..7` $\{1, 3, 5, 7\}$ 시퀀스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87275-129">That is `start .. stop` corresponds to `start..1..stop`, and e.g. `1..2..7` represents the sequence $\{1, 3, 5, 7\}$.</span></span>
- <span data-ttu-id="87275-130">`String` 형식은 사용자가 만든 후 불투명 한 유니코드 문자 시퀀스입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-130">The `String` type is a sequence of Unicode characters that is opaque to the user once created.</span></span>
  <span data-ttu-id="87275-131">이 형식은 오류 또는 진단 이벤트의 경우 메시지를 기존 호스트에 보고 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-131">This type is used to report messages to a classical host in the case of an error or diagnostic event.</span></span>
- <span data-ttu-id="87275-132">`Unit` 형식은 하나의 값 `()`허용 하는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-132">The `Unit` type is the type that allows only one value `()`.</span></span> 
  <span data-ttu-id="87275-133">이 형식은 Q # 함수 또는 연산이 정보를 반환 하지 않음을 나타내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-133">This type is used to indicate that Q# function or operation returns no information.</span></span> 

<span data-ttu-id="87275-134">`true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`및 `Zero` 상수는 Q #에서 모든 예약 된 기호입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-134">The constants `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`, and `Zero` are all reserved symbols in Q#.</span></span>

## <a name="array-types"></a><span data-ttu-id="87275-135">배열 형식</span><span class="sxs-lookup"><span data-stu-id="87275-135">Array Types</span></span>

<span data-ttu-id="87275-136">유효한 Q # 형식 `'T`지정 된 경우 `'T`형식의 값 배열을 나타내는 형식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-136">Given any valid Q# type `'T`, there is a type that represents an array of values of type `'T`.</span></span>
<span data-ttu-id="87275-137">이 배열 형식은 `'T[]`으로 표시 됩니다. 예를 들어 `Qubit[]` 또는 `Int[][]`입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-137">This array type is represented as `'T[]`; for example, `Qubit[]` or `Int[][]`.</span></span>
<span data-ttu-id="87275-138">예를 들어, 정수 컬렉션은 `Int[]`로 표시 되 고, `(Bool, Pauli)` 값 배열의 배열은 `(Bool, Pauli)[][]`로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-138">For instance, a collection of integers is denoted `Int[]`, while an array of arrays of `(Bool, Pauli)` values is denoted `(Bool, Pauli)[][]`.</span></span>

<span data-ttu-id="87275-139">두 번째 예제에서이는 사각형 2 차원 배열이 아니라 잠재적으로 가변 배열 배열을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87275-139">In the second example, note that this represents a potentially jagged array of arrays, and not a rectangular two-dimensional array.</span></span>
<span data-ttu-id="87275-140">Q #에서는 사각형 다차원 배열에 대 한 지원을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-140">Q# does not provide support for rectangular multi-dimensional arrays.</span></span>

<span data-ttu-id="87275-141">`[PauliI, PauliX, PauliY, PauliZ]`와 같이 배열의 요소 주위에 대괄호를 사용 하 여 Q # 소스 코드에서 배열 값을 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-141">An array value can be written in Q# source code by using square brackets around the elements of an array, as in `[PauliI, PauliX, PauliY, PauliZ]`.</span></span>
<span data-ttu-id="87275-142">배열 리터럴의 형식은 배열의 모든 항목에 대 한 공통 기본 형식에 의해 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-142">The type of an array literal is determined by the common base type of all items in the array.</span></span> 

> [!WARNING]
> <span data-ttu-id="87275-143">배열을 만든 후에는 배열의 요소를 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-143">The elements of an array cannot be changed after the array has been created.</span></span>
> <span data-ttu-id="87275-144">업데이트 및 재할당 문 및/또는 복사 및 업데이트 식은 수정 된 배열을 생성 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-144">Update-and-reassign statements and/or copy-and-update expressions can be used to construct a modified array.</span></span>

<span data-ttu-id="87275-145">또는 `new` 키워드를 사용 하 여 크기에서 배열을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-145">Alternatively, an array can be created from its size using the `new` keyword:</span></span>

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

<span data-ttu-id="87275-146">두 경우 모두 배열이 생성 된 후에는 핵심 함수 `Length`를 사용 하 여 요소 수를 `Int`으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-146">In either case, once an array has been constructed, the core function `Length` can be used to obtain the number of elements as an `Int`.</span></span>
<span data-ttu-id="87275-147">배열에는 대괄호를 사용 하 여 첨자 수 있습니다. 아래 첨자는 형식 `Int` 또는 형식 `Range`를 사용 하 여 배열 요소의 하위 집합을 포함 하는 단일 요소나 새 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87275-147">Arrays can be subscripted using square brackets, with subscripts either having type `Int` or type `Range`, to obtain either single elements or new arrays containing a subset of the elements of an array.</span></span>
<span data-ttu-id="87275-148">배열의 첨자는 0부터 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-148">The subscripts of arrays are zero-based:</span></span>

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a><span data-ttu-id="87275-149">튜플 형식</span><span class="sxs-lookup"><span data-stu-id="87275-149">Tuple Types</span></span>

<span data-ttu-id="87275-150">0 개 이상의 다른 형식 `T0`, `T1`, ..., `Tn`지정 된 경우 새 *튜플 형식을* `(T0, T1, ..., Tn)`로 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-150">Given zero or more different types `T0`, `T1`, ..., `Tn`, we can denote a new  *tuple type* as `(T0, T1, ..., Tn)`.</span></span>
<span data-ttu-id="87275-151">새 튜플 형식을 생성 하는 데 사용 되는 형식은 `(Int, (Qubit, Qubit))`처럼 튜플이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-151">The types used to construct a new tuple type can themselves be tuples, as in `(Int, (Qubit, Qubit))`.</span></span>
<span data-ttu-id="87275-152">그러나 이러한 중첩은 항상 유한 하지만 튜플 형식은 어떤 경우에도 자체적으로 포함 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-152">Such nesting is always finite, however, as tuple types cannot under any circumstances contain themselves.</span></span>

<span data-ttu-id="87275-153">새 튜플 형식의 값은 튜플의 각 형식에서 값의 시퀀스로 구성 된 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-153">Values of the new tuple type are tuples formed by sequences of values from each type in the tuple.</span></span>
<span data-ttu-id="87275-154">예를 들어 `(3, false)`은 `(Int, Bool)`튜플 유형인 형식의 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-154">For instance, `(3, false)` is a tuple whose type is the tuple type `(Int, Bool)`.</span></span>
<span data-ttu-id="87275-155">튜플, 배열의 튜플, 하위 튜플 튜플 등의 배열을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-155">It is possible to create arrays of tuples, tuples of arrays, tuples of sub-tuples, etc.</span></span>

<span data-ttu-id="87275-156">Q # 0.3에서 `Unit`은 빈 튜플의 *형식* 이름입니다. `()`는 빈 튜플 *값*에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-156">As of Q# 0.3, `Unit` is the name of the *type* of the empty tuple; `()` is used for the empty tuple *value*.</span></span>

<span data-ttu-id="87275-157">튜플 인스턴스는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-157">Tuple instances are immutable.</span></span>
<span data-ttu-id="87275-158">Q #에서는 생성 된 튜플의 콘텐츠를 변경 하는 메커니즘을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-158">Q# does not provide a mechanism to change the contents of a tuple once created.</span></span>

<span data-ttu-id="87275-159">튜플은 값을 단일 값으로 수집 하 여 보다 쉽게 전달할 수 있도록 Q # 전체에서 사용 되는 강력한 개념입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-159">Tuples are a powerful concept used throughout Q# to collect values together into a single value, making it easier to pass them around.</span></span>
<span data-ttu-id="87275-160">특히 튜플 표기법을 사용 하면 모든 작업 및 호출 가능에서 정확히 하나의 입력을 사용 하 고 정확히 하나의 출력을 반환 하도록 표현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-160">In particular, using tuple notation, we can express that every operation and callable takes exactly one input and returns exactly one output.</span></span>

### <a name="singleton-tuple-equivalence"></a><span data-ttu-id="87275-161">단일 튜플 동등성</span><span class="sxs-lookup"><span data-stu-id="87275-161">Singleton Tuple Equivalence</span></span>

<span data-ttu-id="87275-162">`(5)` 또는 `([1,2,3])`와 같이 singleton (단일 요소) 튜플 `('T1)`만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-162">It is possible to create a singleton (single-element) tuple, `('T1)`, such as `(5)` or `([1,2,3])`.</span></span>
<span data-ttu-id="87275-163">그러나 Q #은 singleton 튜플을 포함 된 형식의 값과 완전히 동일 하 게 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-163">However, Q# treats a singleton tuple as completely equivalent to a value of the enclosed type.</span></span>
<span data-ttu-id="87275-164">즉, `5`와 `(5)`간에 차이가 없으며 `5`와 `(((5)))`사이 또는 `(5, (6))` 간에 차이가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-164">That is, there is no difference between `5` and `(5)`, or between `5` and `(((5)))`, or between `(5, (6))` and `(5, 6)`.</span></span>

<span data-ttu-id="87275-165">이러한 동등성은 할당 및 식을 비롯 한 모든 용도에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-165">This equivalence applies for all purposes, including assignment and expressions.</span></span>
<span data-ttu-id="87275-166">`5+3`를 작성 하는 데 `(5)+3`를 작성 하는 것은 올바르지만 두 식이 모두 `8`으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-166">It is just as valid to write `(5)+3` as to write `5+3`, and both expressions will evaluate to `8`.</span></span>
<span data-ttu-id="87275-167">특히이는 입력 튜플 또는 출력 튜플 형식이 하나의 필드를 갖는 작업 또는 함수가 단일 인수를 사용 하거나 단일 값을 반환 하는 것으로 간주할 수 있음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-167">In particular, this means that an operation or function whose input tuple or output tuple type has one field can be thought of as taking a single argument or returning a single value.</span></span>

<span data-ttu-id="87275-168">이 속성은 _단일 튜플 동치_로 참조 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-168">We refer to this property as _singleton tuple equivalence_.</span></span>

## <a name="user-defined-types"></a><span data-ttu-id="87275-169">사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="87275-169">User-Defined Types</span></span>

<span data-ttu-id="87275-170">Q # 파일은 법적 형식의 단일 값을 포함 하는 새 명명 된 형식을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-170">A Q# file may define a new named type containing a single value of any legal type.</span></span>
<span data-ttu-id="87275-171">`T`모든 튜플 형식에 대해 `newtype` 문으로 `T`의 하위 형식인 새 사용자 정의 형식을 선언할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-171">For any tuple type `T`, we can declare a new user-defined type that is a subtype of `T` with the `newtype` statement.</span></span>
<span data-ttu-id="87275-172">예를 들어 @"microsoft.quantum.canon" 네임 스페이스에서 복소수는 사용자 정의 형식으로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-172">In the @"microsoft.quantum.canon" namespace, for instance, complex numbers are defined as a user-defined type:</span></span>

```qsharp
newtype Complex = (Double, Double);
```

<span data-ttu-id="87275-173">이 문은 `Double`형식의 익명 항목 두 개를 사용 하 여 새 형식을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87275-173">This statement creates a new type with two anonymous items of type `Double`.</span></span>   
<span data-ttu-id="87275-174">익명 항목 외에도 사용자 정의 형식은 Q # 버전 0.7 이상으로 명명 된 항목을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-174">Aside from anonymous items, user defined types also support named items as of Q# version 0.7 or higher.</span></span> <span data-ttu-id="87275-175">예를 들어 복소수의 실수 부분을 나타내는 double의 경우 `Re` 항목의 이름을로 지정 하 고 허수 부분에 대해 `Im` 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-175">For example, we could have named the to items `Re` for the double representing the real part of a complex number and `Im` for the imaginary part:</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="87275-176">사용자 정의 형식에서 한 항목의 이름을 지정 하는 것은 모든 항목의 이름을 지정 해야 한다는 의미는 아닙니다. 명명 된 항목 및 명명 되지 않은 항목의 모든 조합이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-176">Naming one item in a user defined type does not imply that all items need to be named - any combination of named and unnamed items is supported.</span></span> <span data-ttu-id="87275-177">또한 내부 항목의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-177">Furthermore, also inner items may be named.</span></span>
<span data-ttu-id="87275-178">예를 들어 아래에 정의 된 것 처럼 `Nested` 형식에는 `Int` 형식의 항목만 이름이 지정 되 고 다른 모든 항목은 익명 인 기본 형식 `(Double, (Int, String))`있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-178">The type `Nested` as defined below for example has an underlying type `(Double, (Int, String))`, of which only the item of type `Int` is named and all other items are anonymous.</span></span> 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```
<span data-ttu-id="87275-179">명명 된 항목은 `::`액세스 연산자를 통해 직접 액세스할 수 있다는 장점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-179">Named items have the advantage that they can be accessed directly via the access operator `::`.</span></span> 

```qsharp
function Addition (c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

<span data-ttu-id="87275-180">반면에 익명 항목에 액세스 하려면 `!`후 위 연산자를 사용 하 여 래핑된 값을 먼저 추출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-180">In order to access anonymous items on the other hand, the wrapped value first needs to be extracted using the postfix operator `!`.</span></span>
<span data-ttu-id="87275-181">"래핑 해제" 연산자 `!`는 사용자 정의 형식에 포함 된 값을 추출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-181">The "unwrap" operator, `!`, allows to extract the value contained in a user defined type.</span></span>
<span data-ttu-id="87275-182">이러한 "래핑 해제" 식의 형식은 사용자 정의 형식의 기본 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-182">The type of such an "unwrap" expression is the underlying type of the user defined type.</span></span> 

```qsharp
function PrintMsg (value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

<span data-ttu-id="87275-183">래핑 해제 연산자는 정확히 한 줄의의 래핑을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-183">The unwrap operator unwraps exactly one layer of wrapping.</span></span>
<span data-ttu-id="87275-184">여러 래핑 연산자를 사용 하 여 곱하기 래핑된 값에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-184">Multiple unwrap operators may be used to access a multiply-wrapped value.</span></span>

<span data-ttu-id="87275-185">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-185">For instance:</span></span>

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

<span data-ttu-id="87275-186">자세한 내용은 [래핑 해제 식](xref:microsoft.quantum.language.expressions#unwrap-expressions) 및 [연산자 우선 순위](xref:microsoft.quantum.language.expressions#operator-precedence) 에 대 한 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="87275-186">Take a look at the section on [unwrap expressions](xref:microsoft.quantum.language.expressions#unwrap-expressions) and [operators precedence](xref:microsoft.quantum.language.expressions#operator-precedence) for more details.</span></span>

<span data-ttu-id="87275-187">사용자 정의 형식의 값은 해당 형식 생성자를 호출 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-187">Values of a user defined type can be created by calling the corresponding type constructor:</span></span>

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

<span data-ttu-id="87275-188">또는 [복사 및 업데이트 식을](xref:microsoft.quantum.language.expressions#copy-and-update-expressions)사용 하 여 기존 값에서 새 값을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-188">Alternatively, new values can be created from existing ones using [copy-and-update expressions](xref:microsoft.quantum.language.expressions#copy-and-update-expressions).</span></span> <span data-ttu-id="87275-189">배열의 경우와 같이 이러한 식은 지정 된 명명 된 항목을 제외 하 고 원래 식의 모든 항목 값을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-189">Like for arrays, such expressions copy all item values of the original expression, with the exception of the specified named items.</span></span> <span data-ttu-id="87275-190">이러한 값은 식의 오른쪽에 정의 된 값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-190">For these the values are set to the ones defined on the right hand side of the expression.</span></span> <span data-ttu-id="87275-191">예를 들어 [업데이트 및 재할당 문과](xref:microsoft.quantum.language.statements#update-and-reassign-statement)같이 사용자 정의 형식에 명명 된 항목에 대 한 배열 항목에 사용할 수 있는 다른 언어 구문은 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-191">Any other language constructs, like for example [update-and-reassign statements](xref:microsoft.quantum.language.statements#update-and-reassign-statement), that are available for array items exist for named-items in user defined types as well.</span></span>

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

<span data-ttu-id="87275-192">사용자 정의 형식은 다른 모든 형식을 사용할 수 있는 모든 위치에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-192">User-defined types may be used anywhere any other type may be used.</span></span>
<span data-ttu-id="87275-193">특히 사용자 정의 형식의 배열을 정의 하 고 사용자 정의 형식을 튜플 형식의 요소로 포함 하는 것이 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-193">In particular, it is possible to define an array of a user-defined type and to include a user-defined type as an element of a tuple type.</span></span>

<span data-ttu-id="87275-194">재귀 형식 구조를 만들 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-194">It is not possible to create recursive type structures.</span></span>
<span data-ttu-id="87275-195">즉, 사용자 정의 형식을 정의 하는 형식은 사용자 정의 형식의 요소를 포함 하는 튜플 형식이 아닐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-195">That is, the type that defines a user-defined type may not be a tuple type that includes an element of the user-defined type.</span></span>
<span data-ttu-id="87275-196">보다 일반적으로 사용자 정의 형식에는 순환 종속성이 있을 수 없으므로 다음과 같은 형식 정의 집합이 잘못 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-196">More generally, user-defined types may not have cyclic dependencies on each other, so the following set of type definitions would be illegal:</span></span>

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```

<span data-ttu-id="87275-197">잠재적으로 복잡 한 튜플 형식에 대 한 짧은 별칭을 제공 하는 것 외에도 이러한 형식을 정의 하면 특정 값의 의도를 문서화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-197">In addition to providing short aliases for potentially complicated tuple types, one significant advantage of defining such types is that they can document the intent of a particular value.</span></span>
<span data-ttu-id="87275-198">`Complex`예제로 돌아가면 2D 극좌표 형 좌표를 사용자 정의 형식으로 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-198">Returning to the example of `Complex`, one could have also defined 2D polar coordinates as a user-defined type:</span></span>

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

<span data-ttu-id="87275-199">`Complex`와 `Polar` 모두 기본 형식이 `(Double, Double)`있지만 Q #에서 두 가지 형식이 모두 호환 되지 않습니다. 또한 극좌표로 복잡 한 수학 함수를 실수로 호출 하는 위험을 최소화 하 고 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-199">Even though both `Complex` and `Polar` are both have an underlying type `(Double, Double)`, the two types are wholly incompatible in Q#, minimizing the risk of accidentally calling a complex math function with polar coordinates and vice versa.</span></span>
<span data-ttu-id="87275-200">이러한 방식으로 사용자 정의 형식은와 비슷한 역할 F# 을 합니다. 예를 들면입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-200">In this way, user-defined types have a similar role as Records in F# for example.</span></span> 


## <a name="operation-and-function-types"></a><span data-ttu-id="87275-201">작업 및 함수 형식</span><span class="sxs-lookup"><span data-stu-id="87275-201">Operation and Function Types</span></span>

<span data-ttu-id="87275-202">Q # _작업_ 은 퀀텀 서브루틴입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-202">A Q# _operation_ is a quantum subroutine.</span></span>
<span data-ttu-id="87275-203">즉, 퀀텀 작업을 포함 하는 호출 가능 루틴입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-203">That is, it is a callable routine that contains quantum operations.</span></span>

<span data-ttu-id="87275-204">Q # _함수_ 는 퀀텀 알고리즘 내에서 사용 되는 기존 서브루틴입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-204">A Q# _function_ is a classical subroutine used within a quantum algorithm.</span></span>
<span data-ttu-id="87275-205">기존 코드를 포함할 수 있지만 퀀텀 작업은 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-205">It may contain classical code but no quantum operations.</span></span>
<span data-ttu-id="87275-206">특히 함수는 이러한 기능을 할당 하거나 빌려 서 작업을 호출할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-206">Specifically, functions may not allocate or borrow qubits, nor may they call operations.</span></span>
<span data-ttu-id="87275-207">그러나 처리를 위해 작업 또는 원하는 비트를 전달할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-207">It is possible, however, to pass them operations or qubits for processing.</span></span>
<span data-ttu-id="87275-208">따라서 함수는 동일한 인수를 사용 하 여 호출 하면 항상 동일한 결과를 생성 한다는 점에서 완전히 결정적입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-208">Functions are thus entirely deterministic in the sense that calling them with the same arguments will always produce the same result.</span></span> 

<span data-ttu-id="87275-209">작업 및 함수를 함께 _callables_이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-209">Together, operations and functions are called _callables_.</span></span>  <span data-ttu-id="87275-210">아래에 대 한 몇 가지 [예](#examples) 를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-210">You can see some [examples](#examples) of these below.</span></span>

<span data-ttu-id="87275-211">모든 Q # callables은 단일 값을 입력으로 사용 하 고 단일 값을 출력으로 반환 하는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-211">All Q# callables are considered to take a single value as input and return a single value as output.</span></span>
<span data-ttu-id="87275-212">입력 값과 출력 값 모두 튜플이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-212">Both the input and output values may be tuples.</span></span>
<span data-ttu-id="87275-213">결과를 반환 하지 않는 callables `Unit`입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-213">Callables that have no result return `Unit`.</span></span>
<span data-ttu-id="87275-214">입력이 없는 callables은 빈 튜플을 입력으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-214">Callables that have no input take the empty tuple as input.</span></span>

<span data-ttu-id="87275-215">호출할 수 있는 기본 형식은 `('Tinput => 'Tresult)` 또는 `('Tinput -> 'Tresult)`으로 작성 됩니다. 여기서 `'Tinput`와 `'Tresult`는 모두 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-215">The basic type for any callable is written as `('Tinput => 'Tresult)` or `('Tinput -> 'Tresult)`, where both `'Tinput` and `'Tresult` are types.</span></span>
<span data-ttu-id="87275-216">`=>`를 사용 하는 첫 번째 폼은 작업에 사용 됩니다. 함수의 두 번째 형태 (`->`)입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-216">The first form, with `=>`, is used for operations; the second form, with `->`, for functions.</span></span>
<span data-ttu-id="87275-217">예를 들어 `((Qubit, Pauli) => Result)`은 가능한 단일 수준 비트 측정 작업의 시그니처를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87275-217">For example, `((Qubit, Pauli) => Result)` represents the signature for a possible single-qubit measurement operation.</span></span>

<span data-ttu-id="87275-218">함수 형식은 해당 시그니처로 완전히 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-218">Function types are completely specified by their signature.</span></span>
<span data-ttu-id="87275-219">예를 들어, 각도의 사인을 계산 하는 함수에는 `(Double -> Double)`형식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-219">For example, a function that computes the sine of an angle would have type `(Double -> Double)`.</span></span>

<span data-ttu-id="87275-220">작업 (함수 아님)에는 작업 유형의 일부로 표시 되는 특정 추가 _특징이_ 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-220">Operations—but not functions—have certain additional _characteristics_ that are expressed as part of the operation type.</span></span> <span data-ttu-id="87275-221">이러한 특성에는 작업에서 지 원하는 함수에 대 한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-221">Such characteristics include information about what functors the operation supports.</span></span>
<span data-ttu-id="87275-222">함수는 기본 작업의 특수화를 생성 하는 meta 작업입니다. 아래의 [함수](#functors)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="87275-222">Functors are meta-operations that generate a specialization of a base operation; see [Functors](#functors), below.</span></span>

<span data-ttu-id="87275-223">작업 유형은 입력 유형, 출력 유형 및 해당 특성에 의해 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-223">Operation types are specified by the their input type, output type, and their characteristics.</span></span>    
<span data-ttu-id="87275-224">작업 형식에서 `Controlled` 및/또는 `Adjoint` 함수를 지원 하도록 요구 하려면 해당 특성을 나타내는 주석을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-224">In order to require support for the `Controlled` and/or `Adjoint` functor in an operation type, we need to add an annotation indicating the corresponding characteristics.</span></span>
<span data-ttu-id="87275-225">예를 들어 `is Ctl` 주석은 작업을 제어할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87275-225">An annotation `is Ctl` for example indicates that the operation is controllable.</span></span> <span data-ttu-id="87275-226">해당 형식의 작업에서 `Adjoint` 및 `Controlled` 함수를 모두 지원 하도록 요구 하려는 경우이를 `(Qubit => Unit is Adj + Ctl)`로 표현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-226">If we want to require that an operation of that type supports both the `Adjoint` and `Controlled` functor we can express this as `(Qubit => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="87275-227">`Adj` 사용 되는 작업 특성 및 `Ctl`에 대 한 자세한 내용은 미리 정의 된 두 개의 레이블 집합입니다. 각 레이블은 특정 함수에 대 한 지원 등의 특정 작업 특징을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87275-227">The used operation characteristics `Adj` and `Ctl` strictly speaking are two pre-defined sets of labels, where each label indicates a particular operation characteristics like e.g. support for a particular functor.</span></span>
<span data-ttu-id="87275-228">따라서 `+`은 이러한 두 집합의 합집합을 나타내는 데 사용 되며, 교집합을 나타내는 데 사용 되는 `*` (예: 두 집합에 공통 된 레이블).</span><span class="sxs-lookup"><span data-stu-id="87275-228">Hence, `+` is used to indicate the union of those two sets, and `*` is used to indicate the intersection - i.e. the labels that are common to both sets.</span></span>  

<span data-ttu-id="87275-229">예를 들어 Pauli `X` 작업에는 `(Qubit => Unit is Adj + Ctl)`형식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-229">For example, the Pauli `X` operation has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="87275-230">함수을 지원 하지 않는 작업 형식은 입력 및 출력 형식 만으로 지정 되 고 추가 주석은 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-230">An operation type that does not support any functors is specified by its input and output type alone, with no additional annotation.</span></span>


### <a name="type-parameterized-functions-and-operations"></a><span data-ttu-id="87275-231">형식 매개 변수화 된 함수 및 작업</span><span class="sxs-lookup"><span data-stu-id="87275-231">Type-Parameterized Functions and Operations</span></span>

<span data-ttu-id="87275-232">호출 가능 형식에는 형식 매개 변수가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-232">Callable types may contain type parameters.</span></span>
<span data-ttu-id="87275-233">형식 매개 변수는 작은따옴표가 접두사로 붙는 기호로 표시 됩니다. 예를 들어 `'A`은 올바른 형식 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-233">Type parameters are indicated by a symbol prefixed by a single quote; for example, `'A` is a legal type parameter.</span></span>

<span data-ttu-id="87275-234">단일 서명에서 형식 매개 변수가 두 번 이상 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-234">A type parameter may appear more than once in a single signature.</span></span>
<span data-ttu-id="87275-235">예를 들어, 배열의 각 요소에 다른 함수를 적용 하 고 수집 된 결과를 반환 하는 함수는 시그니처를 `(('A[], 'A->'A) -> 'A[])`합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-235">For example, a function that applies another function to each element of an array and returns the collected results would have signature `(('A[], 'A->'A) -> 'A[])`.</span></span>
<span data-ttu-id="87275-236">마찬가지로 두 작업의 컴퍼지션을 반환 하는 함수에는 서명 `((('A=>'B), ('B=>'C)) -> ('A=>'C))`있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-236">Similarly, a function that returns the composition of two operations might have signature `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span></span>

<span data-ttu-id="87275-237">형식이 매개 변수가 있는 호출 가능 매개 변수를 호출 하는 경우 동일한 형식 매개 변수를 갖는 모든 인수는 동일한 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-237">When invoking a type-parameterized callable, all arguments that have the same type parameter must be of the same type.</span></span>

<span data-ttu-id="87275-238">Q #에서는 형식 매개 변수를 대체할 수 있는 가능한 형식을 제한 하는 메커니즘을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-238">Q# does not provide a mechanism for constraining the possible types that might be substituted for a type parameter.</span></span>

### <a name="type-compatibility"></a><span data-ttu-id="87275-239">형식 호환성</span><span class="sxs-lookup"><span data-stu-id="87275-239">Type Compatibility</span></span>

<span data-ttu-id="87275-240">추가 함수 지원 되는 작업은 함수가 더 작은 작업에 사용 될 수 있지만 동일한 서명이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-240">An operation with additional functors supported may be used anywhere an operation with fewer functors but the same signature is expected.</span></span>
<span data-ttu-id="87275-241">예를 들어 형식 `(Qubit => Unit is Adj)`의 작업은 `(Qubit => Unit)` 형식의 작업이 예상 되는 모든 위치에서 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-241">For instance, an operation of type `(Qubit => Unit is Adj)` may be used anywhere an operation of type `(Qubit => Unit)` is expected.</span></span>

<span data-ttu-id="87275-242">Q #은 호출 가능 반환 형식과 관련 하 여 공변 (covariant)이 있습니다. `'A` 형식을 반환 하는 호출 가능은 입력 형식이 동일한 호출 가능 및 `'A`와 호환 되는 결과 형식에 호환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-242">Q# is covariant with respect to callable return types: a callable that returns a type `'A` is compatible with a callable with the same input type and a result type that `'A` is compatible with.</span></span>

<span data-ttu-id="87275-243">Q #은 입력 유형과 관련 하 여 반공 변 (contravariant)입니다. 입력으로 `'A` 형식을 사용 하는 호출 가능은 같은 결과 형식 및 `'A`와 호환 되는 입력 형식으로 호출할 수 있는와 호환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-243">Q# is contravariant with respect to input types: a callable that takes a type `'A` as input is compatible with a callable with the same result type and an input type that is compatible with `'A`.</span></span>

<span data-ttu-id="87275-244">즉, 다음과 같은 정의가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-244">That is, given the following definitions:</span></span>

```qsharp
operation Invertible (qs : Qubit[]) : Unit 
is Adj {...} 
operation Unitary (qs : Qubit[]) : Unit 
is Adj + Ctl {...} 

function ConjugateInvertibleWith (
   inner: (Qubit[] => Unit is Adj),
   outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj) {...}

function ConjugateUnitaryWith (
   inner: (Qubit[] => Unit is Adj + Ctl),
   outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj + Ctl) {...}
```

<span data-ttu-id="87275-245">다음은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-245">the following are true:</span></span>

- <span data-ttu-id="87275-246">`Invertible` 또는 `Unitary`의 `inner` 인수를 사용 하 여 `ConjugateInvertibleWith` 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-246">The operation `ConjugateInvertibleWith` may be invoked with an `inner` argument of either `Invertible` or `Unitary`.</span></span>
- <span data-ttu-id="87275-247">`ConjugateUnitaryWith` 작업은 `Unitary`의 `inner` 인수를 사용 하 여 호출할 수 있지만 `Invertible`는 호출할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-247">The operation `ConjugateUnitaryWith` may be invoked with an `inner` argument of `Unitary`, but not `Invertible`.</span></span>
- <span data-ttu-id="87275-248">`ConjugateInvertibleWith`에서 반환 될 수 `(Qubit[] => Unit is Adj + Ctl)` 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-248">A value of type `(Qubit[] => Unit is Adj + Ctl)` may be returned from `ConjugateInvertibleWith`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87275-249">Q # 0.3에서는 사용자 정의 형식의 동작에 상당한 차이가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-249">Q# 0.3 introduces a significant difference in the behavior of user-defined types.</span></span>

<span data-ttu-id="87275-250">사용자 정의 형식은 하위 형식이 아니라 기본 형식의 래핑된 버전으로 취급 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-250">User-defined types are treated as a wrapped version of the underlying type, rather than as a subtype.</span></span>
<span data-ttu-id="87275-251">이는 기본 형식의 값이 필요한 경우 사용자 정의 형식의 값을 사용할 수 없음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-251">This means that a value of a user-defined type is not usable where a value of the underlying type is expected.</span></span>

### <a name="functors"></a><span data-ttu-id="87275-252">함수</span><span class="sxs-lookup"><span data-stu-id="87275-252">Functors</span></span>

<span data-ttu-id="87275-253">Q #의 함수는 다른 작업에서 새 작업을 정의 하는 팩터리입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-253">A functor in Q# is a factory that defines a new operation from another operation.</span></span>
<span data-ttu-id="87275-254">함수는 새 작업의 구현을 정의할 때 기본 작업의 구현에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-254">Functors have access to the implementation of the base operation when defining the implementation of the new operation.</span></span>
<span data-ttu-id="87275-255">따라서 함수는 기존의 상위 수준 함수 보다 더 복잡 한 함수를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-255">Thus, functors can perform more complex functions than traditional higher-level functions.</span></span>

<span data-ttu-id="87275-256">함수에는 Q # 형식 시스템에 대 한 표현이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-256">Functors do not have a representation in the Q# type system.</span></span> <span data-ttu-id="87275-257">따라서 현재 변수를 변수에 바인딩하거나 인수로 전달할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-257">It is thus currently not possible to bind them to a variable or pass them as arguments.</span></span> 

<span data-ttu-id="87275-258">함수는 작업에 적용 하 여 새 작업을 반환 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-258">A functor is used by applying it to an operation, returning a new operation.</span></span>
<span data-ttu-id="87275-259">예를 들어 `Adjoint` 함수를 `Y` 작업에 적용 하 여 발생 하는 작업은 `Adjoint Y`으로 작성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-259">For example, the operation that results from applying the `Adjoint` functor to the `Y` operation is written as `Adjoint Y`.</span></span>
<span data-ttu-id="87275-260">그런 다음 다른 작업과 마찬가지로 새 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-260">The new operation may then be invoked like any other operation.</span></span>
<span data-ttu-id="87275-261">따라서 `Adjoint Y(q1)`는 Adjoint 함수를 `Y` 작업에 적용 하 여 새 작업을 생성 하 고 `q1`에 새 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-261">Thus, `Adjoint Y(q1)` applies the Adjoint functor to the `Y` operation to generate a new operation, and applies that new operation to `q1`.</span></span>

<span data-ttu-id="87275-262">마찬가지로 `Controlled X(controls, target)`는 제어 되는 함수를 `X` 작업에 적용 하 여 새 작업을 생성 하 고 `controls` 및 `target`에 새 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-262">Similarly, `Controlled X(controls, target)` applies the Controlled functor to the `X` operation to generate a new operation, and applies that new operation to `controls` and `target`.</span></span>

<span data-ttu-id="87275-263">Q #의 두 표준 함수 `Adjoint` `Controlled`됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-263">The two standard functors in Q# are `Adjoint` and `Controlled`.</span></span>

#### <a name="adjoint"></a><span data-ttu-id="87275-264">Adjoint</span><span class="sxs-lookup"><span data-stu-id="87275-264">Adjoint</span></span>

<span data-ttu-id="87275-265">퀀텀 컴퓨팅에서 작업의 adjoint는 작업의 복잡 한 복소수 바꾸기입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-265">In quantum computing, the adjoint of an operation is the complex conjugate transpose of the operation.</span></span>
<span data-ttu-id="87275-266">단일 연산자를 구현 하는 작업의 경우 adjoint는 작업의 역함수입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-266">For operations that implement a unitary operator, the adjoint is the inverse of the operation.</span></span>
<span data-ttu-id="87275-267">특정 집합에 대 한 다른 단일 작업의 시퀀스를 호출 하는 간단한 작업의 경우, 역방향 시퀀스에서 동일한의 하위 작업에 대 한 adjoint를 적용 하 여 adjoint를 계산할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-267">For a simple operation that just invokes a sequence of other unitary operations on a set of qubits, the adjoint may be computed by applying the adjoints of the sub-operations on the same qubits, in the reverse sequence.</span></span>

<span data-ttu-id="87275-268">작업 식이 지정 된 경우 `Adjoint` 함수를 사용 하 여 새 작업 식을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-268">Given an operation expression, a new operation expression may be formed using the `Adjoint` functor.</span></span>
<span data-ttu-id="87275-269">예를 들어 `Adjoint QFT`은 `QFT` 작업의 adjoint를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-269">For instance, `Adjoint QFT` designates the adjoint of the `QFT` operation.</span></span>
<span data-ttu-id="87275-270">새 작업의 시그니처와 형식이 기본 작업과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-270">The new operation has the same signature and type as the base operation.</span></span>
<span data-ttu-id="87275-271">특히, 새 작업은 `Adjoint`를 허용 하며, 기본 작업에서 수행한 경우에만 `Controlled`를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-271">In particular, the new operation also allows `Adjoint`, and will allow `Controlled` if and only if the base operation did.</span></span>

<span data-ttu-id="87275-272">Adjoint 함수는 자체적으로 반전 됩니다. 즉 `Adjoint Adjoint Op` 항상 `Op`와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-272">The Adjoint functor is its own inverse; that is, `Adjoint Adjoint Op` is always the same as `Op`.</span></span>

#### <a name="controlled"></a><span data-ttu-id="87275-273">제어</span><span class="sxs-lookup"><span data-stu-id="87275-273">Controlled</span></span>

<span data-ttu-id="87275-274">제어 되는 작업 버전은 모든 컨트롤이 지정 된 상태에 있는 경우에만 기본 작업을 효과적으로 적용 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-274">The controlled version of an operation is a new operation that effectively applies the base operation only if all of the control qubits are in a specified state.</span></span>
<span data-ttu-id="87275-275">컨트롤의 superposition에 있는 경우 기본 작업은 superposition의 해당 부분에 coherently 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-275">If the control qubits are in superposition, then the base operation is applied coherently to the appropriate part of the superposition.</span></span>
<span data-ttu-id="87275-276">따라서 제어 된 작업은 종종 되거나 얽 히을 생성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-276">Thus, controlled operations are often used to generate entanglement.</span></span>

<span data-ttu-id="87275-277">Q #에서 제어 되는 버전은 항상 컨트롤의 배열을 사용 하 고, 지정 된 상태는 항상 계산 (`PauliZ`) `One` 상태, $ \ket{1}$에 있는 모든 컨트롤에 대해 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-277">In Q#, controlled versions always take an array of control qubits, and the specified state is always for all of the control qubits to be in the computational (`PauliZ`) `One` state, $\ket{1}$.</span></span>
<span data-ttu-id="87275-278">제어 된 작업 이전에 적절 한 단일 작업을 제어 된 작업 이전에 적용 한 다음, 제어 된 작업 후에 단일 작업의 반대을 적용 하 여 다른 상태를 기반으로 하는 제어를 달성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-278">Controlling based on other states may be achieved by applying the appropriate unitary operation to the control qubits before the controlled operation, and then applying the inverses of the unitary operation after the controlled operation.</span></span>
<span data-ttu-id="87275-279">예를 들어 제어 되는 작업 전후에 `X` 연산을 컨트롤에 적용 하면 작업에서 해당 하는 작업의 `Zero` 상태 ($ \ket{0}$)를 제어 합니다. 이전 및 이후 `H` 작업을 적용 하면 `PauliX` `One` 상태가 제어 됩니다. 즉,{0}{1}상태가 아닌 Pauli X, $ \ket{-} \mathrel{: =} (\ket{2}-\ket `PauliZ`)/\sqrt `One` $의-1 eigenvalue입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-279">For example, applying an `X` operation to a control qubit before and after a controlled operation will cause the operation to control on the `Zero` state ($\ket{0}$) for that qubit; applying an `H` operation before and after will control on the `PauliX` `One` state, that is -1 eigenvalue of Pauli X, $\ket{-} \mathrel{:=} (\ket{0} - \ket{1}) / \sqrt{2}$ rather than the `PauliZ` `One` state.</span></span>

<span data-ttu-id="87275-280">작업 식이 지정 된 경우 `Controlled` 함수를 사용 하 여 새 작업 식을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-280">Given an operation expression, a new operation expression may be formed using the `Controlled` functor.</span></span>
<span data-ttu-id="87275-281">새 작업의 서명은 원래 작업의 서명을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-281">The signature of the new operation is based on the signature of the original operation.</span></span>
<span data-ttu-id="87275-282">결과 형식은 동일 하지만 입력 형식은 두 번째 요소로 서, 컨트롤의 요소를 첫 번째 요소로 사용 하 고 원래 작업의 인수를 두 번째 요소로 보유 하 고 있는 두 번째 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-282">The result type is the same, but the input type is a two-tuple with a qubit array that holds the control qubit(s) as the first element and the arguments of the original operation as the second element.</span></span>
<span data-ttu-id="87275-283">새 작업은 `Controlled`를 지원 하 고 원래 작업에서 수행한 경우에만 `Adjoint`를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-283">The new operation supports `Controlled`, and will support `Adjoint` if and only if the original operation did.</span></span>

<span data-ttu-id="87275-284">원래 작업에 단일 인수만 사용한 경우 단일 튜플 동등성은 여기에서 재생 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-284">If the original operation took only a single argument, then singleton tuple equivalence will come into play here.</span></span>
<span data-ttu-id="87275-285">예를 들어 `Controlled X`은 `X` 작업의 제어 된 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-285">For instance, `Controlled X` is the controlled version of the `X` operation.</span></span>
<span data-ttu-id="87275-286">`X` 형식 `(Qubit => Unit is Adj + Ctl)`이므로 `Controlled X` `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`형식입니다. 단일 튜플 때문에 `((Qubit[], Qubit) => Unit is Adj + Ctl)`와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-286">`X` has type `(Qubit => Unit is Adj + Ctl)`, so `Controlled X` has type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`; because of singleton tuple equivalence, this is the same as `((Qubit[], Qubit) => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="87275-287">기본 작업에서 여러 인수를 사용한 경우에는 작업의 제어 되는 버전에 대 한 해당 인수를 괄호로 묶어 튜플로 변환 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-287">If the base operation took several arguments, remember to enclose the corresponding arguments of the controlled version of the operation in parentheses to convert them into a tuple.</span></span>
<span data-ttu-id="87275-288">예를 들어 `Controlled Rz`은 `Rz` 작업의 제어 된 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-288">For instance, `Controlled Rz` is the controlled version of the `Rz` operation.</span></span>
<span data-ttu-id="87275-289">`Rz` 형식 `((Double, Qubit) => Unit is Adj + Ctl)`이므로 `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`형식이 `Controlled Rz` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-289">`Rz` has type `((Double, Qubit) => Unit is Adj + Ctl)`, so `Controlled Rz` has type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="87275-290">따라서 `Controlled Rz(controls, (0.1, target))`은 `Controlled Rz`의 유효한 호출입니다 (`0.1, target`괄호로 묶은 괄호를 참고).</span><span class="sxs-lookup"><span data-stu-id="87275-290">Thus, `Controlled Rz(controls, (0.1, target))` would be a valid invocation of `Controlled Rz` (note the parentheses around `0.1, target`).</span></span>

<span data-ttu-id="87275-291">또 다른 예로 `CNOT(control, target)` `Controlled X([control], target)`로 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-291">As another example, `CNOT(control, target)` can be implemented as `Controlled X([control], target)`.</span></span> <span data-ttu-id="87275-292">대상이 CCNOT (2 컨트롤)로 제어 되어야 하는 경우 `Controlled X([control1, control2], target)` 문을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-292">If a target should be controlled by 2 control qubits (CCNOT), we can use `Controlled X([control1, control2], target)` statement.</span></span>

### <a name="examples"></a><span data-ttu-id="87275-293">예시</span><span class="sxs-lookup"><span data-stu-id="87275-293">Examples</span></span>

<span data-ttu-id="87275-294">Q # 작업의이 예제는 [측정](https://github.com/microsoft/Quantum/tree/master/samples/getting-started/measurement) 샘플에서 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87275-294">This example of a Q# operation comes from the [Measurement](https://github.com/microsoft/Quantum/tree/master/samples/getting-started/measurement) sample.</span></span> <span data-ttu-id="87275-295">작업 내에서, `H` 및 `X`와 같은 해당 기능에 대 한 퀀텀 작업을 할당 하 고이를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-295">Within operations, we can allocate qubits and use quantum operations on those qubits such as `H` and `X`:</span></span>

```qsharp
/// # Summary
/// Prepares a state and measures it in the Pauli-Z basis.
operation MeasureOneQubit () : Result {
        mutable result = Zero;

        using (qubit = Qubit()) { // Allocate a qubit
            H(qubit);               // Use a quantum operation on that qubit

            set result = M(qubit);      // Measure the qubit

            if (result == One) {    // Reset the qubit so that it can be released
                X(qubit);
            }

            return result;
        }
 }
```

<span data-ttu-id="87275-296">이 함수의 예는 [PhaseEstimation](https://github.com/microsoft/Quantum/tree/master/samples/characterization/phase-estimation) 샘플에서 가져온 것입니다.</span><span class="sxs-lookup"><span data-stu-id="87275-296">This example of a function comes from the [PhaseEstimation](https://github.com/microsoft/Quantum/tree/master/samples/characterization/phase-estimation) sample.</span></span> <span data-ttu-id="87275-297">순수 하 게 클래식 코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="87275-297">It contains purely classical code.</span></span> <span data-ttu-id="87275-298">위의 예제와는 달리, 더 이상 할당 되지 않으며 퀀텀 작업을 사용 하지 않는 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-298">You can see that, unlike the example above, no qubits are allocated, and no quantum operations are used.</span></span>


```qsharp
/// # Summary
/// Given two arrays, returns a new array that is the pointwise product
/// of each of the given arrays.
function MultiplyPointwise (left : Double[], right : Double[]) : Double[] {
    mutable product = new Double[Length(left)];

    for (idxElement in IndexRange(left)) {
        set product w/= idxElement <- left[idxElement] * right[idxElement];
    }
    return product;
}
```

<span data-ttu-id="87275-299">[ReversibleLogicSynthesis](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/reversible-logic-synthesis) 샘플의이 예제와 같이 함수를 처리에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-299">It is also possible for a function to be passed qubits for processing, as in this example from the [ReversibleLogicSynthesis](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/reversible-logic-synthesis) sample.</span></span> <span data-ttu-id="87275-300">이 함수에 전달 되 고 처리에 사용 되는 것은 아니지만, 아무 것도 수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87275-300">Qubits are passed to the function and used for processing, although at no point are the qubit states themselves modified.</span></span>

```qsharp
/// # Summary
/// Translate MCT masks into multiple-controlled Toffoli gates (with single
/// targets).
function GateMasksToToffoliGates (qubits : Qubit[], masks : MCMTMask[]) : MCTGate[] {

    mutable result = new MCTGate[0];
    let n = Length(qubits);

    for (i in 0 .. Length(masks) - 1) {
        let (controls, targets) = (masks[i])!;
        let controlBits = IntegerBits(controls, n);
        let targetBits = IntegerBits(targets, n);
        let cQubits = Subarray(controlBits, qubits);
        let tQubits = Subarray(targetBits, qubits);

        for (target in tQubits) {
            set result += [MCTGate(cQubits, target)];
        }
    }

    return result;
}
```
