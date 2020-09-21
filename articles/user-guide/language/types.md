---
title: 의 형식 Q#
description: 프로그래밍 언어에 사용 되는 다양 한 형식에 대해 알아봅니다 Q# .
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
no-loc:
- Q#
- $$v
ms.openlocfilehash: c4a3e6563b8cabee87d1db6b9cb1c1f1c1a7131b
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835828"
---
# <a name="types-in-no-locq"></a><span data-ttu-id="cf132-103">의 형식 Q#</span><span class="sxs-lookup"><span data-stu-id="cf132-103">Types in Q#</span></span>

<span data-ttu-id="cf132-104">이 문서에서는 Q# 유형 모델과 유형을 지정 하 고 작업 하는 구문에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-104">This article describes the Q# type model and the syntax for specifying and working with types.</span></span> <span data-ttu-id="cf132-105">이러한 형식의 식을 만들고 작동 하는 방법에 대 한 자세한 내용은 [형식 식](xref:microsoft.quantum.guide.expressions)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf132-105">For details on how to create and operate on expressions of these types, see [Type Expressions](xref:microsoft.quantum.guide.expressions).</span></span>

<span data-ttu-id="cf132-106">는 강력한 형식의 Q# 언어로, *strongly-typed* 이러한 형식을 신중히 사용 하면 컴파일러가 Q# 컴파일 시간에 프로그램에 대 한 강력한 보증을 제공 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-106">We note that Q# is a *strongly-typed* language, such that careful use of these types can help the compiler to provide strong guarantees about Q# programs at compile time.</span></span>
<span data-ttu-id="cf132-107">가장 강력한 보증을 제공 하기 위해의 형식 간 변환은 Q# 해당 변환을 표현 하는 함수에 대 한 호출을 명시적으로 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-107">To provide the strongest guarantees possible, conversions between types in Q# must be explicit using calls to functions which express that conversion.</span></span> 
<span data-ttu-id="cf132-108">Q# 는 네임 스페이스의 일부분으로 다양 한 함수를 제공 합니다 <xref:microsoft.quantum.convert> .</span><span class="sxs-lookup"><span data-stu-id="cf132-108">Q# provides a variety of such functions as a part of the <xref:microsoft.quantum.convert> namespace.</span></span>
<span data-ttu-id="cf132-109">반면에 호환 되는 형식에 대 한 upcasts은 암시적으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-109">Upcasts to compatible types, on the other hand, happen implicitly.</span></span> 

<span data-ttu-id="cf132-110">Q# 는 직접 사용 되는 기본 형식과 다른 형식에서 새 형식을 생성 하는 다양 한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-110">Q# provides both primitive types, which are used directly, and a variety of ways to produce new types from other types.</span></span>
<span data-ttu-id="cf132-111">이 문서의 나머지 부분에서 각각에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-111">We describe each in the rest of this article.</span></span>

## <a name="primitive-types"></a><span data-ttu-id="cf132-112">기본 유형</span><span class="sxs-lookup"><span data-stu-id="cf132-112">Primitive Types</span></span>

<span data-ttu-id="cf132-113">이 Q# 언어는 프로그램에서 직접 사용할 수 있는 다음과 같은 *기본 형식을*제공 합니다 Q# .</span><span class="sxs-lookup"><span data-stu-id="cf132-113">The Q# language provides the following *primitive types*, all of which you can use directly in Q# programs.</span></span> <span data-ttu-id="cf132-114">이러한 기본 형식을 사용 하 여 새 형식을 생성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-114">You can also use these primitive types to construct new types.</span></span>

- <span data-ttu-id="cf132-115">`Int`형식은 64 비트 부호 있는 정수를 나타냅니다 (예:,, `2` ) `107` `-5` .</span><span class="sxs-lookup"><span data-stu-id="cf132-115">The `Int` type represents a 64-bit signed integer, for example, `2`, `107`, `-5`.</span></span>
- <span data-ttu-id="cf132-116">`BigInt`형식은 임의 크기의 부호 있는 정수를 나타냅니다 (예:,,) `2L` `107L` `-5L` .</span><span class="sxs-lookup"><span data-stu-id="cf132-116">The `BigInt` type represents a signed integer of arbitrary size, for example, `2L`, `107L`, `-5L`.</span></span>
   <span data-ttu-id="cf132-117">이 형식은 .NET을 기반으로 합니다. <xref:System.Numerics.BigInteger></span><span class="sxs-lookup"><span data-stu-id="cf132-117">This type is based on the .NET <xref:System.Numerics.BigInteger></span></span>
   <span data-ttu-id="cf132-118">형식의 매개 변수로 변환됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-118">type.</span></span>

