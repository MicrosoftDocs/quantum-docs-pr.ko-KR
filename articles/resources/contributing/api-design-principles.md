---
title: Q# API 디자인 원칙
description: Q# API 디자인 원칙
author: cgranade
ms.author: chgranad
ms.date: 3/9/2020
ms.topic: article
uid: microsoft.quantum.contributing.api-design
no-loc:
- Q#
- $$v
ms.openlocfilehash: b8623ba7e876c4ccda42d0ddaa07c0012a763292
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231777"
---
# <a name="no-locq-api-design-principles"></a><span data-ttu-id="40b20-103">Q# API 디자인 원칙</span><span class="sxs-lookup"><span data-stu-id="40b20-103">Q# API Design Principles</span></span>

## <a name="introduction"></a><span data-ttu-id="40b20-104">소개</span><span class="sxs-lookup"><span data-stu-id="40b20-104">Introduction</span></span>

<span data-ttu-id="40b20-105">언어 및 플랫폼으로 서 Q# 사용자는 퀀텀 응용 프로그램을 작성, 실행, 이해 및 탐색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-105">As a language and as a platform, Q# empowers users to write, run, understand, and explore quantum applications.</span></span>
<span data-ttu-id="40b20-106">사용자에 게 권한을 부여 하기 위해 Q# 라이브러리를 설계할 때 API 디자인 원칙 집합을 따라 디자인을 안내 하 고 퀀텀 개발 커뮤니티에 사용할 수 있는 라이브러리를 만드는 데 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-106">In order to empower users, when we design Q# libraries, we follow a set of API design principles to guide our designs and to help us make usable libraries for the the quantum development community.</span></span>
<span data-ttu-id="40b20-107">이 문서에서는 이러한 원칙을 나열 하 고 api를 디자인할 때 적용 하는 방법을 안내 하는 예제를 제공 Q# 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-107">This article lists these principles, and gives examples to help guide how to apply them when designing Q# APIs.</span></span>

> [!TIP]
> <span data-ttu-id="40b20-108">이 문서는 라이브러리 개발 및 심층 라이브러리 기여를 돕기 위한 매우 자세한 문서입니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-108">This is a fairly detailed document that's intended to help guide library development and in-depth library contributions.</span></span>
> <span data-ttu-id="40b20-109">에서 사용자 고유의 라이브러리를 작성 하 Q# 는 경우 나 [ Q# 라이브러리 리포지토리에](https://github.com/microsoft/QuantumLibraries)더 큰 기능을 제공 하는 경우에는 가장 유용 하다는 것을 알게 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-109">You'll probably find it most useful if you're writing your own libraries in Q#, or if you're contributing larger features to the [Q# libraries repository](https://github.com/microsoft/QuantumLibraries).</span></span>
>
> <span data-ttu-id="40b20-110">반면에, 일반적으로 퀀텀 개발 키트에 참여 하는 방법을 알아보려면 [기여 가이드](xref:microsoft.quantum.contributing)로 시작 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-110">On the other hand, if you're looking to learn how to contribute to the Quantum Development Kit more generally, we suggest starting with the [contribution guide](xref:microsoft.quantum.contributing).</span></span>
> <span data-ttu-id="40b20-111">코드 서식을 지정 하는 방법에 대 한 일반적인 정보를 원하는 경우 Q# [스타일 가이드](xref:microsoft.quantum.contributing.style)를 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-111">If you're looking for more general information about how we recommend formatting your Q# code, you may be interested in checking out the [style guide](xref:microsoft.quantum.contributing.style).</span></span>

## <a name="general-principles"></a><span data-ttu-id="40b20-112">일반 원칙</span><span class="sxs-lookup"><span data-stu-id="40b20-112">General Principles</span></span>

<span data-ttu-id="40b20-113">**주요 원칙:** 퀀텀 응용 프로그램에 포커스를 두기 위한 Api를 노출 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-113">**Key principle:** Expose APIs that places the focus on quantum applications.</span></span>

- <span data-ttu-id="40b20-114">✅알고리즘과 응용 프로그램의 상위 수준 구조를 반영 하는 작업 및 함수 **이름을 선택 합니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-114">✅ **DO** choose operation and function names that reflect the   high-level structure of algorithms and applications.</span></span>
- <span data-ttu-id="40b20-115">주로 하위 수준 구현 세부 정보에 중점을 둔 Api를 노출 **하지** ⛔️.</span><span class="sxs-lookup"><span data-stu-id="40b20-115">⛔️ **DON'T** expose APIs that focus primarily on low-level   implementation details.</span></span>

<span data-ttu-id="40b20-116">**주요 원칙:** 샘플 사용 사례를 사용 하 여 각 API 디자인을 시작 하 여 Api를 직관적으로 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-116">**Key principle:** Start each API design with sample use cases to ensure that APIs are intuitive to use.</span></span>

- <span data-ttu-id="40b20-117">✅모든 가능한 사용을 시작에서 디자인 하는 대신 공용 API의 각 구성 요소에 해당 하는 사용 사례가 **있는지 확인 합니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-117">✅ **DO** ensure that each component of a public API has a corresponding use case, rather than trying to design for all possible uses from the start.</span></span>
    <span data-ttu-id="40b20-118">유용 하 게 사용할 수 있는 경우에는 공용 Api를 사용 하지 않는 것이 좋습니다. 하지만 API의 각 부분에 유용한 *구체적인* 예제가 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-118">Put differently, don't introduce public APIs in case they are useful, but make sure that each part of an API has a *concrete* example in which it will be useful.</span></span>

  <span data-ttu-id="40b20-119">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-119">*Examples:*</span></span>
  - <span data-ttu-id="40b20-120">@"microsoft.quantum.canon.applytoeachca" 는 `ApplyToEachCA(H, _)` 여러 퀀텀 알고리즘에서 공통 작업 인 일관 된 superposition 상태에서 등록을 준비 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-120">@"microsoft.quantum.canon.applytoeachca" can be used as `ApplyToEachCA(H, _)` to prepare registers in a uniform superposition state, a common task in many quantum algorithms.</span></span> <span data-ttu-id="40b20-121">동일한 작업은 준비, 숫자 및 oracle 기반 알고리즘의 다른 많은 작업에도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-121">The same operation can also be used for many other tasks in preparation, numerics, and oracle-based algorithms.</span></span>