- <span data-ttu-id="cf132-119">`Double`형식은 배정밀도 부동 소수점 숫자를 나타냅니다 (예:,,) `0.0` `-1.3` `4e-7` .</span><span class="sxs-lookup"><span data-stu-id="cf132-119">The `Double` type represents a double-precision floating-point number, for example, `0.0`, `-1.3`, `4e-7`.</span></span>
- <span data-ttu-id="cf132-120">`Bool`형식은 또는의 부울 값을 나타냅니다 `true` `false` .</span><span class="sxs-lookup"><span data-stu-id="cf132-120">The `Bool` type represents a Boolean value of either `true` or `false`.</span></span>
- <span data-ttu-id="cf132-121">`Range`형식은에 의해 표시 되는 정수 시퀀스를 나타냅니다 `start..step..stop` . 여기서 단계는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-121">The `Range` type represents a sequence of integers, denoted by `start..step..stop`, where denoting the step is optional.</span></span> 
   <span data-ttu-id="cf132-122">예를 들어는 `start .. stop` 에 해당 하 `start..1..stop` 고 `1..2..7` 는 $ \{ 1, 3, 5, 7 $ 시퀀스를 나타냅니다 \} .</span><span class="sxs-lookup"><span data-stu-id="cf132-122">For example, `start .. stop` corresponds to `start..1..stop`, and `1..2..7` represents the sequence $\{1, 3, 5, 7\}$.</span></span>
- <span data-ttu-id="cf132-123">`String`형식은 사용자가 만든 후 불투명 한 유니코드 문자 시퀀스입니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-123">The `String` type is a sequence of Unicode characters that is opaque to the user once created.</span></span>
  <span data-ttu-id="cf132-124">`string`오류 또는 진단 이벤트의 경우 유형을 사용 하 여 메시지를 클래식 호스트에 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-124">Use the `string` type to report messages to a classical host in the case of an error or diagnostic event.</span></span>
- <span data-ttu-id="cf132-125">형식에는 `Unit` 하나의 값만 사용할 수 있습니다 `()` .</span><span class="sxs-lookup"><span data-stu-id="cf132-125">The `Unit` type can have only one value, `()`.</span></span> 
  <span data-ttu-id="cf132-126">이 형식을 사용 하 여 Q# 함수 또는 연산이 정보를 반환 하지 않음을 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-126">Use this type to indicate that a Q# function or operation returns no information.</span></span> 
- <span data-ttu-id="cf132-127">`Qubit`형식은 퀀텀 비트 또는 비트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-127">The `Qubit` type represents a quantum bit or qubit.</span></span>
   <span data-ttu-id="cf132-128">`Qubit`는 사용자에 게 불투명 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-128">`Qubit`s are opaque to the user.</span></span> <span data-ttu-id="cf132-129">다른 작업에 전달 하는 것 외에도 가능한 유일한 작업은 id (같음)를 테스트 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-129">The only operation possible with them, other than passing them to another operation, is to test for identity (equality).</span></span>
   <span data-ttu-id="cf132-130">궁극적으로 `Qubit` 는 퀀텀 프로세서 (또는 퀀텀 시뮬레이터)에서 내장 명령을 호출 하 여에 대 한 작업을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-130">Ultimately, you implement actions on `Qubit`s by calling intrinsic instructions on a quantum processor (or a quantum simulator).</span></span>
- <span data-ttu-id="cf132-131">`Pauli`형식은 4 개의 단일 기능 비트 Pauli 연산자 중 하나를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-131">The `Pauli` type represents one of the four single-qubit Pauli operators.</span></span>
   <span data-ttu-id="cf132-132">이 형식을 사용 하 여 회전의 기본 연산을 나타내고 측정 가능한 관찰 가능를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-132">Use this type to denote the base operation for rotations and to specify the observable being measured.</span></span>
   <span data-ttu-id="cf132-133">`PauliI` `PauliX` 형식 상수인,, `PauliY` 및 `PauliZ` 의 네 가지 가능한 값을 가진 열거형 형식입니다 `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="cf132-133">It is an enumerated type that has four possible values: `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, which are constants of type `Pauli`.</span></span>
- <span data-ttu-id="cf132-134">`Result`형식은 측정 결과를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-134">The `Result` type represents the result of a measurement.</span></span>
   <span data-ttu-id="cf132-135">이는 두 가지 가능한 값인 및 (형식의 상수인)를 사용 하는 열거형 형식입니다 `One` `Zero` `Result` .</span><span class="sxs-lookup"><span data-stu-id="cf132-135">It is an enumerated type with two possible values: `One` and `Zero`, which are constants of type `Result`.</span></span>
   <span data-ttu-id="cf132-136">`Zero` + 1 eigenvalue를 측정 했음을 나타냅니다. `One` -1 eigenvalue를 측정 했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-136">`Zero` indicates that the +1 eigenvalue was measured; `One` indicates the -1 eigenvalue was measured.</span></span>

<span data-ttu-id="cf132-137">,,,,,, 및 상수는 `true` `false` `PauliI` `PauliX` `PauliY` `PauliZ` `One` `Zero` 모두에서 예약 된 기호 Q# 입니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-137">The constants `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`, and `Zero` are all reserved symbols in Q#.</span></span>

## <a name="array-types"></a><span data-ttu-id="cf132-138">배열 유형</span><span class="sxs-lookup"><span data-stu-id="cf132-138">Array Types</span></span>

* <span data-ttu-id="cf132-139">유효한 형식의 경우 Q# 해당 형식의 값 배열을 나타내는 형식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-139">For any valid Q# type, there is a type that represents an array of values of that type.</span></span>
    <span data-ttu-id="cf132-140">예를 들어 `Qubit[]` 및는 `(Bool, Pauli)[]` `Qubit` 값과 튜플 값의 배열을 나타냅니다 `(Bool, Pauli)` .</span><span class="sxs-lookup"><span data-stu-id="cf132-140">For example, `Qubit[]` and `(Bool, Pauli)[]` represent arrays of `Qubit` values and `(Bool, Pauli)` tuple values.</span></span>

* <span data-ttu-id="cf132-141">배열의 배열도 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-141">An array of arrays is also valid.</span></span> <span data-ttu-id="cf132-142">앞의 예제에서 확장 하면 배열의 배열이 표시 `(Bool, Pauli)` 됩니다 `(Bool, Pauli)[][]` .</span><span class="sxs-lookup"><span data-stu-id="cf132-142">Expanding on the previous example, an array of `(Bool, Pauli)` arrays is denoted `(Bool, Pauli)[][]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="cf132-143">이 예제는 `(Bool, Pauli)[][]` 사각형 2 차원 배열이 아니라 잠재적으로 가변 배열 배열을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-143">This example, `(Bool, Pauli)[][]`, represents a potentially jagged array of arrays and not a rectangular two-dimensional array.</span></span> <span data-ttu-id="cf132-144">Q# 는 사각형 다차원 배열을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-144">Q# does not support rectangular multi-dimensional arrays.</span></span>

* <span data-ttu-id="cf132-145">Q#에서와 같이 배열의 요소 주위에 대괄호를 사용 하 여 소스 코드에서 배열 값을 쓸 수 있습니다 `[PauliI, PauliX, PauliY, PauliZ]` .</span><span class="sxs-lookup"><span data-stu-id="cf132-145">An array value can be written in Q# source code by using square brackets around the elements of an array, as in `[PauliI, PauliX, PauliY, PauliZ]`.</span></span>
<span data-ttu-id="cf132-146">배열의 모든 항목에 대 한 공통 기본 형식은 배열 리터럴의 형식을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-146">The common base type of all items in the array determines the type of an array literal.</span></span> <span data-ttu-id="cf132-147">따라서 공통 된 기본 형식이 없는 요소를 사용 하 여 배열을 생성 하면 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-147">Hence, constructing an array with elements that have no common base type raises an error.</span></span>  
<span data-ttu-id="cf132-148">예제는 [callables 배열](xref:microsoft.quantum.guide.expressions#arrays-of-callables)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf132-148">For an example, see [arrays of callables](xref:microsoft.quantum.guide.expressions#arrays-of-callables).</span></span>

    > [!WARNING]
    > <span data-ttu-id="cf132-149">배열의 요소를 만든 후에는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-149">Once created, the elements of an array cannot be changed.</span></span>
    > <span data-ttu-id="cf132-150">수정 된 배열을 생성 하려면 [업데이트 및 재할당 문이나](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) [복사 및 업데이트 식을](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions)사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-150">To construct a modified array, use [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) or [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span>

* <span data-ttu-id="cf132-151">또는 키워드를 사용 하 여 크기에서 배열을 만들 수 있습니다 `new` .</span><span class="sxs-lookup"><span data-stu-id="cf132-151">Alternatively, an array can be created from its size using the `new` keyword:</span></span>

    ```qsharp
    let zeros = new Int[13];
    // you can also use new for creating empty arrays:
    let emptyRegister = new Qubit[0];
    ```

* <span data-ttu-id="cf132-152">핵심 함수를 사용 `Length` 하 여 배열의 요소 수를로 가져옵니다 `Int` .</span><span class="sxs-lookup"><span data-stu-id="cf132-152">Use the core function `Length` to obtain the number of elements from an array as an `Int`.</span></span>
* <span data-ttu-id="cf132-153">배열을 첨자 하 여 배열 요소의 하위 집합을 포함 하는 단일 요소나 새 배열을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-153">Arrays can be subscripted to obtain either single elements or new arrays containing a subset of the elements of an array.</span></span>
<span data-ttu-id="cf132-154">배열의 첨자는 0부터 시작 하며 형식 또는 형식 이어야 합니다 `Int` `Range` .</span><span class="sxs-lookup"><span data-stu-id="cf132-154">The subscripts of arrays are zero-based and must be type `Int` or type `Range`:</span></span>

    ```qsharp
    let arr = [10, 11, 36, 49];
    let ten = arr[0]; // 10
    let odds = arr[1..2..4]; // [11, 49]
    ```

## <a name="tuple-types"></a><span data-ttu-id="cf132-155">튜플 형식</span><span class="sxs-lookup"><span data-stu-id="cf132-155">Tuple Types</span></span>

<span data-ttu-id="cf132-156">튜플은 Q# 단일 값으로 함께 값을 수집 하 여 보다 쉽게 전달할 수 있도록 하는 데 사용 되는 강력한 개념입니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-156">Tuples are a powerful concept used throughout Q# to collect values together into a single value, making it easier to pass them around.</span></span>
<span data-ttu-id="cf132-157">특히 튜플 표기법을 사용 하면 모든 작업 및 호출 가능에서 정확히 하나의 입력을 사용 하 고 정확히 하나의 출력을 반환 하도록 표현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-157">In particular, using tuple notation, you can express that every operation and callable takes exactly one input and returns exactly one output.</span></span>

* <span data-ttu-id="cf132-158">0 개 이상의 다른 형식 `T0` ,, ...,이 지정 된 경우 `T1` `Tn` 새  *튜플 형식을* 로 나타낼 수 `(T0, T1, ..., Tn)` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-158">Given zero or more different types `T0`, `T1`, ..., `Tn`, you can denote a new  *tuple type* as `(T0, T1, ..., Tn)`.</span></span>
<span data-ttu-id="cf132-159">에서와 같이 새 튜플 형식을 생성 하는 데 사용 되는 형식은 튜플이 될 수 있습니다 `(Int, (Qubit, Qubit))` .</span><span class="sxs-lookup"><span data-stu-id="cf132-159">The types used to construct a new tuple type can themselves be tuples, as in `(Int, (Qubit, Qubit))`.</span></span>
<span data-ttu-id="cf132-160">그러나 이러한 중첩은 항상 유한 하지만 튜플 형식은 어떤 경우에도 자체적으로 포함 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-160">Such nesting is always finite, however, as tuple types cannot under any circumstances contain themselves.</span></span>

* <span data-ttu-id="cf132-161">새 튜플 형식의 값은 튜플의 각 형식에서 값의 시퀀스로 구성 된 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-161">The values of the new tuple type are tuples formed by sequences of values from each type in the tuple.</span></span>
<span data-ttu-id="cf132-162">예를 들어 `(3, false)` 는 튜플 유형인 형식의 튜플입니다 `(Int, Bool)` .</span><span class="sxs-lookup"><span data-stu-id="cf132-162">For example, `(3, false)` is a tuple whose type is the tuple type `(Int, Bool)`.</span></span>
<span data-ttu-id="cf132-163">튜플, 배열의 튜플, 하위 튜플 튜플 등의 배열을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-163">It is possible to create arrays of tuples, tuples of arrays, tuples of sub-tuples, and so on.</span></span>

* <span data-ttu-id="cf132-164">Q#0.3을 사용 하 여 `Unit` 은 빈 튜플의 *형식* 이름입니다 .는 `()` 빈 튜플의 *값* 에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-164">As of Q# 0.3, `Unit` is the name of the *type* of the empty tuple; `()` is used for the *value* of the empty tuple.</span></span>

* <span data-ttu-id="cf132-165">튜플 인스턴스는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-165">Tuple instances are immutable.</span></span>
<span data-ttu-id="cf132-166">Q# 는 생성 된 튜플의 콘텐츠를 변경 하는 메커니즘을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-166">Q# does not provide a mechanism to change the contents of a tuple once created.</span></span>



### <a name="singleton-tuple-equivalence"></a><span data-ttu-id="cf132-167">단일 튜플 동등성</span><span class="sxs-lookup"><span data-stu-id="cf132-167">Singleton Tuple Equivalence</span></span>

<span data-ttu-id="cf132-168">또는와 같은 singleton (단일 요소) 튜플을 만들 수 있습니다 `('T1)` `(5)` `([1,2,3])` .</span><span class="sxs-lookup"><span data-stu-id="cf132-168">It is possible to create a singleton (single-element) tuple `('T1)`, such as `(5)` or `([1,2,3])`.</span></span>
<span data-ttu-id="cf132-169">그러나는 Q# singleton 튜플을 포함 된 형식의 값과 동일 하 게 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-169">However, Q# treats a singleton tuple as equivalent to a value of the enclosed type.</span></span>
<span data-ttu-id="cf132-170">즉,과 사이에 차이가 없으며,과 사이에 차이가 없습니다 `5` `(5)` `5` `(((5)))` `(5, (6))` `(5, 6)` .</span><span class="sxs-lookup"><span data-stu-id="cf132-170">That is, there is no difference between `5` and `(5)`, or between `5` and `(((5)))`, or between `(5, (6))` and `(5, 6)`.</span></span>
<span data-ttu-id="cf132-171">작성 하는 것 처럼 작성 하는 것은 올바르지만 `(5)+3` `5+3` 두 식이 모두로 계산 됩니다 `8` .</span><span class="sxs-lookup"><span data-stu-id="cf132-171">It is just as valid to write `(5)+3` as it is to write `5+3`; both expressions evaluate to `8`.</span></span>

<span data-ttu-id="cf132-172">이러한 동등성은 할당 및 식을 비롯 한 모든 용도에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-172">This equivalence applies for all purposes, including assignment and expressions.</span></span>
<span data-ttu-id="cf132-173">식이 지정 된 경우 괄호로 묶인 동일한 식이 동일한 형식의 식입니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-173">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="cf132-174">예를 들어는 형식의 식이 고는 형식의 식이고는 `(7)` `Int` `([1,2,3])` `Int[]` `((1,2))` 형식의 식입니다 `(Int, Int)` .</span><span class="sxs-lookup"><span data-stu-id="cf132-174">For example, `(7)` is an expression of type `Int`, `([1,2,3])` is an expression of type `Int[]`, and `((1,2))` is an expression of type `(Int, Int)`.</span></span>

<span data-ttu-id="cf132-175">특히이는 입력 튜플 또는 출력 튜플 형식에 단일 인수를 사용 하거나 단일 값을 반환 하는 하나의 필드가 있는 작업 또는 함수를 볼 수 있음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-175">In particular, this means that you can view an operation or function whose input tuple or output tuple type has one field as taking a single argument or returning a single value.</span></span>

<span data-ttu-id="cf132-176">이 속성은 _단일 튜플 동치_로 참조 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-176">We refer to this property as _singleton tuple equivalence_.</span></span>


## <a name="user-defined-types"></a><span data-ttu-id="cf132-177">사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="cf132-177">User-Defined Types</span></span>

<span data-ttu-id="cf132-178">사용자 정의 형식 선언은 키워드로 구성 된 `newtype` 다음 사용자 정의 형식 이름, `=` , 유효한 형식 사양 및 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-178">A user-defined type declaration consists of the keyword `newtype`, followed by the name of the user-defined type, an `=`, a valid type specification, and a terminating semicolon.</span></span>

<span data-ttu-id="cf132-179">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-179">For example:</span></span>

```qsharp
newtype PairOfInts = (Int, Int);
```
    
* <span data-ttu-id="cf132-180">각 Q# 소스 파일은 원하는 수의 사용자 정의 형식을 선언할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-180">Each Q# source file may declare any number of user-defined types.</span></span>
* <span data-ttu-id="cf132-181">형식 이름은 네임 스페이스 내에서 고유 해야 하며 작업 및 함수 이름과 충돌 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-181">Type names must be unique within a namespace and may not conflict with operation and function names.</span></span>
* <span data-ttu-id="cf132-182">사용자 정의 형식은 기본 형식이 동일한 경우에도 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-182">User-defined types are distinct, even if the base types are identical.</span></span>
<span data-ttu-id="cf132-183">특히 기본 형식이 동일한 경우에도 두 사용자 정의 형식의 값 사이에 자동 변환이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-183">In particular, there is no automatic conversion between the values of two user-defined types, even if the underlying types are identical.</span></span>

### <a name="named-vs-anonymous-items"></a><span data-ttu-id="cf132-184">명명 된 항목과 익명 항목 비교</span><span class="sxs-lookup"><span data-stu-id="cf132-184">Named vs. anonymous items</span></span>

<span data-ttu-id="cf132-185">Q#파일은 모든 법적 형식의 단일 값을 포함 하는 새 명명 된 형식을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-185">A Q# file may define a new named type containing a single value of any legal type.</span></span>
<span data-ttu-id="cf132-186">모든 튜플 형식의 경우 `T` 문을 사용 하 여의 하위 형식인 새 사용자 정의 형식을 선언할 수 있습니다 `T` `newtype` .</span><span class="sxs-lookup"><span data-stu-id="cf132-186">For any tuple type `T`, you can declare a new user-defined type that is a subtype of `T` with the `newtype` statement.</span></span>
<span data-ttu-id="cf132-187">예를 들어 @"microsoft.quantum.math" 네임 스페이스에서 복소수는 사용자 정의 형식으로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-187">In the @"microsoft.quantum.math" namespace, for example, complex numbers are defined as a user-defined type:</span></span>

```qsharp
newtype Complex = (Double, Double);
```
<span data-ttu-id="cf132-188">이 문은 형식의 익명 항목 두 개를 사용 하 여 새 형식을 만듭니다 `Double` .</span><span class="sxs-lookup"><span data-stu-id="cf132-188">This statement creates a new type with two anonymous items of type `Double`.</span></span>   

<span data-ttu-id="cf132-189">익명 항목 외에도 사용자 정의 형식은 버전 0.7 이상으로 *명명 된 항목* 을 지원 Q# 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-189">Aside from anonymous items, user-defined types also support *named items* as of Q# version 0.7 or higher.</span></span> <span data-ttu-id="cf132-190">예를 들어 `Real` 복소수의 실수 부분을 나타내는 double에 대해 항목의 이름을로, 허수 부분에 대해로 이름을로 설정할 수 있습니다 `Imag` .</span><span class="sxs-lookup"><span data-stu-id="cf132-190">For example, you could name the items to `Real` for the double representing the real part of a complex number and `Imag` for the imaginary part:</span></span> 

```qsharp
newtype Complex = (Real : Double, Imag : Double);
```
<span data-ttu-id="cf132-191">사용자 정의 형식에서 한 항목의 이름을 지정 하는 것은 모든 항목의 이름을 지정 해야 한다는 의미는 아닙니다. 명명 된 항목 및 명명 되지 않은 항목의 모든 조합이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-191">Naming one item in a user-defined type does not imply that all items need to be named - any combination of named and unnamed items is supported.</span></span> <span data-ttu-id="cf132-192">또한 내부 항목의 이름을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-192">Furthermore, inner items may also be named.</span></span>
<span data-ttu-id="cf132-193">예를 들어 아래에 정의 된 형식에는 형식 `Nested` `(Double, (Int, String))` 의 항목만 이라는 기본 형식이 `Int` 있으며, 다른 모든 항목은 익명입니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-193">The type `Nested`, as defined below for example, has an underlying type `(Double, (Int, String))`, of which only the item of type `Int` is named, and all other items are anonymous.</span></span> 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

<span data-ttu-id="cf132-194">명명 된 항목은 *액세스 연산자* 를 통해 직접 액세스할 수 있다는 장점이 있습니다 `::` .</span><span class="sxs-lookup"><span data-stu-id="cf132-194">Named items have the advantage that they can be accessed directly via the *access operator* `::`.</span></span> 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Real + c2::Real, c1::Imag + c2::Imag);
}
```

<span data-ttu-id="cf132-195">잠재적으로 복잡 한 튜플 형식에 대 한 짧은 별칭을 제공 하는 것 외에도 이러한 형식을 정의 하면 특정 값의 의도를 문서화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-195">In addition to providing short aliases for potentially complicated tuple types, a significant advantage of defining such types is that they can document the intent of a particular value.</span></span>
<span data-ttu-id="cf132-196">의 예제로 돌아가면 `Complex` 극좌표 형 표현인 사용자 정의 형식으로 정의 했을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-196">Returning to the example of `Complex`, one could have also defined a polar coordinate represenation as a user-defined type:</span></span>

```qsharp
newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```

<span data-ttu-id="cf132-197">`Complex`및 `ComplexPolar` 둘 다에 기본 형식이 있는 경우에도 두 형식은 모두와 `(Double, Double)` 완전히 호환 되지 않으므로 Q# 극좌표를 사용 하 여 복잡 한 수학 함수를 실수로 호출 하는 위험을 최소화 하 고 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-197">Even though both `Complex` and `ComplexPolar` both have an underlying type `(Double, Double)`, the two types are wholly incompatible in Q#, minimizing the risk of accidentally calling a complex math function with polar coordinates and vice versa.</span></span>

#### <a name="access-anonymous-items-with-the-unwrap-operator"></a><span data-ttu-id="cf132-198">래핑 해제 연산자를 사용 하 여 익명 항목 액세스</span><span class="sxs-lookup"><span data-stu-id="cf132-198">Access anonymous items with the unwrap operator</span></span>

<span data-ttu-id="cf132-199">익명 항목에 액세스 하려면 먼저 후 위 연산자를 사용 하 여 래핑된 값을 추출 합니다 `!` .</span><span class="sxs-lookup"><span data-stu-id="cf132-199">To access anonymous items, first extract the wrapped value using the postfix operator `!`.</span></span>
<span data-ttu-id="cf132-200">"래핑 해제" 연산자를 사용 하 여 `!` 사용자 정의 형식에 포함 된 값을 추출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-200">With the "unwrap" operator, `!`, you can extract the value contained in a user-defined type.</span></span>
<span data-ttu-id="cf132-201">이러한 "래핑 해제" 식의 형식은 사용자 정의 형식의 기본 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-201">The type of such an "unwrap" expression is the underlying type of the user-defined type.</span></span> 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

<span data-ttu-id="cf132-202">단일 래핑 해제 연산자는 한 줄의의 래핑을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-202">A single unwrap operator unwraps one layer of wrapping.</span></span> <span data-ttu-id="cf132-203">여러 래핑 해제 연산자를 사용 하 여 곱하기 래핑된 값에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-203">Use multiple unwrap operators to access a multiply-wrapped value.</span></span>

<span data-ttu-id="cf132-204">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-204">For example:</span></span>

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

<span data-ttu-id="cf132-205">래핑 해제 연산자에 대 한 자세한 내용은 [ Q# 의 형식 식 ](xref:microsoft.quantum.guide.expressions)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf132-205">For more details on the unwrap operator, see [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions).</span></span>

### <a name="creating-values-of-user-defined-types"></a><span data-ttu-id="cf132-206">사용자 정의 형식 값 만들기</span><span class="sxs-lookup"><span data-stu-id="cf132-206">Creating values of user-defined types</span></span>

<span data-ttu-id="cf132-207">해당 형식 생성자를 호출 하 여 사용자 정의 형식의 값을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-207">Create values of a user-defined type by calling the corresponding type constructor:</span></span>

```qsharp
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