- <span data-ttu-id="40b20-122">✅새 API 설계 **를 브레인스토밍 및** 워크숍 하 여 직관적이 고 제안 된 사용 사례를 충족 하는지 다시 한 번 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-122">✅ **DO** brainstorm and workshop new API designs to double-check   that they are intuitive and meet proposed use cases.</span></span>

  <span data-ttu-id="40b20-123">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-123">*Examples:*</span></span>
  - <span data-ttu-id="40b20-124">현재 Q \# 코드를 검사 하 여 새 API 디자인이 기존 구현을 간소화 하 고 명확 하 게 파악할 수 있는 방법을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-124">Inspect current Q\# code to see how new API designs could   simplify and clarify existing implementations.</span></span>
  - <span data-ttu-id="40b20-125">주 대상의 담당자를 통해 제안 된 API 디자인을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-125">Review proposed API designs with representatives of primary   audiences.</span></span>

<span data-ttu-id="40b20-126">**주요 원칙:** 읽을 수 있는 코드를 지원 하 고 권장 하는 Api를 디자인 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-126">**Key principle:** Design APIs to support and encourage readable code.</span></span>

- <span data-ttu-id="40b20-127">✅도메인 전문가와 전문가가 아닌 사람이 코드를 읽을 **수 있도록 합니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-127">✅ **DO** ensure that code is readable by domain experts and   non-experts alike.</span></span>
- <span data-ttu-id="40b20-128">✅구현 세부 정보를 적절 하 게 파악 하기 위해 설명서를 사용 하 여 각 작업의 영향 및 함수를 상위 수준 알고리즘 내에서 **수행** 하는 데 집중 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-128">✅ **DO** place the focus on the effects of each operation and   function within the high-level algorithm, using documentation to   delve into implementation details as appropriate.</span></span>
- <span data-ttu-id="40b20-129">✅해당 하는 경우 일반적인 [Q \# 스타일 가이드](xref:microsoft.quantum.contributing.style) **를 따르세요.**</span><span class="sxs-lookup"><span data-stu-id="40b20-129">✅ **DO** follow the common [Q\# style guide](xref:microsoft.quantum.contributing.style) whenever applicable.</span></span>

<span data-ttu-id="40b20-130">**주요 원칙:** 안정적이 고 이전 버전과의 호환성을 제공 하기 위해 Api를 디자인 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-130">**Key principle:** Design APIs to be stable and to provide forward compatibility.</span></span>

- <span data-ttu-id="40b20-131">✅주요 변경이 필요할 때 기존 Api를 정상적 **으로 사용 중단.**</span><span class="sxs-lookup"><span data-stu-id="40b20-131">✅ **DO** deprecate old APIs gracefully when breaking changes are   required.</span></span>

- <span data-ttu-id="40b20-132">✅사용 중단 중에 기존 사용자 코드가 제대로 작동 하도록 허용 하는 "shim" 작업 및 함수 **를 제공 합니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-132">✅ **DO** provide "shim" operations and functions that allow   existing user code to operate correctly during deprecation.</span></span>

  <span data-ttu-id="40b20-133">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-133">*Examples:*</span></span>
  - <span data-ttu-id="40b20-134">로 호출 되는 작업의 이름을 바꾸면 `EstimateExpectation`   `EstimateAverage`   `EstimateExpectation` 기존 코드가 계속 제대로 작동할 수 있도록 새 이름으로 원래 작업을 호출 하는 라는 새 작업을 소개 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-134">When renaming an operation called `EstimateExpectation` to   `EstimateAverage`, introduce a new operation called   `EstimateExpectation` that calls the original operation at   its new name, so that existing code can continue to work   correctly.</span></span>

- <span data-ttu-id="40b20-135">✅**DO** 특성을 사용 @"microsoft.quantum.core.deprecated" 하 여 사용자에 게 결함를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-135">✅ **DO** use the @"microsoft.quantum.core.deprecated" attribute to communicate deprecations to the user.</span></span>

- <span data-ttu-id="40b20-136">✅ 작업 또는 함수의 이름을 바꿀 때에는에 **대 한 문자열** 입력으로 새 이름을 제공 `@Deprecated` 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-136">✅ When renaming an operation or function, **DO** provide the new   name as a string input to `@Deprecated`.</span></span>

- <span data-ttu-id="40b20-137">미리 보기 릴리스 기간을 6 개월 이상 사용 하지 않거나 지원 되는 릴리스에 대해 2 년 이상 사용 하지 않는 기존 함수 또는 작업은 제거 **하지 않습니다** . ⛔️</span><span class="sxs-lookup"><span data-stu-id="40b20-137">⛔️ **DON'T** remove existing functions or operations without a   deprecation period of at least six months for preview releases,   or at least two years for supported releases.</span></span>

## <a name="functions-and-operations"></a><span data-ttu-id="40b20-138">함수 및 작업</span><span class="sxs-lookup"><span data-stu-id="40b20-138">Functions and Operations</span></span>

<span data-ttu-id="40b20-139">**주요 원칙:** 모든 함수와 작업에 API 내에서 잘 정의 된 단일 용도가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-139">**Key principle:** ensure that every function and operation has a single well-defined purpose within the API.</span></span>

- <span data-ttu-id="40b20-140">관련 없는 여러 태스크를 수행 하는 함수 및 작업을 노출 **하지** ⛔️.</span><span class="sxs-lookup"><span data-stu-id="40b20-140">⛔️ **DON'T** expose functions and operations that perform multiple   unrelated tasks.</span></span>

<span data-ttu-id="40b20-141">**주요 원칙:** 함수 및 작업을 최대한 재사용 가능 하도록 디자인 하 고 향후의 요구를 예상 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-141">**Key principle:** design functions and operations to be as reusable as possible, and to anticipate future needs.</span></span>

- <span data-ttu-id="40b20-142">✅동일한 API와 이전에 존재 하는 라이브러리에서 다른 함수 및 작업과 함께 잘 구성 되도록 함수 및 작업 **을 디자인 합니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-142">✅ **DO** design functions and operations to compose well with other   functions and operations, both in the same API and in previously   existing libraries.</span></span>

  <span data-ttu-id="40b20-143">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-143">*Examples:*</span></span>
  - <span data-ttu-id="40b20-144">@"microsoft.quantum.canon.delay"작업은 해당 입력에 대 한 가정을 최소화 하므로 Q# 표준 라이브러리 전체에서 또는 사용자가 정의한 대로 두 작업의 응용 프로그램을 지연 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-144">The @"microsoft.quantum.canon.delay" operation makes minimal assumptions about its input, and thus can be used to delay applications of either operations across the Q# standard library or as defined by users.</span></span>
    <!-- TODO: define bad example. -->

- <span data-ttu-id="40b20-145">✅순수 하 게 결정적으로 **수행** 되는 모든 논리를 작업 대신 함수로 노출 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-145">✅ **DO** expose purely deterministic classical logic as   as functions rather than operations.</span></span>

  <span data-ttu-id="40b20-146">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-146">*Examples:*</span></span>
  - <span data-ttu-id="40b20-147">부동 소수점 입력을 제곱 하는 서브루틴은 명확 하 게 작성할 수 있으므로 작업이 아니라 사용자에 게 노출 되어야 합니다 `Squared : Double -> Double` `Square : Double => Double` .</span><span class="sxs-lookup"><span data-stu-id="40b20-147">A subroutine which squares its floating-point input can be written deterministically, and so should be exposed to the user as `Squared : Double -> Double` rather than as an operation `Square : Double => Double`.</span></span> <span data-ttu-id="40b20-148">이를 통해 더 많은 위치에서 서브루틴이 호출 될 수 있으며 (예: 다른 함수 내부) 성능 및 최적화에 영향을 줄 수 있는 유용한 최적화 정보를 컴파일러에 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-148">This allows for the subroutine to be called in more places (e.g.: inside of other functions), and provides useful optimization information to the compiler that can affect performance and optimizations.</span></span>
  - <span data-ttu-id="40b20-149">`ForEach<'TInput, 'TOutput>('TInput => 'TOutput, 'TInput[]) => 'TOutput[]` 및 `Mapped<'TInput, 'TOutput>('TInput -> 'TOutput, 'TInput[]) -> 'TOutput[]` 는 명확성을 고려 하 여 보장 됩니다. 두 가지 모두 다른 상황에서 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-149">`ForEach<'TInput, 'TOutput>('TInput => 'TOutput, 'TInput[]) => 'TOutput[]` and `Mapped<'TInput, 'TOutput>('TInput -> 'TOutput, 'TInput[]) -> 'TOutput[]` differ in the guarantees made with respect to   determinism; both are useful in different circumstances.</span></span>
  - <span data-ttu-id="40b20-150">퀀텀 작업의 응용 프로그램을 변환 하는 API 루틴은 결정적 방식으로 수행 될 수 있으므로와 같은 함수로 사용할 수 있습니다   `CControlled<'T>(op : 'T => Unit) => ((Bool, 'T) => Unit)` .</span><span class="sxs-lookup"><span data-stu-id="40b20-150">API routines that transform the application of quantum   operations can often be carried out in a deterministic     fashion and hence can be made available as functions such as   `CControlled<'T>(op : 'T => Unit) => ((Bool, 'T) => Unit)`.</span></span>

- <span data-ttu-id="40b20-151">✅필요에 따라 형식 매개 변수를 사용 하 여 각 함수 및 작업에 대 한 적절 한 입력 **형식을 일반화 합니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-151">✅ **DO** generalize the input type as much as reasonable for each   function and operation, using type parameters as needed.</span></span>

  <span data-ttu-id="40b20-152">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-152">*Examples:*</span></span>
  - <span data-ttu-id="40b20-153">`ApplyToEach` 에는 `<'T>(('T => Unit), 'T[]) => Unit` 가장 일반적인 응용 프로그램의 특정 형식이 아닌 형식이 `((Qubit => Unit), Qubit[]) => Unit` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-153">`ApplyToEach` has type `<'T>(('T => Unit), 'T[]) => Unit` rather than the specific type of its most common   application, `((Qubit => Unit), Qubit[]) => Unit`.</span></span>

> [!TIP]
> <span data-ttu-id="40b20-154">향후 요구 사항을 예상 하는 것이 중요 하지만 사용자에 대 한 구체적인 문제를 해결 하는 것도 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-154">It is important to anticipate future needs, but it is also important to solve concrete problems for your users.</span></span>
> <span data-ttu-id="40b20-155">따라서이 키 원칙을 사용 하는 경우 "just-in-time" Api 개발을 방지 하기 위해 항상 신중 하 게 고려 하 고 균형을 유지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-155">Acting on this key principle thus always requires careful consideration and balancing to avoid developing APIs "just in case."</span></span>

<span data-ttu-id="40b20-156">**주요 원칙:** 예측 가능 하 고 호출 가능의 용도를 전달 하는 함수 및 작업에 대 한 입력 및 출력 형식을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-156">**Key principle:** choose input and output types for functions and operations that are predictable, and that communicate the purpose of a callable.</span></span>

- <span data-ttu-id="40b20-157">✅튜플 **형식을 사용 하** 여 함께 간주할 때만 중요 한 입력 및 출력을 논리적으로 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-157">✅ **DO** use tuple types to logically group inputs and outputs that are only significant when considered together.</span></span> <span data-ttu-id="40b20-158">이러한 경우에는 사용자 정의 형식을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-158">Consider using a user-defined type in these cases.</span></span>

  <span data-ttu-id="40b20-159">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-159">*Examples:*</span></span>
  - <span data-ttu-id="40b20-160">다른 함수의 로컬 최소을 출력 하는 함수는 `LocalMinima(fn : (Double -> Double), (left : Double, right : Double)) : Double` 적절 한 서명이 될 수 있는 입력으로 검색 간격의 범위를 사용 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-160">A function to output the local minima of another function   may need to take bounds of a search interval as input, such   that `LocalMinima(fn : (Double -> Double), (left : Double, right : Double)) : Double` may be an appropriate signature.</span></span>
  - <span data-ttu-id="40b20-161">매개 변수 이동 기법을 사용 하 여 기계 학습 분류자의 파생을 예측 하는 작업은 이동 된 매개 변수 벡터와 이동 되지 않은 매개 변수 벡터를 입력으로 사용 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-161">An operation to estimate a derivative of a machine learning classifier using the parameter shift technique may need to take both the shifted and unshifted parameter vectors as inputs.</span></span> <span data-ttu-id="40b20-162">이 경우에는와 유사한 입력 `(unshifted : Double[], shifted : Double[])` 이 적합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-162">An input similar to `(unshifted : Double[], shifted : Double[])` may be appropriate in this case.</span></span>

- <span data-ttu-id="40b20-163">✅입력 및 출력 튜플의 항목을 다양 한 함수 및 작업에서 일관 되 **게 정렬 합니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-163">✅ **DO** order items in input and output tuples consistently   across different functions and operations.</span></span>

  <span data-ttu-id="40b20-164">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-164">*Examples:*</span></span>
  - <span data-ttu-id="40b20-165">각각 회전 각도와 대상 비트를 입력으로 사용 하는 두 개의 함수 또는 함수를 고려 하는 경우 각 입력 튜플에 동일한 순서로 정렬 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-165">If considering two or functions or operations that each take a rotation angle and a target qubit as inputs, ensure that they are ordered the same in each input tuple.</span></span> <span data-ttu-id="40b20-166">즉, 및를 사용 하는 것이 좋습니다 `ApplyRotation(angle : Double, target : Qubit) : Unit is Adj + Ctl` `DelayedRotation(angle : Double, target : Qubit) : (Unit => Unit is Adj + Ctl)` `ApplyRotation(target : Qubit, angle : Double) : Unit is Adj + Ctl` `DelayedRotation(angle : Double, target : Qubit) : (Unit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="40b20-166">That is, prefer `ApplyRotation(angle : Double, target : Qubit) : Unit is Adj + Ctl` and `DelayedRotation(angle : Double, target : Qubit) : (Unit => Unit is Adj + Ctl)` to `ApplyRotation(target : Qubit, angle : Double) : Unit is Adj + Ctl` and `DelayedRotation(angle : Double, target : Qubit) : (Unit => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="40b20-167">**주요 원칙:** 부분 응용 프로그램 등의 Q 언어 기능에서 잘 작동 하도록 함수 및 작업을 디자인 \# 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-167">**Key principle:** design functions and operations to work well with Q\# language features such as partial application.</span></span>

- <span data-ttu-id="40b20-168">✅가장 일반적으로 적용 되는 입력이 먼저 발생 하도록 (즉, 부분 응용 프로그램이 currying와 비슷하게 작동 하도록) 입력 튜플의 항목 **을 정렬 합니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-168">✅ **DO** order items in input tuples such that the most commonly   applied inputs occur first (i.e.: so that partial application   acts similarly to currying).</span></span>

  <span data-ttu-id="40b20-169">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-169">*Examples:*</span></span>
  - <span data-ttu-id="40b20-170">부동 소수점 `ApplyRotation` 숫자와 원하는 비트를 입력으로 사용 하는 연산은 형식의 입력을 필요로 하는 작업과 함께 사용 하기 위해 먼저 부동 소수점 입력에 부분적으로 적용 될 수 있습니다 `Qubit => Unit` .</span><span class="sxs-lookup"><span data-stu-id="40b20-170">An operation `ApplyRotation` that takes a floating-point number and a qubit as inputs may often be partially applied with the floating-point input first for use with operations that expect an input of type `Qubit => Unit`.</span></span> <span data-ttu-id="40b20-171">따라서 서명 된 `operation ApplyRotation(angle : Double, target : Qubit) : Unit is Adj + Ctl`</span><span class="sxs-lookup"><span data-stu-id="40b20-171">Thus, a signature of `operation ApplyRotation(angle : Double, target : Qubit) : Unit is Adj + Ctl`</span></span>
      <span data-ttu-id="40b20-172">는 부분 응용 프로그램에서 가장 일관 된 방식으로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-172">would work most consistently with partial application.</span></span>
  - <span data-ttu-id="40b20-173">일반적으로이 지침은 입력 튜플의 모든 모든 데이터를 앞에 배치 하는 것을 의미 하지만 좋은 결정을 사용 하 고 API가 실제로 호출 되는 방식을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-173">Typically, this guidance means placing all classical data   before all qubits in input tuples, but use good judgment and   examine how your API is called in practice.</span></span>

## <a name="user-defined-types"></a><span data-ttu-id="40b20-174">사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="40b20-174">User-Defined Types</span></span>

<span data-ttu-id="40b20-175">**주요 원칙:** 사용자 정의 형식을 사용 하 여 api를 더 쉽게 표현 하 고 편리 하 게 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-175">**Key principle:** use user-defined types to help make APIs more expressive and convenient to use.</span></span>

- <span data-ttu-id="40b20-176">✅Long 및/또는 복잡 한 형식에 대해 유용한 약어를 제공 하기 위해 새로운 사용자 정의 **형식을 도입 합니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-176">✅ **DO** introduce new user-defined types to provide helpful   shorthand for long and/or complicated types.</span></span>

  <span data-ttu-id="40b20-177">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-177">*Examples:*</span></span>
  - <span data-ttu-id="40b20-178">세 개의 비트율 비트 배열 입력을 포함 하는 작업 유형을 일반적으로 입력으로 사용 하거나 출력으로 반환 하는 경우와 같은 UDT를 제공 합니다. `newtype TimeDependentBlockEncoding = ((Qubit[], Qubit[], Qubit[]) => Unit is Adj + Ctl)`</span><span class="sxs-lookup"><span data-stu-id="40b20-178">In cases where an operation type with three qubit array inputs is commonly taken as an input or returned as an output, providing a UDT such as `newtype TimeDependentBlockEncoding = ((Qubit[], Qubit[], Qubit[]) => Unit is Adj + Ctl)`</span></span>
      <span data-ttu-id="40b20-179">는 유용한 약어를 제공 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-179">can help provide a useful shorthand.</span></span>

- <span data-ttu-id="40b20-180">✅지정 된 기본 형식이 매우 특정 한 의미 에서만 사용 되어야 함을 나타내기 위해 새 사용자 정의 **형식을 도입 합니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-180">✅ **DO** introduce new user-defined types to indicate that a given   base type should only be used in a very particular sense.</span></span>

  <span data-ttu-id="40b20-181">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-181">*Examples:*</span></span>
  - <span data-ttu-id="40b20-182">기존 데이터를 퀀텀 레지스터로 인코딩하는 작업으로 특별히 해석 해야 하는 작업은 사용자 정의 형식으로 레이블에 적합할 수 있습니다 `newtype InputEncoder = (Apply : (Qubit[] => Unit))` .</span><span class="sxs-lookup"><span data-stu-id="40b20-182">An operation that should be interpreted specifically as an   operation that encodes classical data into a quantum   register may be appropriate to label with a user-defined   type `newtype InputEncoder = (Apply : (Qubit[] => Unit))`.</span></span>

- <span data-ttu-id="40b20-183">✅이후 확장성을 허용 하는 명명 된 항목 (예: 앞으로 추가 명명 된 항목을 포함할 수 있는 결과 구조)을 포함 하는 새로운 사용자 정의 **형식을 도입 합니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-183">✅ **DO** introduce new user-defined types with named items that   allow for future extensibility (e.g.: a results structure that   may contain additional named items in the future).</span></span>

  <span data-ttu-id="40b20-184">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-184">*Examples:*</span></span>
  - <span data-ttu-id="40b20-185">작업에서 `TrainModel` 많은 구성 옵션을 노출 하는 경우 이러한 옵션을 새 udt로 노출 하   `TrainingOptions` 고 새 함수를 제공 하면   `DefaultTrainingOptions : Unit -> TrainingOptions` 라이브러리 개발자가 새 udt 항목을 적절 하 게 추가할 수 있도록 하는 동시에 TrainingOptions UDT 값의 특정 명명 된 항목을 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-185">When an operation `TrainModel` exposes a large number of   configuration options, exposing these options as a new   `TrainingOptions` UDT and providing a new function   `DefaultTrainingOptions : Unit -> TrainingOptions` allows   users to override specific named items in TrainingOptions   UDT values while still allowing library developers to add   new UDT items as appropriate.</span></span>

- <span data-ttu-id="40b20-186">✅사용자가 올바른 튜플 분해를 알아야 하는 기본 설정에서 새 사용자 정의 형식에 대해 명명 된 항목 **을 선언 합니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-186">✅ **DO** declare named items for new user-defined types in   preference to requiring users to know the correct tuple   deconstruction.</span></span>

  <span data-ttu-id="40b20-187">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-187">*Examples:*</span></span>
  - <span data-ttu-id="40b20-188">극좌표 형 분해에서 복소수를 나타낼 경우에는를 사용 하는 것이 좋습니다   `newtype ComplexPolar = (Magnitude: Double, Argument: Double)`   `newtype ComplexPolar = (Double, Double)` .</span><span class="sxs-lookup"><span data-stu-id="40b20-188">When representing a complex number in its polar   decomposition, prefer   `newtype ComplexPolar = (Magnitude: Double, Argument: Double)` to   `newtype ComplexPolar = (Double, Double)`.</span></span>

<span data-ttu-id="40b20-189">**주요 원칙:** 에서 사용자 정의 형식을 사용 하 여 인지 부하를 줄이고 사용자가 추가 개념 및 명명법을 배우지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-189">**Key principle:** use user-defined types in ways reduce  cognitive load and that don't require the user to learn additional concepts and nomenclature.</span></span>

- <span data-ttu-id="40b20-190">사용자가 래핑 연산자 ()를 자주 사용 하거나 래핑 해제의 여러 수준을 자주 필요로 하는 사용자 정의 형식을 도입 **하지 않습니다** `!` . ⛔️</span><span class="sxs-lookup"><span data-stu-id="40b20-190">⛔️ **DON'T** introduce user-defined types that require the user to make frequent use of the unwrap operator (`!`), or that commonly require multiple levels of unwrapping.</span></span> <span data-ttu-id="40b20-191">가능한 완화 전략은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-191">Possible mitigation strategies include:</span></span>

  - <span data-ttu-id="40b20-192">단일 항목으로 사용자 정의 형식을 노출 하는 경우 해당 항목의 이름을 정의 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-192">When exposing a user-defined type with a single item, consider defining a name for that item.</span></span> <span data-ttu-id="40b20-193">예를 들어 `newtype Encoder = (Apply : (Qubit[] => Unit is Adj + Ctl))` 를로 설정 하는 것이 좋습니다 `newtype Encoder = (Qubit[] => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="40b20-193">For instance, consider `newtype Encoder = (Apply : (Qubit[] => Unit is Adj + Ctl))` in preference to `newtype Encoder = (Qubit[] => Unit is Adj + Ctl)`.</span></span>

  - <span data-ttu-id="40b20-194">다른 함수 및 작업이 "래핑된" UDT 인스턴스를 직접 수락할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-194">Ensuring that other functions and operations can accept   "wrapped" UDT instances directly.</span></span>

- <span data-ttu-id="40b20-195">⛔️는 추가 표현을를 제공 하지 않고 기본 제공 형식이 중복 되는 새로운 사용자 정의 형식을 도입 **하지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-195">⛔️ **DON'T** introduce new user-defined types that duplicate   built-in types without providing additional expressiveness.</span></span>

  <span data-ttu-id="40b20-196">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-196">*Examples:*</span></span>
  - <span data-ttu-id="40b20-197">UDT는 `newtype QubitRegister = Qubit[]` 추가 표현을를 제공 하지 않으며 `Qubit[]` , 따라서 띄는 혜택 없이 사용 하기 어려워집니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-197">A UDT `newtype QubitRegister = Qubit[]` provides no   additional expressiveness over `Qubit[]`, and is thus harder   to use with no discernable benefit.</span></span>
  - <span data-ttu-id="40b20-198">UDT는 기본 `newtype LittleEndian = Qubit[]` 레지스터를 사용 하 고 해석 하는 방법을 문서화 하므로 기본 형식에 대 한 추가 표현을을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-198">A UDT `newtype LittleEndian = Qubit[]` documents how the   underlying register is to be used and interpreted, and thus   provides additional expressiveness over its base type.</span></span>

- <span data-ttu-id="40b20-199">반드시 필요한 경우가 아니면 접근자 함수 **를 도입할 ⛔️** .   이 경우 명명 된 항목을 강력 하 게 선호 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-199">⛔️ **DON'T** introduce accessor functions unless strictly required;   strongly prefer named items in this case.</span></span>

  <span data-ttu-id="40b20-200">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-200">*Examples:*</span></span>
  - <span data-ttu-id="40b20-201">UDT를 도입할 때 `newtype Complex = (Double, Double)`   `newtype Complex = (Real : Double, Imag : Double)` 함수 및를 도입 하기 위해 정의를 수정 하는 것을 선호 합니다 `GetReal : Complex -> Double`   `GetImag : Complex -> Double` .</span><span class="sxs-lookup"><span data-stu-id="40b20-201">When introducing a UDT `newtype Complex = (Double, Double)`,   prefer modifying the definition to   `newtype Complex = (Real : Double, Imag : Double)` to introducing   functions `GetReal : Complex -> Double` and   `GetImag : Complex -> Double`.</span></span>

## <a name="namespaces-and-organization"></a><span data-ttu-id="40b20-202">네임 스페이스 및 조직</span><span class="sxs-lookup"><span data-stu-id="40b20-202">Namespaces and Organization</span></span>

<span data-ttu-id="40b20-203">**주요 원칙:** 예측 가능 하 고 각 네임 스페이스의 함수, 작업 및 사용자 정의 형식에 대 한 용도를 명확 하 게 전달 하는 네임 스페이스 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-203">**Key principle:** choose namespace names that are predictable and that clearly communicate the purpose of functions, operations, and user-defined types in each namespace.</span></span>

- <span data-ttu-id="40b20-204">✅네임 **스페이스 이름을** 로 `Publisher.Product.DomainArea` 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-204">✅ **DO** name namespaces as `Publisher.Product.DomainArea`.</span></span>

  <span data-ttu-id="40b20-205">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-205">*Examples:*</span></span>
  - <span data-ttu-id="40b20-206">Microsoft에서 퀀텀 개발 키트의 퀀텀 시뮬레이션 기능의 일부로 게시 한 함수, 작업 및 Udt는 네임 스페이스에 배치 됩니다   `Microsoft.Quantum.Simulation` .</span><span class="sxs-lookup"><span data-stu-id="40b20-206">Functions, operations, and UDTs published by Microsoft as a   part of the quantum simulation feature of the Quantum   Development Kit are placed in the   `Microsoft.Quantum.Simulation` namespace.</span></span>
  - <span data-ttu-id="40b20-207">`Microsoft.Quantum.Math` Microsoft에서 수학 도메인 영역과 관련 된 퀀텀 개발 키트의 일부로 게시 한 네임 스페이스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-207">`Microsoft.Quantum.Math` represents a namespace   published by Microsoft as part of the Quantum Development   Kit pertaining to the mathematics domain area.</span></span>

- <span data-ttu-id="40b20-208">✅특정 기능에 사용 되는 작업, 함수 및 사용자 정의 형식을 해당 기능을 설명 하는 네임 스페이스 **에 추가 하** 여 해당 기능이 여러 문제 도메인에서 사용 되는 경우에도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-208">✅ **DO** place operations, functions, and user-defined types used   for specific functionality into a namespace that describes that   functionality, even when that functionality is used across   different problem domains.</span></span>

  <span data-ttu-id="40b20-209">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-209">*Examples:*</span></span>
  - <span data-ttu-id="40b20-210">Microsoft에서 퀀텀 개발 키트의 일부로 게시 한 상태 준비 Api는에 배치 됩니다   `Microsoft.Quantum.Preparation` .</span><span class="sxs-lookup"><span data-stu-id="40b20-210">State preparation APIs published by Microsoft as a part of   the Quantum Development Kit would be placed into   `Microsoft.Quantum.Preparation`.</span></span>
  - <span data-ttu-id="40b20-211">Microsoft에서 퀀텀 개발 키트의 일부로 게시 한 퀀텀 시뮬레이션 Api는에 배치 됩니다   `Microsoft.Quantum.Simulation` .</span><span class="sxs-lookup"><span data-stu-id="40b20-211">Quantum simulation APIs published by Microsoft as a part of the Quantum   Development Kit would be placed into   `Microsoft.Quantum.Simulation`.</span></span>

- <span data-ttu-id="40b20-212">✅특정 도메인 내 에서만 사용 되는 작업, 함수 및 사용자 정의 형식을 유틸리티의 도메인을 나타내는 네임 **스페이스로 추가 합니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-212">✅ **DO** place operations, functions, and user-defined types used only within specific domains into namespaces indicating their domain of utility.</span></span> <span data-ttu-id="40b20-213">필요한 경우 네임 스페이스를 사용 하 여 각 도메인별 네임 스페이스 내에서 포커스가 있는 작업을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-213">If needed, use subnamespaces to indicate focused tasks within each domain-specific namespace.</span></span>

  <span data-ttu-id="40b20-214">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-214">*Examples:*</span></span>
  - <span data-ttu-id="40b20-215">Microsoft에서 게시 하는 퀀텀 기계 학습 라이브러리는 대부분 @"microsoft.quantum.machinelearning" 네임 스페이스에 저장 되지만 네임 스페이스는 예제 데이터 집합을 제공 합니다 @"microsoft.quantum.machinelearning.datasets"   .</span><span class="sxs-lookup"><span data-stu-id="40b20-215">The quantum machine learning library published by Microsoft is largely   placed into the @"microsoft.quantum.machinelearning" namespace, but example   datasets are provided by the @"microsoft.quantum.machinelearning.datasets"   namespace.</span></span>
  - <span data-ttu-id="40b20-216">Microsoft에서 퀀텀 개발 키트의 일부로 게시 한 퀀텀 화학 Api는에 배치 해야 `Microsoft.Quantum.Chemistry` 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-216">Quantum chemistry APIs published by Microsoft as a part of the Quantum Development Kit should be placed into `Microsoft.Quantum.Chemistry`.</span></span> <span data-ttu-id="40b20-217">Wigner 분해 구현과 관련 된 기능을에 배치 하 여 `Microsoft.Quantum.Chemistry.JordanWigner` 퀀텀 화학 도메인 영역에 대 한 기본 인터페이스가 구현과 관련 되지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-217">Functionality specific to implementing the Jordan--Wigner decomposition may be placed in `Microsoft.Quantum.Chemistry.JordanWigner`, so that the primary interface for the quantum chemistry domain area is not concerned with implementations.</span></span>

<span data-ttu-id="40b20-218">**주요 원칙:** 네임 스페이스와 액세스 한정자를 함께 사용 하 여 사용자에 게 노출 되는 API 노출에 대해 의도적인 다음 Api의 구현 및 테스트와 관련 된 내부 세부 정보를 숨깁니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-218">**Key principle:** Use namespaces and access modifiers together to be intentional about the API surface exposed to users, and to hide internal details related to implementation and testing of your APIs.</span></span>

- <span data-ttu-id="40b20-219">✅ 적절 한 경우 **에는** api를 구현 하는 데 필요한 모든 함수 및 작업을 구현 하는 api와 동일한 네임 스페이스에 저장 하지만 "private" 또는 "internal" 키워드로 표시 하 여 라이브러리에 대 한 공용 api 표면의 일부가 아님을 나타내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-219">✅ Whenever reasonable, **DO** place all functions and operations needed to implement an API into the same namespace as the API being implemented, but marked with the "private" or "internal" keywords to indicate that they are not part of the public API surface for a library.</span></span> <span data-ttu-id="40b20-220">밑줄 ()로 시작 하는 이름을 사용 `_` 하 여 전용 및 내부 작업과 공용 callables의 함수를 시각적으로 구분할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-220">Use a name beginning with an underscore (`_`) to visually distinguish private and internal operations and functions from public callables.</span></span>

  <span data-ttu-id="40b20-221">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-221">*Examples:*</span></span>
  - <span data-ttu-id="40b20-222">작업 이름은 `_Features` 지정 된 네임 스페이스와 어셈블리에 대 한 전용 함수를 나타내며 키워드와 함께 제공 되어야 합니다 `internal` .</span><span class="sxs-lookup"><span data-stu-id="40b20-222">The operation name `_Features` indicates a function that is   private to a given namespace and assembly, and should be   accompanied by either the `internal` keyword.</span></span>

- <span data-ttu-id="40b20-223">✅ 드물지만 지정 된 네임 스페이스에 대 한 **API를 구현** 하기 위해 광범위 한 전용 함수 또는 작업 집합이 필요한 경우에는 구현 하 고 끝나는 네임 스페이스와 일치 하는 새 네임 스페이스에 저장 `.Private` 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-223">✅ In the rare case that an extensive set of private functions or operations are needed to implement the API for a given namespace, **DO** place them in a new namespace matching the namespace being implemented and ending in `.Private`.</span></span>

- <span data-ttu-id="40b20-224">✅모든 단위 테스트를 테스트 중인 네임 스페이스와 일치 하는 네임 스페이스 **에 저장 하** 고 종료 `.Tests` 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-224">✅ **DO** place all unit tests into namespaces matching the     namespace under test and ending in `.Tests`.</span></span>

## <a name="naming-conventions-and-vocabulary"></a><span data-ttu-id="40b20-225">명명 규칙 및 어휘</span><span class="sxs-lookup"><span data-stu-id="40b20-225">Naming Conventions and Vocabulary</span></span>

<span data-ttu-id="40b20-226">**주요 원칙:** 퀀텀 초보자 및 전문가를 비롯 하 여 다양 한 대상에서 명확 하 고, 액세스 가능 하며, 읽을 수 있는 이름 및 용어를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-226">**Key principle:** Choose names and terminology that are clear, accessible, and readable across a diverse range of audiences, including both quantum novices and experts.</span></span>

- <span data-ttu-id="40b20-227">차별적인 또는 exclusionary 식별자 이름과 API 문서 주석에는 용어를 사용 **하지 않습니다** . ⛔️</span><span class="sxs-lookup"><span data-stu-id="40b20-227">⛔️ **DON'T** use discriminatory or exclusionary identifier names,   nor terminology in API documentation comments.</span></span>

- <span data-ttu-id="40b20-228">✅API 문서 **주석을 사용 하 여 관련** 컨텍스트, 예제 및 참조를 제공할 수 있습니다. 특히 더 어려운 개념을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-228">✅ **DO** use API documentation comments to provide relevant   context, examples, and references, especially for more difficult   concepts.</span></span>

- <span data-ttu-id="40b20-229">불필요 하 게 까다로운 식별자 이름을 사용 하지 않거나 중요 한 퀀텀 알고리즘 정보를 읽는 데 필요한 식별자 이름을 사용 **하지** ⛔️ 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-229">⛔️ **DON'T** use identifier names that are unnecessarily esoteric,   or that require significant quantum algorithms knowledge to   read.</span></span>

  <span data-ttu-id="40b20-230">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-230">*Examples:*</span></span>
  - <span data-ttu-id="40b20-231">"Grover 반복"에 "진폭 증폭 반복"을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-231">Prefer "amplitude amplification iteration" to "Grover   iteration."</span></span>

- <span data-ttu-id="40b20-232">✅호출을 구현 하는 것이 아니라 호출 가능 여부를 명확 하 게 전달 하는 작업 및 함수 **이름을 선택 합니다** .</span><span class="sxs-lookup"><span data-stu-id="40b20-232">✅ **DO** choose operations and function names that clearly communicate the intended effect of a callable, and not its implementation.</span></span> <span data-ttu-id="40b20-233">구현은 [API 문서 주석에](xref:microsoft.quantum.qsharp.comments#documentation-comments)설명 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-233">Note that the implementation can and should be documented in [API documentation comments](xref:microsoft.quantum.qsharp.comments#documentation-comments).</span></span>

  <span data-ttu-id="40b20-234">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-234">*Examples:*</span></span>
  - <span data-ttu-id="40b20-235">후자가 이전에 구현 되는 방식을 전달 하므로 "Hadamard test"에 "예상 겹치기"를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-235">Prefer "estimate overlap" to "Hadamard test," as the latter   communicates how the former is implemented.</span></span>

- <span data-ttu-id="40b20-236">✅모든 Q api에서 일관 된 방식으로 단어 **를 사용 합니다** \# .</span><span class="sxs-lookup"><span data-stu-id="40b20-236">✅ **DO** use words in a consistent fashion across all Q\# APIs:</span></span>

  - <span data-ttu-id="40b20-237">**동사의**</span><span class="sxs-lookup"><span data-stu-id="40b20-237">**Verbs:**</span></span>

    - <span data-ttu-id="40b20-238">**Assert**: 물리적 리소스를 사용 하 여 대상 컴퓨터와 해당 비트의 상태에 대 한 가정이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-238">**Assert**: Check that an assumption about the state of a target machine and its qubits holds, possibly by using unphysical resources.</span></span> <span data-ttu-id="40b20-239">이 동사를 사용 하는 작업은 라이브러리 및 실행 프로그램의 기능에 영향을 주지 않고 항상 안전 하 게 제거 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-239">Operations using this verb should always be safely removable without affecting the functionality of libraries and executable programs.</span></span> <span data-ttu-id="40b20-240">팩트와 달리 어설션은 일반적으로의 상태 (예: 표준), 실행 환경 등의 외부 상태에 따라 달라질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-240">Note that unlike facts, assertions may, in general, depend on external state, such as the state of a qubit register, the run environment or so forth.</span></span> <span data-ttu-id="40b20-241">외부 상태에 대 한 종속성은 일종의 부작용 이므로 어설션이 함수 대신 작업으로 노출 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-241">As dependency on external state is a kind of side effect, assertions must be exposed as operations rather than functions.</span></span>

    - <span data-ttu-id="40b20-242">**예상**: 하나 이상의 반복 되는 측정값을 사용 하 여 측정 결과에서 기존 수량을 예측 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-242">**Estimate**: Using one or more possibly repeated   measurements, estimate a classical quantity from   measurement results.</span></span>

      <span data-ttu-id="40b20-243">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-243">*Examples:*</span></span>
      - @"microsoft.quantum.characterization.estimatefrequency"
      - @"microsoft.quantum.characterization.estimateoverlapbetweenstates"

    - <span data-ttu-id="40b20-244">**준비**: 특정 초기 상태 (일반적으로 $ \ket{00\cdots 0} $)에서 시작 하 여 해당 하는 작업의 상태를 원하는 끝 상태로 전환 하는 데 퀀텀 작업 또는 일련의 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-244">**Prepare**: Apply a quantum operation or sequence of operations to one or more qubits assumed to start in a particular initial state (typically $\ket{00\cdots 0}$), causing the state of those qubits to evolve to a desired end state.</span></span> <span data-ttu-id="40b20-245">일반적으로 지정 된 시작 상태를 제외 하 고 상태에 대해 작업을 수행 하면 정의 되지 않은 단일 변환이 발생할 **수** 있지만 작업 및 해당 adjoint "취소"를 유지 하 고 작업을 적용 하지 **않아야** 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-245">In general, acting on states other than the given starting state **MAY** result in an undefined unitary transformation, but **SHOULD** still preserve that an operation and its adjoint "cancel out" and apply a no-op.</span></span>

      <span data-ttu-id="40b20-246">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-246">*Examples:*</span></span>
      - @"microsoft.quantum.preparation.preparearbitrarystate"
      - @"microsoft.quantum.preparation.prepareuniformsuperposition"

    - <span data-ttu-id="40b20-247">**Measure**: 하나 이상의 이상에 퀀텀 작업 또는 일련의 작업을 적용 하 여 기존 데이터를 다시 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-247">**Measure**: Apply a quantum operation or sequence of   operations to one or more qubits, reading classical data   back out.</span></span>

      <span data-ttu-id="40b20-248">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-248">*Examples:*</span></span>
      - @"Microsoft.Quantum.Intrinsic.Measure"
      - @"microsoft.quantum.arithmetic.measurefxp"
      - @"microsoft.quantum.arithmetic.measureinteger"

    - <span data-ttu-id="40b20-249">**적용**: 하나 이상의 이상에 퀀텀 작업 또는 일련의 작업을 적용 하 여 해당 하는 비트의 상태를 일관 된 방식으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-249">**Apply**: Apply a quantum operation or sequence of operations to one or more qubits, causing the state of those qubits to change in a coherent fashion.</span></span> <span data-ttu-id="40b20-250">이 동사는 Q 명명법에서 가장 일반적 \# 으로 사용 되는 **동사 이며** 보다 구체적인 동사가 더 직접적으로 관련 된 경우에는 사용 하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-250">This verb is the most general verb in Q\# nomenclature, and **SHOULD NOT BE** used when a more specific verb is more directly relevant.</span></span>

  - <span data-ttu-id="40b20-251">**명사**:</span><span class="sxs-lookup"><span data-stu-id="40b20-251">**Nouns**:</span></span>

    - <span data-ttu-id="40b20-252">**팩트**: 대상 컴퓨터의 상태, 해당 환경 또는 컴퓨터의 기능에 대 한 상태가 아닌 입력에만 의존 하는 부울 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-252">**Fact**: A Boolean condition which depends only on its inputs and not on the state of a target machine, its environment, or the state of the machine's qubits.</span></span> <span data-ttu-id="40b20-253">어설션과 달리 팩트는 해당 팩트에 제공 되는 *값* 만을 인식 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-253">By contrast with an assertion, a fact is only sensitive to the *values* provided to that fact.</span></span> <span data-ttu-id="40b20-254">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="40b20-254">For example:</span></span>

      <span data-ttu-id="40b20-255">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-255">*Examples:*</span></span>
      - <span data-ttu-id="40b20-256">@"microsoft.quantum.diagnostics.equalityfacti": 두 정수 입력에 대 한 같음 팩트를 나타냅니다. 입력으로 제공 된 정수는 서로 같거나 다른 프로그램 상태와는 독립적입니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-256">@"microsoft.quantum.diagnostics.equalityfacti": represents an equality fact about two integer inputs; either the integers provided as input are equal to each other, or they are not, independent of any other program state.</span></span>

    - <span data-ttu-id="40b20-257">**옵션:** 함수 또는 작업에 대해 "선택적 인수"로 작동할 수 있는 여러 개의 명명 된 항목이 포함 된 UDT입니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-257">**Options:** A UDT containing several named items that can act as "optional arguments" to a function or operation.</span></span> <span data-ttu-id="40b20-258">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="40b20-258">For example:</span></span>

      <span data-ttu-id="40b20-259">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-259">*Examples:*</span></span>
      - <span data-ttu-id="40b20-260">UDT에는 @"microsoft.quantum.machinelearning.trainingoptions" 학습 률, 미니 배치 크기 및 ML 학습을 위한 구성 가능한 기타 매개 변수에 대 한 명명 된 항목이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-260">The @"microsoft.quantum.machinelearning.trainingoptions" UDT includes named items for learning rate, minibatch size, and other configurable parameters for ML training.</span></span>

  - <span data-ttu-id="40b20-261">**형용사**:</span><span class="sxs-lookup"><span data-stu-id="40b20-261">**Adjectives**:</span></span>

    - <span data-ttu-id="40b20-262">⛔️ **New**: 많은 프로그래밍 언어 (예: c + +, c #, Java, TypeScript, PowerShell)에서 동사로 사용 되는 혼동을 방지 하기 위해이 형용사를 사용 하면 **안 됩니다.**</span><span class="sxs-lookup"><span data-stu-id="40b20-262">⛔️ **New**: This adjective **SHOULD NOT** be used, as to avoid confusion   with its usage as a verb in many   programming languages (e.g.: C++, C#, Java, TypeScript, PowerShell).</span></span>

  - <span data-ttu-id="40b20-263">**전치사:** 경우에 따라 전치사를 사용 하 여 함수 및 작업 이름에서 명사와 동사의 역할을 보다 명확 하 게 구분 하거나 명확 하 게 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-263">**Prepositions:** In some cases, prepositions can be used to further disambiguate or clarify the roles of nouns and verbs in function and operation names.</span></span> <span data-ttu-id="40b20-264">그러나 신중 하 고 일관 된 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-264">Care should be taken to do so sparingly and consistently, however.</span></span>

    - <span data-ttu-id="40b20-265">**As:** 함수의 입력 및 출력이 동일한 정보를 나타내지만 출력은 해당 정보를 원래 표현이 아닌 *X* **로** 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-265">**As:** Represents that a function's input and output represent the same information, but that the output represents that information **as** an *X* instead of its original representation.</span></span> <span data-ttu-id="40b20-266">이는 형식 변환 함수에 특히 일반적입니다.</span><span class="sxs-lookup"><span data-stu-id="40b20-266">This is especially common for type conversion functions.</span></span>

      <span data-ttu-id="40b20-267">*예:*</span><span class="sxs-lookup"><span data-stu-id="40b20-267">*Examples:*</span></span>
      - <span data-ttu-id="40b20-268">`IntAsDouble(2)` 입력 ( `2` )과 출력 ()이 모두 `2.0` 동일한 정보를 나타내지만 다른 Q 데이터 형식을 사용 하 여 qualitatively 나타냅니다 \# .</span><span class="sxs-lookup"><span data-stu-id="40b20-268">`IntAsDouble(2)` indicates that both the input (`2`) and the output (`2.0`)   represent qualitatively the same information, but using   different Q\# data types to do so.</span></span>

    - <span data-ttu-id="40b20-269">**시작:** 일관성을 유지 하기 위해이 **전치사를** 사용 하 여 형식 변환 함수 또는 다른 모든 경우를 사용 하면 안 **됩니다.**</span><span class="sxs-lookup"><span data-stu-id="40b20-269">**From:** To ensure consistency, this preposition   **SHOULD NOT** be used to indicate type conversion   functions or any other case where **As** is appropriate.</span></span>

    - <span data-ttu-id="40b20-270">⛔️ **:** 이 전치사는 많은 프로그래밍 언어의 동사로 사용과 혼동 하지 않도록 하기 위해 사용해 서는 **안 됩니다.**</span><span class="sxs-lookup"><span data-stu-id="40b20-270">⛔️ **To:** This preposition **SHOULD NOT** be used, as to   avoid confusion with its usage as a verb in many   programming languages.</span></span>