<span data-ttu-id="cf132-208">또는 [복사 및 업데이트 식을](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions)사용 하 여 기존 값에서 새 값을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-208">Alternatively, you can create new values from existing ones using [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span> <span data-ttu-id="cf132-209">배열과 마찬가지로 복사 및 업데이트 식은 지정 된 명명 된 항목을 제외 하 고 원래 식의 모든 항목 값을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-209">Just as they do with arrays, copy-and-update expressions copy all item values of the original expression, except for the specified named items.</span></span> <span data-ttu-id="cf132-210">이러한 예외에 대해 이러한 항목의 값은 식의 오른쪽에 정의 된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-210">For these exceptions, the values of these items are the values defined on the right-hand side of the expression.</span></span> <span data-ttu-id="cf132-211">[업데이트 및 재할당 문과](xref:microsoft.quantum.guide.variables#update-and-reassign-statements)같이 배열 항목에 사용할 수 있는 다른 언어 구문은 사용자 정의 형식의 명명 된 항목에도 존재 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-211">Any other language constructs that are available for array items, for example [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), exist for named-items in user-defined types as well.</span></span>

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

* <span data-ttu-id="cf132-212">다른 형식을 사용 하는 모든 위치에서 사용자 정의 형식을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-212">You can use user-defined types anywhere you use any other types.</span></span>
<span data-ttu-id="cf132-213">특히 사용자 정의 형식의 배열을 정의 하 고 사용자 정의 형식을 튜플 형식의 요소로 포함 하는 것이 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-213">In particular, it is possible to define an array of a user-defined type and to include a user-defined type as an element of a tuple type.</span></span>

* <span data-ttu-id="cf132-214">재귀 형식 구조를 만들 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-214">It is not possible to create recursive type structures.</span></span>
<span data-ttu-id="cf132-215">즉, 사용자 정의 형식을 정의 하는 형식은 사용자 정의 형식의 요소를 포함 하는 튜플 형식일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-215">That is, the type that defines a user-defined type cannot be a tuple type that includes an element of the user-defined type.</span></span>
<span data-ttu-id="cf132-216">보다 일반적으로 사용자 정의 형식에는 순환 종속성이 있을 수 없으므로 다음과 같은 형식 정의 집합이 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-216">More generally, user-defined types may not have cyclic dependencies on each other, so the following set of type definitions are invalid:</span></span>

    ```qsharp
    newtype TypeA = (Int, TypeB);
    newtype TypeB = (Double, TypeC);
    newtype TypeC = (TypeA, Range);
    ```


## <a name="operation-and-function-types"></a><span data-ttu-id="cf132-217">작업 및 함수 형식</span><span class="sxs-lookup"><span data-stu-id="cf132-217">Operation and Function Types</span></span>

<span data-ttu-id="cf132-218">다음 형식 및이 제공 됩니다 `'Tinput` `'Tresult` .</span><span class="sxs-lookup"><span data-stu-id="cf132-218">Given the types `'Tinput` and `'Tresult`:</span></span>

* <span data-ttu-id="cf132-219">`('Tinput => 'Tresult)` 는 모든 *작업*(예:)에 대 한 기본 형식입니다 `((Qubit, Pauli) => Result)` .</span><span class="sxs-lookup"><span data-stu-id="cf132-219">`('Tinput => 'Tresult)` is the basic type for any *operation*, for example `((Qubit, Pauli) => Result)`.</span></span>
* <span data-ttu-id="cf132-220">`('Tinput -> 'Tresult)` 는 *함수*에 대 한 기본 형식입니다 (예:) `(Int -> Int)` .</span><span class="sxs-lookup"><span data-stu-id="cf132-220">`('Tinput -> 'Tresult)` is the basic type for any *function*, for example `(Int -> Int)`.</span></span> 

<span data-ttu-id="cf132-221">이를 호출 가능의 *서명* 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-221">These are called the *signature* of the callable.</span></span>

* <span data-ttu-id="cf132-222">모든 Q# callables은 단일 값을 입력으로 사용 하 고 단일 값을 출력으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-222">All Q# callables take a single value as input and return a single value as output.</span></span>
* <span data-ttu-id="cf132-223">입력 및 출력 값 모두에 튜플을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-223">You can use tuples for both the input and output values.</span></span>
* <span data-ttu-id="cf132-224">결과가 없는 callables은을 반환 `Unit` 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-224">Callables that have no result, return `Unit`.</span></span>
* <span data-ttu-id="cf132-225">입력이 없는 callables은 빈 튜플을 입력으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-225">Callables that have no input take the empty tuple as input.</span></span>

### <a name="functors"></a><span data-ttu-id="cf132-226">함수</span><span class="sxs-lookup"><span data-stu-id="cf132-226">Functors</span></span>

<span data-ttu-id="cf132-227">*함수* 형식은 해당 시그니처로 완전히 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-227">*Function* types are completely specified by their signature.</span></span> <span data-ttu-id="cf132-228">예를 들어, 각도의 사인을 계산 하는 함수는 형식을 갖습니다 `(Double -> Double)` .</span><span class="sxs-lookup"><span data-stu-id="cf132-228">For example, a function that computes the sine of an angle would have type `(Double -> Double)`.</span></span> 

<span data-ttu-id="cf132-229">작업에는 작업 형식의 일부로 표시 되는 특정 추가 *특징이 있습니다.*</span><span class="sxs-lookup"><span data-stu-id="cf132-229">*Operations* have certain additional characteristics that are expressed as part of the operation type.</span></span> <span data-ttu-id="cf132-230">이러한 특성에는 작업에서 지 원하는 *함수* 에 대 한 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-230">Such characteristics include information about which *functors* the operation supports.</span></span>
<span data-ttu-id="cf132-231">예를 들어 작업을 실행 하는 동안 다른 값을 사용 하는 경우 함수를 지원 해야 합니다 `Controlled` . 작업에 역이 있으면 함수를 지원 해야 합니다 `Adjoint` .</span><span class="sxs-lookup"><span data-stu-id="cf132-231">For example, if the running of the operation relies on the state of other qubits, then it should support the `Controlled` functor; if the operation has an inverse, then it should support the `Adjoint` functor.</span></span>

> [!NOTE]
> <span data-ttu-id="cf132-232">이 문서에서는 함수에서 작업 서명을 변경 하는 방법에 대해서만 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-232">This article only discuss how functors alter the operation signature.</span></span> <span data-ttu-id="cf132-233">함수 및 작업에 대 한 자세한 내용은 [의 Q# 작업 및 함수 ](xref:microsoft.quantum.guide.operationsfunctions)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf132-233">For more details about functors and operations, see [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span> 

<span data-ttu-id="cf132-234">`Controlled`작업 형식에서 and/or 함수를 지원 하려면 `Adjoint` 해당 특성을 나타내는 주석을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-234">To require support for the `Controlled` and/or `Adjoint` functor in an operation type, you need to add an annotation indicating the corresponding characteristics.</span></span>
<span data-ttu-id="cf132-235">주석 `is Ctl` (예:)은 `(Qubit => Unit is Ctl)` 작업을 제어할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-235">The annotation `is Ctl` (for example, `(Qubit => Unit is Ctl)`) indicates that the operation is controllable.</span></span> <span data-ttu-id="cf132-236">즉, 해당 실행은 다른 비트율 비트 또는 기타 비트의 상태에 의존 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-236">That is, its run relies on the state of another qubit or qubits.</span></span> <span data-ttu-id="cf132-237">마찬가지로 주석은 `is Adj` 작업에 adjoint가 있음을 나타냅니다. 즉, 작업을 연속적으로 적용 한 다음 해당 adjoint 상태를 변경 되지 않은 상태로 유지 하는 "반전" 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-237">Similarly, the annotation `is Adj` indicates that the operation has an adjoint, that is, it can be "inverted" such that successively applying an operation and then its adjoint to a state leaves the state unchanged.</span></span> 

<span data-ttu-id="cf132-238">해당 형식의 작업에서 및 함수를 둘 다 지원 하도록 요구 하려는 경우 `Adjoint` `Controlled` 이를로 표현할 수 있습니다 `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="cf132-238">If you want to require that an operation of that type supports both the `Adjoint` and `Controlled` functor you can express this as `(Qubit => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="cf132-239">예를 들어 기본 제공 Pauli 작업에는 <xref:microsoft.quantum.intrinsic.x> 형식이 `(Qubit => Unit is Adj + Ctl)` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-239">For example, the built-in Pauli <xref:microsoft.quantum.intrinsic.x> operation has type `(Qubit => Unit is Adj + Ctl)`.</span></span> 

<span data-ttu-id="cf132-240">함수을 지원 하지 않는 작업 형식은 입력 및 출력 형식 만으로 지정 되 고 추가 주석은 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-240">An operation type that does not support any functors is specified by its input and output type alone, with no additional annotation.</span></span>

### <a name="type-parameterized-functions-and-operations"></a><span data-ttu-id="cf132-241">형식 매개 변수화 된 함수 및 작업</span><span class="sxs-lookup"><span data-stu-id="cf132-241">Type-Parameterized Functions and Operations</span></span>

<span data-ttu-id="cf132-242">호출 가능 형식에는 *형식 매개 변수가*포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-242">Callable types may contain *type parameters*.</span></span>
<span data-ttu-id="cf132-243">작은따옴표를 접두사로 사용 하는 기호를 사용 하 여 형식 매개 변수를 나타냅니다. 예를 들어 `'A` 은 올바른 형식 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-243">Use a symbol prefixed by a single quote to indicated a type parameter; for example, `'A` is a legal type parameter.</span></span>
<span data-ttu-id="cf132-244">형식 매개 변수가 있는 callables을 정의 하는 방법에 대 한 자세한 내용 및 세부 정보는 [의 Q# 작업 및 함수 ](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf132-244">For more information and details on how to define type-parameterized callables, see [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables).</span></span>

<span data-ttu-id="cf132-245">단일 서명에서 형식 매개 변수가 두 번 이상 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-245">A type parameter may appear more than once in a single signature.</span></span>
<span data-ttu-id="cf132-246">예를 들어, 배열의 각 요소에 다른 함수를 적용 하 고 수집 된 결과에 시그니처가 있음을 반환 하는 함수입니다 `(('A[], 'A->'A) -> 'A[])` .</span><span class="sxs-lookup"><span data-stu-id="cf132-246">For example, a function that applies another function to each element of an array and returns the collected results has the signature `(('A[], 'A->'A) -> 'A[])`.</span></span>
<span data-ttu-id="cf132-247">마찬가지로 두 작업의 컴퍼지션을 반환 하는 함수에는 시그니처가 `((('A=>'B), ('B=>'C)) -> ('A=>'C))` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-247">Similarly, a function that returns the composition of two operations has the signature `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span></span>

<span data-ttu-id="cf132-248">형식이 매개 변수가 있는 호출 가능 매개 변수를 호출 하는 경우 동일한 형식 매개 변수를 갖는 모든 인수는 동일한 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-248">When you invoke a type-parameterized callable, all arguments that have the same type parameter must be of the same type.</span></span>

<span data-ttu-id="cf132-249">Q# 는 사용자가 형식 매개 변수를 대체할 수 있는 가능한 형식을 제한 하는 메커니즘을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf132-249">Q# does not provide a mechanism for constraining the possible types that a user might substitute for a type parameter.</span></span>

## <a name="next-steps"></a><span data-ttu-id="cf132-250">다음 단계</span><span class="sxs-lookup"><span data-stu-id="cf132-250">Next steps</span></span>

<span data-ttu-id="cf132-251">언어를 구성 하는 모든 형식을 살펴보았으므로 이제 Q# 다양 한 형식의 식을 만들고 조작 하는 방법을 알아보려면 [의 Q# 형식 식](xref:microsoft.quantum.guide.expressions) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf132-251">Now that you've seen all the types which comprise the Q# language, see [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions) to learn how to create and manipulate expressions of these various types.</span></span>
