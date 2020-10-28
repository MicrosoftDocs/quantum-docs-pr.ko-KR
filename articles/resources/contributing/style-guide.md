---
title: 'Microsoft :::no-loc(Q#)::: 스타일 가이드'
description: '프로그램 및 라이브러리에 대 한 이름 지정, 입력, 설명서 및 서식 규칙에 대해 알아봅니다 :::no-loc(Q#)::: .'
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.style
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: 7666974e255d537c8d611d0077b7f9b37a61f918
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691742"
---
# <a name="no-locq-style-guide"></a><span data-ttu-id="a5fa6-103">:::no-loc(Q#)::: 스타일 안내선</span><span class="sxs-lookup"><span data-stu-id="a5fa6-103">:::no-loc(Q#)::: Style Guide</span></span> #
## <a name="general-conventions"></a><span data-ttu-id="a5fa6-104">일반 규칙</span><span class="sxs-lookup"><span data-stu-id="a5fa6-104">General Conventions</span></span> ##

<span data-ttu-id="a5fa6-105">이 가이드에서 제안 하는 규칙은 쉽게 읽고 이해할 수 있도록 작성 된 프로그램 및 라이브러리를 만드는 데 도움을 주기 위한 것 :::no-loc(Q#)::: 입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-105">The conventions suggested in this guide are intended to help make programs and libraries written in :::no-loc(Q#)::: easier to read and understand.</span></span>

## <a name="guidance"></a><span data-ttu-id="a5fa6-106">지침</span><span class="sxs-lookup"><span data-stu-id="a5fa6-106">Guidance</span></span>

<span data-ttu-id="a5fa6-107">다음을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-107">We suggest:</span></span>

- <span data-ttu-id="a5fa6-108">사용자에 게 더 읽기 쉽고 이해 하기 쉬운 코드를 제공 하기 위해 의도적으로 수행 하는 경우가 아니면 규칙을 무시 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-108">Never disregard a convention unless you’re doing so intentionally in order to provide more readable and understandable code for your users.</span></span>

## <a name="naming-conventions"></a><span data-ttu-id="a5fa6-109">명명 규칙</span><span class="sxs-lookup"><span data-stu-id="a5fa6-109">Naming Conventions</span></span> ##

<span data-ttu-id="a5fa6-110">퀀텀 개발 키트를 제공할 때 퀀텀 개발자가 쉽게 읽을 수 있는 프로그램을 작성 하는 데 도움이 되는 함수 및 작업 이름에 대해 노력 하 고 있으며이를 최소화 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-110">In offering the Quantum Development Kit, we strive for function and operation names that help quantum developers write programs that are easy to read and that minimize surprise.</span></span>
<span data-ttu-id="a5fa6-111">의 중요 한 부분은 함수, 작업 및 형식에 대 한 이름을 선택할 때 프로그래머가 퀀텀 개념을 표현 하는 데 사용 하는 *어휘* 를 설정 하는 것입니다. 이 옵션을 사용 하면 명확 하 게 통신할 수 있도록 도와 드릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-111">An important part of that is that when we choose names for functions, operations, and types, we are establishing the *vocabulary* that programmers use to express quantum concepts; with our choices, we either help or hinder them in their effort to clearly communicate.</span></span>
<span data-ttu-id="a5fa6-112">이는 도입 된 이름이 은둔 대신 명확성을 제공 하는지 확인 하는 책임을 집니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-112">This places a responsibility on us to make sure that the names we introduce offer clarity rather than obscurity.</span></span>
<span data-ttu-id="a5fa6-113">이 섹션에서는 개발 커뮤니티에서 가장 잘 활용 하는 데 도움이 되는 명시적 지침을 기준으로이 의무를 어떻게 충족 하는지 자세히 설명 :::no-loc(Q#)::: 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-113">In this section, we detail how we meet this obligation in terms of explicit guidance that helps us do the best by the :::no-loc(Q#)::: development community.</span></span>

### <a name="operations-and-functions"></a><span data-ttu-id="a5fa6-114">작업 및 함수</span><span class="sxs-lookup"><span data-stu-id="a5fa6-114">Operations and Functions</span></span> ###

<span data-ttu-id="a5fa6-115">이름을 설정 해야 하는 첫 번째 작업 중 하나는 지정 된 기호가 함수 또는 작업을 나타내는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-115">One of the first things that a name should establish is whether a given symbol represents a function or an operation.</span></span>
<span data-ttu-id="a5fa6-116">함수 및 작업 간의 차이점은 코드 블록이 동작 하는 방식을 이해 하는 데 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-116">The difference between functions and operations is critical to understanding how a block of code behaves.</span></span>
<span data-ttu-id="a5fa6-117">함수와 작업을 사용자에 게 구분 하기 위해 의도 하지 않은 :::no-loc(Q#)::: 결과를 사용 하 여 퀀텀 작업을 모델링 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-117">To communicate the distinction between functions and operations to users, we rely on that :::no-loc(Q#)::: models quantum operations through the use of side effects.</span></span>
<span data-ttu-id="a5fa6-118">즉, 작업은 어떤 작업을 *수행* 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-118">That is, an operation *does* something.</span></span>

<span data-ttu-id="a5fa6-119">이와 대조적으로 함수는 데이터 간의 수학적 관계를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-119">By contrast, functions describe the mathematical relationships between data.</span></span>
<span data-ttu-id="a5fa6-120">식은 이며 `Sin(PI() / 2.0)` *is* `1.0` 프로그램이 나 그 이상 비트의 상태에 대해서는 아무 것도 의미 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-120">The expression `Sin(PI() / 2.0)` *is* `1.0`, and implies nothing about the state of a program or its qubits.</span></span>

<span data-ttu-id="a5fa6-121">요약 하면 함수는 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-121">Summarizing, operations do things while functions are things.</span></span>
<span data-ttu-id="a5fa6-122">이러한 구분은 작업을 명사로 서 동사와 함수로 이름을 지정할 것을 제안 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-122">This distinction suggests that we name operations as verbs and functions as nouns.</span></span>

> [!NOTE]
> <span data-ttu-id="a5fa6-123">사용자 정의 형식이 선언 되 면 해당 형식의 인스턴스를 생성 하는 새 함수가 암시적으로 동시에 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-123">When a user-defined type is declared, a new function that constructs instances of that type is implicitly defined at the same time.</span></span>
> <span data-ttu-id="a5fa6-124">이러한 관점에서 사용자 정의 형식은 형식 자체와 생성자 함수에 일관 된 이름을 갖도록 명사로 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-124">From that perspective, user-defined types should be named as nouns so that both the type itself and the constructor function have consistent names.</span></span>

<span data-ttu-id="a5fa6-125">적절 한 경우 작업 이름이 작업에서 수행한 효과를 명확 하 게 나타내는 동사로 시작 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-125">Where reasonable, ensure that operation names begin with verbs that clearly indicate the effect taken by the operation.</span></span>
<span data-ttu-id="a5fa6-126">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-126">For example:</span></span>

- `MeasureInteger`
- `EstimateEnergy`
- `SampleInt`

<span data-ttu-id="a5fa6-127">특별 한 언급할 만한 사례는 작업이 다른 작업을 입력으로 사용 하 고 호출 하는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-127">One case that deserves special mention is when an operation takes another operation as input and calls it.</span></span>
<span data-ttu-id="a5fa6-128">이러한 경우에는 외부 작업이 정의 될 때 입력 작업에서 수행 하는 동작이 명확 하지 않으므로 오른쪽 동사가 명확 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-128">In such cases, the action taken by the input operation is not clear when the outer operation is defined, such that the right verb is not immediately clear.</span></span>
<span data-ttu-id="a5fa6-129">`Apply`, 및에서와 같이 동사를 권장 합니다 `ApplyIf` `ApplyToEach` `ApplyToFirst` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-129">We recommend the verb `Apply`, as in `ApplyIf`, `ApplyToEach`, and `ApplyToFirst`.</span></span>
<span data-ttu-id="a5fa6-130">다른 동사는이 경우에도 유용 하 게 사용할 수 있습니다 `IterateThroughCartesianPower` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-130">Other verbs may be useful in this case as well, as in `IterateThroughCartesianPower`.</span></span>

| <span data-ttu-id="a5fa6-131">동사</span><span class="sxs-lookup"><span data-stu-id="a5fa6-131">Verb</span></span> | <span data-ttu-id="a5fa6-132">예상 효과</span><span class="sxs-lookup"><span data-stu-id="a5fa6-132">Expected Effect</span></span> |
| ---- | ------ |
| <span data-ttu-id="a5fa6-133">적용</span><span class="sxs-lookup"><span data-stu-id="a5fa6-133">Apply</span></span> | <span data-ttu-id="a5fa6-134">입력으로 제공 된 작업을 라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-134">An operation provided as input is called</span></span> |
| <span data-ttu-id="a5fa6-135">Assert</span><span class="sxs-lookup"><span data-stu-id="a5fa6-135">Assert</span></span> | <span data-ttu-id="a5fa6-136">가능한 퀀텀 측정의 결과에 대 한 가설은 시뮬레이터에 의해 확인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-136">A hypothesis about the outcome of a possible quantum measurement is checked by a simulator</span></span> |
| <span data-ttu-id="a5fa6-137">예측값</span><span class="sxs-lookup"><span data-stu-id="a5fa6-137">Estimate</span></span> | <span data-ttu-id="a5fa6-138">하나 이상의 측정값 으로부터 그려진 추정치를 나타내는 고전 값이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-138">A classical value is returned, representing an estimate drawn from one or more measurements</span></span> |
| <span data-ttu-id="a5fa6-139">측정값</span><span class="sxs-lookup"><span data-stu-id="a5fa6-139">Measure</span></span> | <span data-ttu-id="a5fa6-140">퀀텀 측정이 수행 되며 결과가 사용자에 게 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-140">A quantum measurement is performed, and its result is returned to the user</span></span> |
| <span data-ttu-id="a5fa6-141">준비</span><span class="sxs-lookup"><span data-stu-id="a5fa6-141">Prepare</span></span> | <span data-ttu-id="a5fa6-142">지정 된 비트 레지스터가 특정 상태로 초기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-142">A given register of qubits is initialized into a particular state</span></span> |
| <span data-ttu-id="a5fa6-143">샘플</span><span class="sxs-lookup"><span data-stu-id="a5fa6-143">Sample</span></span> | <span data-ttu-id="a5fa6-144">일부 분포에서 무작위로 값이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-144">A classical value is returned at random from some distribution</span></span> |

<span data-ttu-id="a5fa6-145">함수의 경우 일반적인 명사를 선호 하는 동사를 사용 하지 않는 것이 좋습니다 (아래의 적절 한 명사에 대 한 지침 참조).</span><span class="sxs-lookup"><span data-stu-id="a5fa6-145">For functions, we suggest avoiding the use of verbs in favor of common nouns (see guidance on proper nouns below) or adjectives:</span></span>

- `ConstantArray`
- `Head`
- `LookupFunction`

<span data-ttu-id="a5fa6-146">특히 거의 모든 경우에, 함수 이름이 퀀텀 프로그램의 다른 위치에 있는 작업 또는 부작용에 강력 하 게 연결 되어 있음을 나타내기 위해 해당 하는 경우 과거 participles를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-146">In particular, in almost all cases, we suggest using past participles where appropriate to indicate that a function name is strongly connected to an action or side effect elsewhere in a quantum program.</span></span>
<span data-ttu-id="a5fa6-147">예를 들어는  `ControlledOnInt` 동사 "control"의 part 분사 폼을 사용 하 여 함수에서 인수를 수정 하는 형용사로 동작 함을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-147">For example,  `ControlledOnInt` uses the part participle form of the verb "control" to indicate that the function acts as an adjective to modify its argument.</span></span>
<span data-ttu-id="a5fa6-148">이 이름에는 아래에서 설명한 대로 기본 제공 함수의 의미 체계와 일치 하는 추가 혜택이 있습니다 `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-148">This name has the additional benefit of matching the semantics of the built-in `Controlled` functor, as discussed further below.</span></span>
<span data-ttu-id="a5fa6-149">마찬가지로 _에이전트 명사_ 는와 강력 하 게 연결 된 udt의 이름에 대 한 작업 이름에서 함수와 UDT 이름을 생성 하는 데 사용할 수 있습니다 `Encoder` `Encode` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-149">Similarly, _agent nouns_ can be used to construct function and UDT names from operation names, as in the case of the name `Encoder` for a UDT that is strongly associated with `Encode`.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="a5fa6-150">지침</span><span class="sxs-lookup"><span data-stu-id="a5fa6-150">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="a5fa6-151">다음을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-151">We suggest:</span></span>

- <span data-ttu-id="a5fa6-152">작업 이름에 대 한 동사를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-152">Use verbs for operation names.</span></span>
- <span data-ttu-id="a5fa6-153">함수 이름에 명사 또는 형용사를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-153">Use nouns or adjectives for function names.</span></span>
- <span data-ttu-id="a5fa6-154">사용자 정의 형식 및 특성에는 명사를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-154">Use nouns for user-defined types and attributes.</span></span>
- <span data-ttu-id="a5fa6-155">모든 호출 가능 이름의 경우 `CamelCase` , 또는에 대해 강력한 기본 설정으로를 사용 `pascalCase` `snake_case` `ANGRY_CASE` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-155">For all callable names, use `CamelCase` in strong preference to `pascalCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="a5fa6-156">특히 호출 가능 이름이 대문자로 시작 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-156">In particular, ensure that callable names start with uppercase letters.</span></span>
- <span data-ttu-id="a5fa6-157">모든 지역 변수의 경우 `pascalCase` , 또는에 대해 강력한 기본 설정으로를 사용 `CamelCase` `snake_case` `ANGRY_CASE` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-157">For all local variables, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="a5fa6-158">특히 지역 변수가 소문자로 시작 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-158">In particular, ensure that local variables start with lowercase letters.</span></span>
- <span data-ttu-id="a5fa6-159">`_`함수 및 작업 이름에 밑줄을 사용 하지 마십시오. 계층의 추가 수준이 필요한 경우 네임 스페이스 및 네임 스페이스 별칭을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-159">Avoid the use of underscores `_` in function and operation names; where additional levels of hierarchy are needed, use namespaces and namespace aliases.</span></span>

# <a name="examples"></a>[<span data-ttu-id="a5fa6-160">예</span><span class="sxs-lookup"><span data-stu-id="a5fa6-160">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="a5fa6-161">Name</span><span class="sxs-lookup"><span data-stu-id="a5fa6-161">Name</span></span> | <span data-ttu-id="a5fa6-162">Description</span><span class="sxs-lookup"><span data-stu-id="a5fa6-162">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="a5fa6-163">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-163">☑</span></span> | `operation ReflectAboutStart` | <span data-ttu-id="a5fa6-164">작업의 효과를 나타내려면 동사 ("반사")를 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-164">Clear use of a verb ("reflect") to indicate the effect of the operation.</span></span> |
| <span data-ttu-id="a5fa6-165">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-165">☒</span></span> | <s>`operation XRotation`</s> | <span data-ttu-id="a5fa6-166">명사구를 사용 하는 것은 연산이 아니라 함수를 제안 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-166">Use of noun phrase suggests function, rather than operation.</span></span> |
| <span data-ttu-id="a5fa6-167">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-167">☒</span></span> | <s>`operation search_oracle`</s> | <span data-ttu-id="a5fa6-168">`snake_case`Contravenes 표기법을 사용 :::no-loc(Q#)::: 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-168">Use of `snake_case` contravenes :::no-loc(Q#)::: notation.</span></span> |
| <span data-ttu-id="a5fa6-169">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-169">☒</span></span> | <s>`operation Search_Oracle`</s> | <span data-ttu-id="a5fa6-170">작업 이름 contravenes 표기법 내부에서 밑줄을 사용 :::no-loc(Q#)::: 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-170">Use of underscores internal to operation name contravenes :::no-loc(Q#)::: notation.</span></span> |
| <span data-ttu-id="a5fa6-171">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-171">☑</span></span> | `function StatePreparationOracle` | <span data-ttu-id="a5fa6-172">명사구를 사용 하면 함수가 연산을 반환 하는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-172">Use of noun phrase suggests that the function returns an operation.</span></span> |
| <span data-ttu-id="a5fa6-173">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-173">☑</span></span> | `function EqualityFact` | <span data-ttu-id="a5fa6-174">명사 ("fact")를 명확 하 게 사용 하 여 함수가 함수 임을 나타내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-174">Clear use of noun ("fact") to indicate that this is a function, while the adjective.</span></span> |
| <span data-ttu-id="a5fa6-175">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-175">☒</span></span> | <s>`function GetRotationAngles`</s> | <span data-ttu-id="a5fa6-176">동사 ("get")를 사용 하는 것은 이것이 작업 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-176">Use of verb ("get") suggests that this is an operation.</span></span> |
| <span data-ttu-id="a5fa6-177">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-177">☑</span></span> | `newtype GeneratorTerm` | <span data-ttu-id="a5fa6-178">명사 구를 사용 하면 UDT 생성자 호출 결과를 명확 하 게 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-178">Use of noun phrase clearly refers to the result of calling the UDT constructor.</span></span> |
| <span data-ttu-id="a5fa6-179">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-179">☒</span></span> | <s>`@Attribute() newtype RunOnce()`</s> | <span data-ttu-id="a5fa6-180">동사 구를 사용 하면 UDT 생성자가 연산이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-180">Use of verb phrase suggests that the UDT constructor is an operation.</span></span> |
| <span data-ttu-id="a5fa6-181">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-181">☑</span></span> | `@Attribute() newtype Deprecated(Reason : String)` | <span data-ttu-id="a5fa6-182">명사구를 사용 하면 특성의 사용이 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-182">Use of noun phrase communicates the use of the attribute.</span></span> |

***

### <a name="entry-points"></a><span data-ttu-id="a5fa6-183">진입점</span><span class="sxs-lookup"><span data-stu-id="a5fa6-183">Entry Points</span></span>

<span data-ttu-id="a5fa6-184">프로그램에 대 한 진입점을 정의 하는 경우 :::no-loc(Q#)::: :::no-loc(Q#)::: 컴파일러는 진입점이 특정 이름 (예: [ `@EntryPoint()` ](xref:Microsoft.Quantum.Core.EntryPoint) `main` , `Main` 또는 `__main__` )을 요구 하는 대신 특성을 인식 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-184">When defining an entry point into a :::no-loc(Q#)::: program, the :::no-loc(Q#)::: compiler recognizes the [`@EntryPoint()` attribute](xref:Microsoft.Quantum.Core.EntryPoint) rather requiring that entry points have a particular name (e.g.: `main`, `Main`, or `__main__`).</span></span>
<span data-ttu-id="a5fa6-185">즉, 개발자의 관점에서 :::no-loc(Q#)::: 진입점은로 주석이 지정 된 일반 작업입니다 `@EntryPoint()` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-185">That is, from the perspective of a :::no-loc(Q#)::: developer, entry points are ordinary operations annotated with `@EntryPoint()`.</span></span>
<span data-ttu-id="a5fa6-186">또한 :::no-loc(Q#)::: 진입점은 전체 응용 프로그램에 대 한 진입점 일 수 있습니다 (예 :::no-loc(Q#)::: : 독립 실행형 실행 프로그램의 경우) :::no-loc(Q#)::: . 또는 응용 프로그램의 호스트 프로그램 (예: Python 또는 .net과 함께를 사용 하는 경우)에 대 한 진입점이 진입점 :::no-loc(Q#)::: 에 적용 될 때 잘못 된 이름일 :::no-loc(Q#)::: 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-186">Moreover, :::no-loc(Q#)::: entry points may be entry points for an entire application (for example, in :::no-loc(Q#)::: standalone executable programs), or may be an interface between a :::no-loc(Q#)::: program and the host program for an application (i.e.: when using :::no-loc(Q#)::: with Python or .NET), such that the name "main" could be misleading when applied to a :::no-loc(Q#)::: entry point.</span></span>

<span data-ttu-id="a5fa6-187">`@EntryPoint()`위에 나열 된 이름 지정 작업에 대 한 일반적인 조언을 사용 하 여 특성 사용을 반영 하기 위해 명명 진입점을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-187">We suggest using naming entry points to reflect the use of the `@EntryPoint()` attribute by using the general advice for naming operations listed above.</span></span>


# <a name="guidance"></a>[<span data-ttu-id="a5fa6-188">지침</span><span class="sxs-lookup"><span data-stu-id="a5fa6-188">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="a5fa6-189">다음을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-189">We suggest:</span></span>

- <span data-ttu-id="a5fa6-190">진입점 작업의 이름을 "main"으로 지정 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-190">Do not name entry point operations as "main."</span></span>
- <span data-ttu-id="a5fa6-191">진입점 작업의 이름을 일반 작업으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-191">Name entry point operations as ordinary operations.</span></span>

# <a name="examples"></a>[<span data-ttu-id="a5fa6-192">예</span><span class="sxs-lookup"><span data-stu-id="a5fa6-192">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="a5fa6-193">Name</span><span class="sxs-lookup"><span data-stu-id="a5fa6-193">Name</span></span> | <span data-ttu-id="a5fa6-194">Description</span><span class="sxs-lookup"><span data-stu-id="a5fa6-194">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="a5fa6-195">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-195">☑</span></span> | `@EntryPoint() operation RunSimulation` | <span data-ttu-id="a5fa6-196">작업 이름을 통해 진입점의 용도를 명확 하 게 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-196">Clearly communicates purpose of entry point through operation name.</span></span> |
| <span data-ttu-id="a5fa6-197">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-197">☒</span></span> | <s>`@EntryPoint() operation Main`</s> | <span data-ttu-id="a5fa6-198">를 사용 `Main` 하면 진입점의 목적이 명확 하 게 전달 되지 않으며 특성으로 중복 됩니다 `@EntryPoint()` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-198">Use of `Main` doesn't clearly communicate purpose of entry point, and is redundant with `@EntryPoint()` attribute.</span></span> |

<span data-ttu-id="a5fa6-199">\*\*_</span><span class="sxs-lookup"><span data-stu-id="a5fa6-199">\*\*_</span></span>

### <a name="shorthand-and-abbreviations"></a><span data-ttu-id="a5fa6-200">약어 및 약어</span><span class="sxs-lookup"><span data-stu-id="a5fa6-200">Shorthand and Abbreviations</span></span> ###

<span data-ttu-id="a5fa6-201">위의 충고도 불구는 퀀텀 컴퓨팅에서 공통적이 고 널리 사용 되는 여러 가지 형태의 축약형입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-201">The above advice notwithstanding, there are many forms of shorthand that see common and pervasive use in quantum computing.</span></span>
<span data-ttu-id="a5fa6-202">특히 대상 컴퓨터의 작업에 내장 된 작업의 경우 기존 및 일반적인 약어를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-202">We suggest using existing and common shorthand where it exists, especially for operations that are intrinsic to the operation of a target machine.</span></span>
<span data-ttu-id="a5fa6-203">예를 들어 대신 및 대신 이름을 선택 `X` `ApplyX` `Rz` `RotateAboutZ` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-203">For example, we choose the name `X` instead of `ApplyX`, and `Rz` instead of `RotateAboutZ`.</span></span>
<span data-ttu-id="a5fa6-204">이러한 약어를 사용 하는 경우 작업 이름은 모두 대문자 여야 합니다 (예: `MAJ` ).</span><span class="sxs-lookup"><span data-stu-id="a5fa6-204">When using such shorthand, operation names should be all uppercase (e.g.: `MAJ`).</span></span>

<span data-ttu-id="a5fa6-205">일반적으로 사용 되는 머리글자어의 경우에는 "퀀텀 푸리에 변환"의 경우 "QFT"와 같은의 두문자어 정의에이 규칙을 적용할 때 주의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-205">Some care is required when applying this convention in the case of commonly used acronyms and initialisms such as "QFT" for "quantum Fourier transform."</span></span>
<span data-ttu-id="a5fa6-206">전체 이름에 머리글자어 및의 두문자어 정의를 사용 하는 데 일반적인 .NET 규칙을 사용 하는 것이 좋습니다 .이에 대 한 자세한 내용은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-206">We suggest following general .NET conventions for the use of acronyms and initialisms in full names, which prescribe that:</span></span>

- <span data-ttu-id="a5fa6-207">두 문자로 된 머리글자어와의 두문자어 정의는 대문자로 명명 됩니다 (예: `BE` "빅 endian"의 경우).</span><span class="sxs-lookup"><span data-stu-id="a5fa6-207">two-letter acronyms and initialisms are named in upper case (e.g.: `BE` for "big-endian"),</span></span>
- <span data-ttu-id="a5fa6-208">모든 긴 머리글자어 및의 두문자어 정의는 `CamelCase` (예: `Qft` "퀀텀 푸리에 변환"의 경우)로 이름이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-208">all longer acronyms and initialisms are named in `CamelCase` (e.g.: `Qft` for "quantum Fourier transform")</span></span>

<span data-ttu-id="a5fa6-209">따라서 QFT를 구현 하는 작업을 `QFT` 약어로 호출 하거나로 작성할 수 있습니다 `ApplyQft` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-209">Thus, an operation implementing the QFT could either be called `QFT` as shorthand, or written out as `ApplyQft`.</span></span>

<span data-ttu-id="a5fa6-210">특히 일반적으로 사용 되는 작업 및 함수에 대해 더 긴 형식의 _별칭_ 으로 약식 이름을 제공 하는 것이 좋을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-210">For particularly commonly used operations and functions, it may be desirable to provide a shorthand name as an _alias_ for a longer form:</span></span>

```qsharp
operation CCNOT(control0 : Qubit, control1 : Qubit, target : Qubit)
is Adj + Ctl {
    Controlled X([control0, control1], target);
}
```

# <a name="guidance"></a>[<span data-ttu-id="a5fa6-211">지침</span><span class="sxs-lookup"><span data-stu-id="a5fa6-211">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="a5fa6-212">다음을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-212">We suggest:</span></span>

- <span data-ttu-id="a5fa6-213">적절 한 경우 일반적으로 허용 되 고 널리 사용 되는 약식 이름을 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-213">Consider commonly accepted and widely used shorthand names when appropriate.</span></span>
- <span data-ttu-id="a5fa6-214">약어에 대문자를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-214">Use uppercase for shorthand.</span></span>
- <span data-ttu-id="a5fa6-215">Short (2 자) 머리글자어 및의 두문자어 정의에 대문자를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-215">Use uppercase for short (two-letter) acronyms and initialisms.</span></span>
- <span data-ttu-id="a5fa6-216">`CamelCase`더 긴 (3 자 이상) 머리글자어 및의 두문자어 정의에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-216">Use `CamelCase` for longer (three or more letter) acronyms and initialisms.</span></span>

# <a name="examples"></a>[<span data-ttu-id="a5fa6-217">예</span><span class="sxs-lookup"><span data-stu-id="a5fa6-217">Examples</span></span>](#tab/examples)

| &nbsp;   | <span data-ttu-id="a5fa6-218">Name</span><span class="sxs-lookup"><span data-stu-id="a5fa6-218">Name</span></span> | <span data-ttu-id="a5fa6-219">Description</span><span class="sxs-lookup"><span data-stu-id="a5fa6-219">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="a5fa6-220">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-220">☑</span></span> | `X` | <span data-ttu-id="a5fa6-221">"$X $ 변환 적용"의 이해 하기 쉬운 약어</span><span class="sxs-lookup"><span data-stu-id="a5fa6-221">Well-understood shorthand for "apply an $X$ transformation"</span></span> |
| <span data-ttu-id="a5fa6-222">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-222">☑</span></span> | `CNOT` | <span data-ttu-id="a5fa6-223">"제어-없음"에 대 한 이해 하기 쉬운 약어</span><span class="sxs-lookup"><span data-stu-id="a5fa6-223">Well-understood shorthand for "controlled-NOT"</span></span> |
| <span data-ttu-id="a5fa6-224">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-224">☒</span></span> | <s>`Cnot`</s> | <span data-ttu-id="a5fa6-225">약어는에 사용할 수 없습니다 `CamelCase` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-225">Shorthand should not be in `CamelCase`.</span></span> |
| <span data-ttu-id="a5fa6-226">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-226">☑</span></span> | `ApplyQft` | <span data-ttu-id="a5fa6-227">일반적인 initialism "QFT"는 긴 형식 이름의 일부로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-227">Common initialism "QFT" appears as a part of a long-form name.</span></span> |
| <span data-ttu-id="a5fa6-228">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-228">☑</span></span> | `QFT` | <span data-ttu-id="a5fa6-229">일반적인 initialism "QFT"는 약식 이름의 일부로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-229">Common initialism "QFT" appears as a part of a shorthand name.</span></span> |



_*_


### <a name="proper-nouns-in-names"></a><span data-ttu-id="a5fa6-230">이름에 적절 한 명사</span><span class="sxs-lookup"><span data-stu-id="a5fa6-230">Proper Nouns in Names</span></span> ###

<span data-ttu-id="a5fa6-231">물리학에는 첫 번째 사람이 게시 한 후 이름을 변경 하는 것이 일반적 이지만 대부분의 비 physicists은 모든 사용자의 이름 및 모든 기록에 대해 잘 알고 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-231">While in physics it is common to name things after the first person to publish about them, most non-physicists aren’t familiar with everyone’s names and all of the history.</span></span>
<span data-ttu-id="a5fa6-232">다른 배경의 사용자는 일반적인 작업 및 개념을 사용 하기 위해 많은 수의 불투명 한 이름을 알아야 하므로, 물리의 명명 규칙에 너무 많이 의존 하는 것은 매우 중요 한 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-232">Relying too heavily on naming conventions from physics can thus put up a substantial barrier to entry, as users from other backgrounds must learn a large number of seemingly opaque names in order to use common operations and concepts.</span></span>
<!-- An important part of the task of reducing confusion is to make code more accessible.
Especially in a field such as quantum computing that is rich with domain expertise, we must at all times be cognizant of the demands we place on that expertise as we design quantum software.
In naming code symbols, one way that this cognizance expresses itself is as an awareness of the convention from physics of adopting as the names of algorithms and operations the names of their original publishers.
While we must maintain the history and intellectual provenance of concepts in quantum computing, demanding that all users be versed in this history to use even the most basic of functions and operations places a barrier to entry that is in most cases severe enough to even present an ethical compromise. -->
<span data-ttu-id="a5fa6-233">따라서 개념을 설명 하는 적절 한 일반적인 명사를 개념의 게시 기록을 설명 하는 적절 한 명사에 적용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-233">Thus, we recommend that wherever reasonable, common nouns that describe a concept be adopted in strong preference to proper nouns that describe the publication history of a concept.</span></span>
<span data-ttu-id="a5fa6-234">특정 한 예로, 단일 제어 된 교환 및 이중 제어 되지 않는 작업을 교육용 자료의 "Fredkin" 및 "Toffoli" 작업 이라고 :::no-loc(Q#)::: 하며 주로 및로 식별 됩니다 `CSWAP` `CCNOT` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-234">As a particular example, the singly controlled SWAP and doubly controlled NOT operations are often called the "Fredkin" and "Toffoli" operations in academic literature, but are identified in :::no-loc(Q#)::: primarily as `CSWAP` and `CCNOT`.</span></span>
<span data-ttu-id="a5fa6-235">두 경우 모두 적절 한 명사와 함께 적절 한 명사를 기반으로 하는 동의어 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-235">In both cases, the API documentation comments provide synonymous names based on proper nouns, along with all appropriate citations.</span></span>

<span data-ttu-id="a5fa6-236">이러한 기본 설정은 특히 적절 한 명사를 사용 하는 것이 항상 필요한 경우에 특히 중요 합니다 :::no-loc(Q#)::: . 예를 들어, 여러 기존 언어에서 설정 된 전통을을 따르고, `Bool` 부울 논리에 대 한 참조의 형식을 참조 하며,이는 George Boole의 준수에 명명 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-236">This preference is especially important given that some usage of proper nouns will always be necessary — :::no-loc(Q#)::: follows the tradition set by many classical languages, for instance, and refers to `Bool` types in reference to Boolean logic, which is in turn named in honor of George Boole.</span></span>
<span data-ttu-id="a5fa6-237">이와 비슷한 몇 가지 퀀텀 개념은 `Pauli` 언어에 기본 제공 되는 형식을 포함 하 여 비슷한 방식으로 이름이 지정 됩니다 :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-237">A few quantum concepts similarly are named in a similar fashion, including the `Pauli` type built-in to the :::no-loc(Q#)::: language.</span></span>
<span data-ttu-id="a5fa6-238">이러한 사용법이 필수적이 지 않은 적절 한 명사 사용을 최소화 하면 적절 한 명사를 피할 수 없는 영향을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-238">By minimizing the usage of proper nouns where such usage is not essential, we reduce the impact where proper nouns cannot be reasonably avoided.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="a5fa6-239">지침</span><span class="sxs-lookup"><span data-stu-id="a5fa6-239">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="a5fa6-240">다음을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-240">We suggest:</span></span>

- <span data-ttu-id="a5fa6-241">이름에 적절 한 명사를 사용 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-241">Avoid the use of proper nouns in names.</span></span>

# <a name="examples"></a>[<span data-ttu-id="a5fa6-242">예</span><span class="sxs-lookup"><span data-stu-id="a5fa6-242">Examples</span></span>](#tab/examples)

_*_

### <a name="type-conversions"></a><span data-ttu-id="a5fa6-243">형식 변환</span><span class="sxs-lookup"><span data-stu-id="a5fa6-243">Type Conversions</span></span> ###

<span data-ttu-id="a5fa6-244">:::no-loc(Q#):::는 강력 하 고 staticly 지정 된 언어 이므로 한 형식의 값은 형식 변환 함수에 대 한 명시적 호출을 사용 하 여 다른 형식의 값 으로만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-244">Since :::no-loc(Q#)::: is a strongly and staticly typed language, a value of one type can only be used as a value of another type by using an explicit call to a type conversion function.</span></span>
<span data-ttu-id="a5fa6-245">이는 값이 암시적으로 (예: 유형 프로 모션) 형식을 변경 하거나 캐스팅을 통해 변경할 수 있는 언어와는 대조적입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-245">This is in contrast to languages which allow for values to change types implicitly (e.g.: type promotion), or through casting.</span></span>
<span data-ttu-id="a5fa6-246">결과적으로 형식 변환 함수는 라이브러리 개발 시 중요 한 역할을 :::no-loc(Q#)::: 하며 명명에 대 한 보다 일반적으로 발생 하는 사항 중 하나를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-246">As a result, type conversion functions play an important role in :::no-loc(Q#)::: library development, and comprise one of the more commonly encountered decisions about naming.</span></span>
<span data-ttu-id="a5fa6-247">그러나 형식 변환은 항상 _결정적_ 이므로 함수로 작성 될 수 있으므로 위의 권장 사항 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-247">We note, however, that since type conversions are always _deterministic_ , they can be written as functions and thus fall under the advice above.</span></span>
<span data-ttu-id="a5fa6-248">특히 형식 변환 함수에는 동사 (예:) 또는 부사 prepositional 구 ()로 이름을 지정 하지 않는 것이 좋지만,이 경우에 `ConvertToX` `ToX` 는 소스 및 대상 형식 ()을 나타내는 형용사 prepositional 구로 명명 되어야 합니다 `XAsY` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-248">In particular, we suggest that type conversion functions should never be named as verbs (e.g.: `ConvertToX`) or adverb prepositional phrases (`ToX`), but should be named as adjective prepositional phrases that indicate the source and destination types (`XAsY`).</span></span>
<span data-ttu-id="a5fa6-249">형식 변환 함수 이름에 배열 형식을 나열할 때 줄임을 권장 `Arr` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-249">When listing array types in type conversion function names, we recommend the shorthand `Arr`.</span></span>
<span data-ttu-id="a5fa6-250">예외적인 상황을 제외 하 고,를 사용 하 여 모든 형식 변환 함수 이름을 지정 하 여 신속 하 게 식별할 수 있도록 하는 것이 좋습니다 `As` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-250">Barring exceptional circumstances, we recommend that all type conversion functions be named using `As` so that they can be quickly identified.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="a5fa6-251">지침</span><span class="sxs-lookup"><span data-stu-id="a5fa6-251">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="a5fa6-252">다음을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-252">We suggest:</span></span>

- <span data-ttu-id="a5fa6-253">함수가 형식의 값을 형식의 값으로 변환 하는 경우 `X` `Y` 이름 또는을 사용 `AsY` `XAsY` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-253">If a function converts a value of type `X` to a value of type `Y`, use either the name `AsY` or `XAsY`.</span></span>

# <a name="examples"></a>[<span data-ttu-id="a5fa6-254">예</span><span class="sxs-lookup"><span data-stu-id="a5fa6-254">Examples</span></span>](#tab/examples)

| &nbsp;   | <span data-ttu-id="a5fa6-255">Name</span><span class="sxs-lookup"><span data-stu-id="a5fa6-255">Name</span></span> | <span data-ttu-id="a5fa6-256">Description</span><span class="sxs-lookup"><span data-stu-id="a5fa6-256">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="a5fa6-257">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-257">☒</span></span> | <s>`ToDouble`</s> | <span data-ttu-id="a5fa6-258">전치사 "to"는 동사가 아닌 연산을 나타내는 동사 구를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-258">The preposition "to" results in a verb phrase, indicating an operation and not a function.</span></span> |
| <span data-ttu-id="a5fa6-259">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-259">☒</span></span> | <s>`AsDouble`</s> | <span data-ttu-id="a5fa6-260">입력 형식이 함수 이름에서 명확 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-260">The input type is not clear from the function name.</span></span> |
| <span data-ttu-id="a5fa6-261">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-261">☒</span></span> | <s>`PauliArrFromBoolArr`</s> | <span data-ttu-id="a5fa6-262">입력 및 출력 형식이 잘못 된 순서로 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-262">The input and output types appear in the wrong order.</span></span> |
| <span data-ttu-id="a5fa6-263">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-263">☑</span></span> | `ResultArrAsBoolArr` | <span data-ttu-id="a5fa6-264">입력 형식과 출력 형식은 모두 명확 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-264">Both the input types and output types are clear.</span></span> |

_*_

### <a name="private-or-internal-names"></a><span data-ttu-id="a5fa6-265">개인 또는 내부 이름</span><span class="sxs-lookup"><span data-stu-id="a5fa6-265">Private or Internal Names</span></span> ###

<span data-ttu-id="a5fa6-266">대부분의 경우 이름은 라이브러리 또는 프로젝트 내부에서 사용 하기 위한 것 이며 라이브러리에서 제공 하는 API의 보장 된 부분이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-266">In many cases, a name is intended strictly for use internal to a library or project, and is not a guaranteed part of the API offered by a library.</span></span>
<span data-ttu-id="a5fa6-267">내부 전용 코드에 대 한 실수로 종속성이 명확 하 게 적용 되도록 함수 및 작업의 이름을 지정 하는 경우이를 명확 하 게 표시 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-267">It is helpful to clearly indicate that this is the case when naming functions and operations so that accidental dependencies on internal-only code are made obvious.</span></span>
<span data-ttu-id="a5fa6-268">작업 또는 함수가 직접 사용 하기 위한 것이 아니며, 부분 응용 프로그램에서 작동 하는 일치 하는 호출 가능에서 사용 해야 하는 경우에는 `internal` 부분적으로 적용 되는 호출 가능에 대해 키워드로 시작 하는 이름을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-268">If an operation or function is not intended for direct use, but rather should be used by a matching callable which acts by partial application, consider using a name starting with the `internal` keyword for the callable that is partially applied.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="a5fa6-269">지침</span><span class="sxs-lookup"><span data-stu-id="a5fa6-269">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="a5fa6-270">다음을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-270">We suggest:</span></span>

- <span data-ttu-id="a5fa6-271">함수, 작업 또는 사용자 정의 형식이 라이브러리 또는 프로그램에 대 한 공용 API의 일부가 아닌 경우 :::no-loc(Q#)::: `internal` , 또는 선언 앞에 키워드를 배치 하 여 내부로 표시 되었는지 확인 `function` `operation` `newtype` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-271">When a function, operation, or user-defined type is not a part of the public API for a :::no-loc(Q#)::: library or program, ensure that it is marked as internal by placing the `internal` keyword before the `function`, `operation`, or `newtype` declaration.</span></span>

# <a name="examples"></a>[<span data-ttu-id="a5fa6-272">예</span><span class="sxs-lookup"><span data-stu-id="a5fa6-272">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="a5fa6-273">Name</span><span class="sxs-lookup"><span data-stu-id="a5fa6-273">Name</span></span> | <span data-ttu-id="a5fa6-274">Description</span><span class="sxs-lookup"><span data-stu-id="a5fa6-274">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="a5fa6-275">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-275">☒</span></span> | <s>`operation _ApplyDecomposedOperation`</s> | <span data-ttu-id="a5fa6-276">`_`이 작업이 내부용 으로만 사용 됨을 나타내기 위해 밑줄을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-276">Do not use an underscore `_` to indicate that this operation is for internal use only.</span></span> |
| <span data-ttu-id="a5fa6-277">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-277">☑</span></span> | `internal operation ApplyDecomposedOperation` | <span data-ttu-id="a5fa6-278">`internal`시작 부분에 있는 키워드는이 작업이 내부용 으로만 사용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-278">The `internal` keyword at the beginning clearly indicates that this operation is for internal use only.</span></span> |

_*_
### <a name="variants"></a><span data-ttu-id="a5fa6-279">변형</span><span class="sxs-lookup"><span data-stu-id="a5fa6-279">Variants</span></span> ###

<span data-ttu-id="a5fa6-280">이후 버전의에서는 이러한 제한 사항이 유지 되지 않을 수 있지만 :::no-loc(Q#)::: , 현재는 해당 입력을 함수 하는 것과 관련 된 작업 또는 함수의 그룹이 나 구체적으로 인수를 사용할 수 있는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-280">Though this limitation may not persist in future versions of :::no-loc(Q#):::, it is presently the case that there will often be groups of related operations or functions that are distinguished by which functors their inputs support, or by the concrete types of their arguments.</span></span>
<span data-ttu-id="a5fa6-281">이러한 그룹은 동일한 루트 이름과 해당 변형을 나타내는 하나 또는 두 개의 문자를 사용 하 여 구분할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-281">These groups can be distinguished by using the same root name, followed by one or two letters that indicate its variant.</span></span>

| <span data-ttu-id="a5fa6-282">접미사</span><span class="sxs-lookup"><span data-stu-id="a5fa6-282">Suffix</span></span> | <span data-ttu-id="a5fa6-283">의미</span><span class="sxs-lookup"><span data-stu-id="a5fa6-283">Meaning</span></span> |
|--------|---------|
| `A` | <span data-ttu-id="a5fa6-284">지원 해야 하는 입력 `Adjoint`</span><span class="sxs-lookup"><span data-stu-id="a5fa6-284">Input expected to support `Adjoint`</span></span> |
| `C` | <span data-ttu-id="a5fa6-285">지원 해야 하는 입력 `Controlled`</span><span class="sxs-lookup"><span data-stu-id="a5fa6-285">Input expected to support `Controlled`</span></span> |
| `CA` | <span data-ttu-id="a5fa6-286">입력은 및를 지원 해야 합니다. `Controlled``Adjoint`</span><span class="sxs-lookup"><span data-stu-id="a5fa6-286">Input expected to support `Controlled` and `Adjoint`</span></span> |
| `I` | <span data-ttu-id="a5fa6-287">입력 또는 입력은 형식입니다. `Int`</span><span class="sxs-lookup"><span data-stu-id="a5fa6-287">Input or inputs are of type `Int`</span></span> |
| `D` | <span data-ttu-id="a5fa6-288">입력 또는 입력은 형식입니다. `Double`</span><span class="sxs-lookup"><span data-stu-id="a5fa6-288">Input or inputs are of type `Double`</span></span> |
| `L` | <span data-ttu-id="a5fa6-289">입력 또는 입력은 형식입니다. `BigInt`</span><span class="sxs-lookup"><span data-stu-id="a5fa6-289">Input or inputs are of type `BigInt`</span></span> |

# <a name="guidance"></a>[<span data-ttu-id="a5fa6-290">지침</span><span class="sxs-lookup"><span data-stu-id="a5fa6-290">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="a5fa6-291">다음을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-291">We suggest:</span></span>

- <span data-ttu-id="a5fa6-292">함수 또는 작업이 해당 입력의 유형 및 함수 지원에 의해 유사한 함수 또는 작업과 관련이 없는 경우에는 접미사를 사용 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-292">If a function or operation is not related to any similar functions or operations by the types and functor support of their inputs, do not use a suffix.</span></span>
- <span data-ttu-id="a5fa6-293">함수 또는 작업이 해당 입력의 유형 및 함수 지원에 의해 유사한 함수 또는 작업과 관련 된 경우에는 위의 표에서와 같이 접미사를 사용 하 여 변형을 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-293">If a function or operation is related to any similar functions or operations by the types and functor support of their inputs, use suffixes as in the table above to distinguish variants.</span></span>

# <a name="examples"></a>[<span data-ttu-id="a5fa6-294">예</span><span class="sxs-lookup"><span data-stu-id="a5fa6-294">Examples</span></span>](#tab/examples)

_*_

### <a name="arguments-and-variables"></a><span data-ttu-id="a5fa6-295">인수 및 변수</span><span class="sxs-lookup"><span data-stu-id="a5fa6-295">Arguments and Variables</span></span> ###

<span data-ttu-id="a5fa6-296">:::no-loc(Q#):::함수 또는 작업에 대 한 코드의 핵심 목표는 쉽게 읽고 이해할 수 있도록 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-296">A key goal of the :::no-loc(Q#)::: code for a function or operation is for it to be easily read and understood.</span></span>
<span data-ttu-id="a5fa6-297">마찬가지로 입력 및 형식 인수의 이름은 제공 된 후 함수 또는 인수가 사용 되는 방식에 대해 통신 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-297">Similarly, the names of inputs and type arguments should communicate how a function or argument will be used once provided.</span></span>


# <a name="guidance"></a>[<span data-ttu-id="a5fa6-298">지침</span><span class="sxs-lookup"><span data-stu-id="a5fa6-298">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="a5fa6-299">다음을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-299">We suggest:</span></span>

- <span data-ttu-id="a5fa6-300">모든 변수 및 입력 이름에 대해 `pascalCase` 강력한 기본 설정에서, 또는로를 사용 `CamelCase` `snake_case` `ANGRY_CASE` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-300">For all variable and input names, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span>
- <span data-ttu-id="a5fa6-301">입력 이름은 설명적 이어야 합니다. 가능 하면 하나 또는 두 개의 문자 이름을 사용 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-301">Input names should be descriptive; avoid one or two letter names where possible.</span></span>
- <span data-ttu-id="a5fa6-302">정확히 하나의 형식 인수를 허용 하는 작업 및 함수는 `T` 해당 역할이 명확 하 게 될 때에서 해당 형식 인수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-302">Operations and functions accepting exactly one type argument should denote that type argument by `T` when its role is obvious.</span></span>
- <span data-ttu-id="a5fa6-303">함수 또는 작업에서 여러 형식 인수를 사용 하거나 단일 형식 인수의 역할이 명확 하지 않은 경우 각 형식에 대해 앞에 오는 짧은 대문자 단어 `T` (예:)를 사용 하는 것이 좋습니다 `TOutput` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-303">If a function or operation takes multiple type arguments, or if the role of a single type argument is not obvious, consider using a short capitalized word prefaced by `T` (e.g.: `TOutput`) for each type.</span></span>
- <span data-ttu-id="a5fa6-304">인수 및 변수 이름에 형식 이름을 포함 하지 마십시오. 이 정보는 개발 환경에서 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-304">Do not include type names in argument and variable names; this information can and should be provided by your development environment.</span></span>
- <span data-ttu-id="a5fa6-305">리터럴 이름 ( `flagQubit` ) 및 배열 형식 ()으로 스칼라 형식을 나타냅니다 `measResults` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-305">Denote scalar types by their literal names (`flagQubit`), and array types by a plural (`measResults`).</span></span>
  <span data-ttu-id="a5fa6-306">구체적 비트 배열의 경우에는 `Register` 이름이 특정 방식으로 밀접 하 게 관련 된 다양 한 비트 시퀀스를 참조 하는 방식으로 이러한 형식을 나타내는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-306">For arrays of qubits in particular, consider denoting such types by `Register` where the name refers to a sequence of qubits that are closely related in some way.</span></span>
- <span data-ttu-id="a5fa6-307">배열로 인덱스로 사용 되는 변수는로 시작 해야 `idx` 하며 단수형 (예:) 이어야 합니다. `things[idxThing]`</span><span class="sxs-lookup"><span data-stu-id="a5fa6-307">Variables used as indices into arrays should begin with `idx` and should be singular (e.g.: `things[idxThing]`).</span></span>
  <span data-ttu-id="a5fa6-308">특히 단일 문자 변수 이름을 인덱스로 사용 하지 않는 것이 좋습니다. `idx` 최소한을 사용 하십시오.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-308">In particular, strongly avoid using single-letter variable names as indices; consider using `idx` at a minimum.</span></span>
- <span data-ttu-id="a5fa6-309">배열의 길이를 포함 하는 데 사용 되는 변수는로 시작 해야 `n` 하 고 복수화 해야 합니다 (예: `nThings` ).</span><span class="sxs-lookup"><span data-stu-id="a5fa6-309">Variables used to hold lengths of arrays should begin with `n` and should be pluralized (e.g.: `nThings`).</span></span>

# <a name="examples"></a>[<span data-ttu-id="a5fa6-310">예</span><span class="sxs-lookup"><span data-stu-id="a5fa6-310">Examples</span></span>](#tab/examples)

_*_

### <a name="user-defined-type-named-items"></a><span data-ttu-id="a5fa6-311">User-Defined 형식의 명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="a5fa6-311">User-Defined Type Named Items</span></span> ###

<span data-ttu-id="a5fa6-312">사용자 정의 형식의 명명 된 항목은 `CamelCase` UDT 생성자에 대 한 입력으로도로 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-312">Named items in user-defined types should be named as `CamelCase`, even in input to UDT constructors.</span></span>
<span data-ttu-id="a5fa6-313">이를 통해 접근자 표기법 (예: `callable::Apply` ) 또는 복사 및 업데이트 표기법 ()을 사용할 때 명명 된 항목을 지역 범위 변수에 대 한 참조에서 명확 하 게 구분할 수 있습니다. `set arr w/= Data <- newData`</span><span class="sxs-lookup"><span data-stu-id="a5fa6-313">This helps in order to clearly separate named items from references to locally scoped variables when using accessor notation (e.g.: `callable::Apply`) or copy-and-update notation (`set arr w/= Data <- newData`).</span></span>

# <a name="guidance"></a>[<span data-ttu-id="a5fa6-314">지침</span><span class="sxs-lookup"><span data-stu-id="a5fa6-314">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="a5fa6-315">다음을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-315">We suggest:</span></span>

- <span data-ttu-id="a5fa6-316">UDT 생성자의 명명 된 항목 이름은로 지정 해야 합니다. `CamelCase` 즉, 초기 대문자로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-316">Named items in UDT constructors should be named as `CamelCase`; that is, they should begin with an initial uppercase.</span></span>
- <span data-ttu-id="a5fa6-317">작업으로 확인 되는 명명 된 항목은 동사 단계로 명명 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-317">Named items that resolve to operations should be named as verb phases.</span></span>
- <span data-ttu-id="a5fa6-318">작업을 확인 하지 않는 명명 된 항목은 명사 구로 명명 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-318">Named items that do not resolve to operations should be named as noun phrases.</span></span>
- <span data-ttu-id="a5fa6-319">작업을 래핑하는 Udt의 경우 라는 이름의 단일 항목을 `Apply` 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-319">For UDTs that wrap operations, a single named item called `Apply` should be defined.</span></span>

# <a name="examples"></a>[<span data-ttu-id="a5fa6-320">예</span><span class="sxs-lookup"><span data-stu-id="a5fa6-320">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="a5fa6-321">코드 조각</span><span class="sxs-lookup"><span data-stu-id="a5fa6-321">Snippet</span></span> | <span data-ttu-id="a5fa6-322">Description</span><span class="sxs-lookup"><span data-stu-id="a5fa6-322">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="a5fa6-323">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-323">☑</span></span> | `newtype Oracle = (Apply : Qubit[] => Unit is Adj + Ctl)` | <span data-ttu-id="a5fa6-324">이름은 `Apply` `CamelCase` 형식이 지정 된 동사 구로, 명명 된 항목이 작업 임을 제안 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-324">The name `Apply` is a `CamelCase`-formatted verb phrase, suggesting that the named item is an operation.</span></span> |
| <span data-ttu-id="a5fa6-325">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-325">☒</span></span> | <s>`newtype Oracle = (apply : Qubit[] => Unit is Adj + Ctl) `</s> | <span data-ttu-id="a5fa6-326">명명 된 항목은 초기 대문자로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-326">Named items should begin with an initial uppercase letter.</span></span> |
| <span data-ttu-id="a5fa6-327">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-327">☒</span></span> | <s>`newtype Collection = (Length : Int, Get : Int -> (Qubit => Unit)) `</s> | <span data-ttu-id="a5fa6-328">함수를 확인 하는 명명 된 항목은 동사 구가 아닌 명사 구로 명명 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-328">Named items which resolve to functions should be named as noun phrases, not as verb phrases.</span></span> |

_*_

## <a name="input-conventions"></a><span data-ttu-id="a5fa6-329">입력 규칙</span><span class="sxs-lookup"><span data-stu-id="a5fa6-329">Input Conventions</span></span> ##

<span data-ttu-id="a5fa6-330">개발자가 작업 또는 함수를 호출 하는 경우 해당 작업 또는 함수에 대 한 다양 한 입력을 특정 순서로 지정 하 여 개발자가 라이브러리를 사용 하기 위해 직면 하 게 되는 인지 부하를 늘려야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-330">When a developer calls into an operation or function, the various inputs to that operation or function must be specified in a particular order, increasing the cognitive load that a developer faces in order to make use of a library.</span></span>
<span data-ttu-id="a5fa6-331">특히 입력 순서 기억 하는 작업은 일반적으로 퀀텀 알고리즘의 구현 프로그래밍의 작업에서 혼란 스 러가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-331">In particular, the task of remembering input orderings is often a distraction from the task at hand: programming an implementation of a quantum algorithm.</span></span>
<span data-ttu-id="a5fa6-332">풍부한 IDE 지원으로 인해이를 매우 광범위 하 게 완화할 수 있지만 일반적인 규칙을 잘 설계 하 고 준수 하는 것은 API에 의해 적용 되는 인지 부하를 최소화 하는 데도 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-332">Though rich IDE support can mitigate this to a large extent, good design and adherence to common conventions can also help to minimize the cognitive load imposed by an API.</span></span>

<span data-ttu-id="a5fa6-333">가능 하면 작업이 나 함수에 필요한 입력 수를 줄이는 것이 도움이 될 수 있습니다. 그러면 각 입력의 역할이 해당 작업 또는 함수를 호출 하는 개발자와 나중에 해당 코드를 읽는 개발자에 게 더 즉각적으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-333">Where possible, it can be helpful to reduce the number of inputs expected by an operation or function, so that the role of each input is more immediately obvious both to developers calling into that operation or function, and to developers reading that code later.</span></span>
<span data-ttu-id="a5fa6-334">특히 작업이 나 함수에 대 한 인수 수를 줄이는 것이 불가능 하거나 적절 하지 않은 경우 입력 순서를 예측할 때 사용자가 직면 하는 갑작스러운 요소를 최소화 하는 일관 된 순서를 지정 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-334">Especially when it is not possible or reasonable to reduce the number of arguments to an operation or function, it is important to have a consistent ordering that minimizes the surprise that a user faces when predicting the order of inputs.</span></span>

<span data-ttu-id="a5fa6-335">Currying f (x, y) ≡ f (x) (y)의 일반화로 부분 응용 프로그램의 생각에서 주로 파생 되는 입력 순서 지정 규칙을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-335">We recommend an input ordering conventions that largely derives from thinking of partial application as a generalization of currying 𝑓(𝑥, 𝑦) ≡ 𝑓(𝑥)(𝑦).</span></span>
<span data-ttu-id="a5fa6-336">따라서 첫 번째 인수를 부분적으로 적용 하면 적절 한 경우 항상 적절 한 권한으로 사용할 수 있는 호출 가능이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-336">Thus, partially applying the first arguments should result in a callable that is useful in its own right whenever that is reasonable.</span></span>
<span data-ttu-id="a5fa6-337">이 원칙에 따라 다음과 같은 인수 순서를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-337">Following this principle, consider using the following order of arguments:</span></span>

- <span data-ttu-id="a5fa6-338">각도, 거듭제곱 벡터 등의 호출 가능 하지 않은 클래식 인수</span><span class="sxs-lookup"><span data-stu-id="a5fa6-338">Classical non-callable arguments such as angles, vectors of powers, etc.</span></span>
- <span data-ttu-id="a5fa6-339">호출 가능 인수 (함수 및 인수)</span><span class="sxs-lookup"><span data-stu-id="a5fa6-339">Callable arguments (functions and arguments).</span></span>
  <span data-ttu-id="a5fa6-340">함수와 연산이 모두 인수로 사용 되는 경우 함수 뒤에 작업을 배치 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-340">If both functions and operations are taken as arguments, consider placing operations after functions.</span></span>
- <span data-ttu-id="a5fa6-341">,, 및와 비슷한 방식으로 호출 가능한 인수에 의해 처리 된 컬렉션 `Map` `Iter` `Enumerate` `Fold` 입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-341">Collections acted upon by callable arguments in a similar way to `Map`, `Iter`, `Enumerate`, and `Fold`.</span></span>
- <span data-ttu-id="a5fa6-342">컨트롤로 사용 되는 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-342">Qubit arguments used as controls.</span></span>
- <span data-ttu-id="a5fa6-343">대상으로 사용 되는 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-343">Qubit arguments used as targets.</span></span>

<span data-ttu-id="a5fa6-344">`ApplyPhaseEstimationIteration`각도와 oracle을 사용 하는 단계 추정에서 사용 하기 위한 작업을 고려 하 고, `Rz` 다른 배율 인수 배열에 의해 수정 된 각도를 전달한 다음 oracle의 응용 프로그램을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-344">Consider an operation `ApplyPhaseEstimationIteration` for use in phase estimation that takes an angle and an oracle, passes the angle to `Rz` modified by an array of different scaling factors, and then controls applications of the oracle.</span></span>
<span data-ttu-id="a5fa6-345">입력은 `ApplyPhaseEstimationIteration` 다음과 같은 방식으로 정렬 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-345">We would order the inputs to `ApplyPhaseEstimationIteration` in the following fashion:</span></span>

```qsharp
operation ApplyPhaseEstimationIteration(
    angle : Double,
    callable : (Qubit => () is Ctl),
    scaleFactors : Double[],
    controlQubit : Qubit,
    targetQubits : Qubit[]
)
: Unit
...
```
<span data-ttu-id="a5fa6-346">갑작스러운 문제를 최소화 하는 특별 한 경우에는 일부 함수 및 작업이 기본 제공 함수 및의 동작을 모방 합니다 `Adjoint` `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-346">As a special case of minimizing surprise, some functions and operations mimic the behavior of the built-in functors `Adjoint` and `Controlled`.</span></span>
<span data-ttu-id="a5fa6-347">예를 들어,에는 `ControlledOnInt<'T>` `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)` `ControlledOnInt<Qubit[]>(5, _)` 함수 처럼 작동 `Controlled` 하지만 컨트롤 레지스터가 상태 $ \ket {5} = \ket $를 나타내는 조건의 {101} 형식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-347">For instance, `ControlledOnInt<'T>` has type `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)`, such that `ControlledOnInt<Qubit[]>(5, _)` acts like the `Controlled` functor, but on the condition that the control register represents the state $\ket{5} = \ket{101}$.</span></span>
<span data-ttu-id="a5fa6-348">따라서 개발자는 호출 되는 호출을 마지막으로 변환 하는 입력을 예상 하 `ControlledOnInt` 고 그 `(Qubit[], 'T)` 다음에 함수 출력을 사용 하는 것과 동일한 순서로 결과 작업을 입력---합니다 `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-348">Thus, a developer expects that the inputs to `ControlledOnInt` place the callable being transformed last, and that the resulting operation takes as its input `(Qubit[], 'T)` --- the same order as followed by the output of the `Controlled` functor.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="a5fa6-349">지침</span><span class="sxs-lookup"><span data-stu-id="a5fa6-349">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="a5fa6-350">다음을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-350">We suggest:</span></span>

- <span data-ttu-id="a5fa6-351">부분 응용 프로그램을 사용 하는 경우 입력 순서 일치를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-351">Use input orderings consistent with the use of partial application.</span></span>
- <span data-ttu-id="a5fa6-352">기본 제공 함수와 일치 하는 입력 순서을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-352">Use input orderings consistent with built-in functors.</span></span>
- <span data-ttu-id="a5fa6-353">모든 기존 입력을 퀀텀 입력 앞에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-353">Place all classical inputs before any quantum inputs.</span></span>

# <a name="examples"></a>[<span data-ttu-id="a5fa6-354">예</span><span class="sxs-lookup"><span data-stu-id="a5fa6-354">Examples</span></span>](#tab/examples)

_*_

## <a name="documentation-conventions"></a><span data-ttu-id="a5fa6-355">설명서 표기 규칙</span><span class="sxs-lookup"><span data-stu-id="a5fa6-355">Documentation Conventions</span></span> ##

<span data-ttu-id="a5fa6-356">:::no-loc(Q#):::이 언어를 사용 하면 특수 형식의 문서 주석을 사용 하 여 작업, 함수 및 사용자 정의 형식에 대 한 설명서를 첨부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-356">The :::no-loc(Q#)::: language allows for attaching documentation to operations, functions, and user-defined types through the use of specially formatted documentation comments.</span></span>
<span data-ttu-id="a5fa6-357">삼중 슬래시 ()로 표시 되는 `///` 이러한 설명서 주석은 각 작업, 함수 및 사용자 정의 형식, 각 작업의 용도를 설명 하는 데 사용할 수 있는 작은 [docfx-flavored Markdown](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) 문서입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-357">Denoted by triple-slashes (`///`), these documentation comments are small [DocFX-flavored Markdown](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) documents that can be used to describing the purpose of each operation, function, and user-defined type, what inputs each expects, and so forth.</span></span>
<span data-ttu-id="a5fa6-358">퀀텀 개발 키트와 함께 제공 되는 컴파일러는 이러한 주석을 추출 하 고이를 사용 하 여와 비슷한 조판 설명서를 제공 https://docs.microsoft.com/quantum 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-358">The compiler provided with the Quantum Development Kit extracts these comments and uses them to help typeset documentation similar to that at https://docs.microsoft.com/quantum.</span></span>
<span data-ttu-id="a5fa6-359">마찬가지로 퀀텀 개발 키트와 함께 제공 되는 언어 서버는 이러한 주석을 사용 하 여 코드에서 기호를 마우스로 가리킬 때 사용자에 게 도움을 제공 합니다 :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-359">Similarly, the language server provided with the Quantum Development Kit uses these comments to provide help to users when they hover over symbols in their :::no-loc(Q#)::: code.</span></span>
<span data-ttu-id="a5fa6-360">따라서 문서 주석을 사용 하면이 문서의 다른 규칙을 사용 하 여 쉽게 표현 되지 않는 세부 정보에 대 한 유용한 참조를 제공 하 여 사용자가 코드를 이해 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-360">Making use of documentation comments can thus help users to make sense of code by providing a useful reference for details that are not easily expressed using the other conventions in this document.</span></span>

> [!div class="nextstepaction"]
> <span data-ttu-id="a5fa6-361">[문서 주석 구문 참조](xref:microsoft.quantum.guide.filestructure#documentation-comments)입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-361">[Documentation comment syntax reference](xref:microsoft.quantum.guide.filestructure#documentation-comments).</span></span>

<span data-ttu-id="a5fa6-362">이 기능을 효과적으로 사용 하 여 사용자를 돕기 위해 문서 주석을 작성할 때 몇 가지 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-362">In order to effectively use this functionality to help users, we recommend keeping a few things in mind as you write documentation comments.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="a5fa6-363">지침</span><span class="sxs-lookup"><span data-stu-id="a5fa6-363">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="a5fa6-364">다음을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-364">We suggest:</span></span>

- <span data-ttu-id="a5fa6-365">각 public 함수, 작업 및 사용자 정의 형식은 문서 주석 바로 앞에와 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-365">Each public function, operation, and user-defined type should be immediately preceded by a documentation comment.</span></span>
- <span data-ttu-id="a5fa6-366">최소한 각 문서 주석에는 다음 섹션이 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-366">At a minimum, each documentation comment should include the following sections:</span></span>
    - <span data-ttu-id="a5fa6-367">요약</span><span class="sxs-lookup"><span data-stu-id="a5fa6-367">Summary</span></span>
    - <span data-ttu-id="a5fa6-368">입력</span><span class="sxs-lookup"><span data-stu-id="a5fa6-368">Input</span></span>
    - <span data-ttu-id="a5fa6-369">출력 (해당 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="a5fa6-369">Output (if applicable)</span></span>
- <span data-ttu-id="a5fa6-370">모든 요약이 두 문장 이내 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-370">Ensure that all summaries are two sentences or less.</span></span> <span data-ttu-id="a5fa6-371">더 많은 공간이 필요한 경우 `# Description` `# Summary` 전체 세부 정보를 사용 하 여 바로 다음 섹션을 제공 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-371">If more room is needed, provide a `# Description` section immediately following `# Summary` with complete details.</span></span>
- <span data-ttu-id="a5fa6-372">모든 클라이언트에서 요약에 TeX 표기법을 지 원하는 것이 아니라 적절 한 경우 요약에 수학을 포함 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-372">Where reasonable, do not include math in summaries, as not all clients support TeX notation in summaries.</span></span> <span data-ttu-id="a5fa6-373">Prose 문서를 작성 하는 경우 (예: TeX 또는 Markdown) 더 긴 줄 길이를 사용 하는 것이 더 적합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-373">Note that when writing prose documents (e.g. TeX or Markdown), it may be preferable to use longer line lengths.</span></span>
- <span data-ttu-id="a5fa6-374">섹션에서 관련 된 모든 수학 식을 제공 `# Description` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-374">Provide all relevant mathematical expressions in the `# Description` section.</span></span>
- <span data-ttu-id="a5fa6-375">입력을 설명할 때 컴파일러에서 유추할 수 있는 각 입력의 형식과 불일치를 발생 하는 위험을 반복 해 서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-375">When describing inputs, do not repeat the types of each input as these can be inferred by the compiler and risk introducing inconsistency.</span></span>
- <span data-ttu-id="a5fa6-376">각각의 고유한 섹션에서 적절 한 예제를 제공 `# Example` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-376">Provide examples as appropriate, each in their own `# Example` section.</span></span>
- <span data-ttu-id="a5fa6-377">코드를 나열 하기 전에 각 예제를 간략하게 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-377">Briefly describe each example before listing code.</span></span>
- <span data-ttu-id="a5fa6-378">섹션에서 관련 된 모든 교육용 게시 (예: 용지, proceedings of the, 블로그 게시물 및 대체 구현)를 `# References` 링크의 글머리 기호 목록으로 인용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-378">Cite all relevant academic publications (e.g.: papers, proceedings, blog posts, and alternative implementations) in a `# References` section as a bulleted list of links.</span></span>
- <span data-ttu-id="a5fa6-379">가능 하면 모든 인용 링크가 영구적이 고 변경할 수 없는 식별자 (DOIs 또는 버전이 지정 된 arXiv 번호)에 해당 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-379">Ensure that, where possible, all citation links are to permanent and immutable identifiers (DOIs or versioned arXiv numbers).</span></span>
- <span data-ttu-id="a5fa6-380">작업 또는 함수가 함수 변형에 의해 다른 작업 또는 함수와 관련 된 경우 섹션에서 다른 변형을 글머리 기호로 나열 `# See Also` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-380">When an operation or function is related to other operations or functions by functor variants, list other variants as bullets in the `# See Also` section.</span></span>
- <span data-ttu-id="a5fa6-381">수준-1 () 섹션 사이에 빈 주석 줄을 그대로 두고 `/// #` 수준-2 () 섹션 사이에 빈 줄을 남겨 둡니다 `/// ##` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-381">Leave a blank comment line between level-1 (`/// #`) sections, but do not leave a blank line between level-2 (`/// ##`) sections.</span></span>

# <a name="examples"></a>[<span data-ttu-id="a5fa6-382">예</span><span class="sxs-lookup"><span data-stu-id="a5fa6-382">Examples</span></span>](#tab/examples)

#### <a name=""></a><span data-ttu-id="a5fa6-383">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-383">☑</span></span> ####

```
/// # Summary
/// Applies a rotation about the X-axis by a given angle.
///
///
/// # Description
/// This operation rotates a single qubit by the unitary operation
/// \begin{align}
///     R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2}.
/// \end{align}
///
/// # Input
/// ## theta
/// Angle about which the qubit is to be rotated.
/// ## qubit
/// Qubit to which the gate should be applied.
///
/// # Remarks
/// Equivalent to:
/// ```qsharp
/// R(PauliX, theta, qubit);
/// ```
///
/// # See Also
/// - Ry
/// - Rz
operation Rx(theta : Double, qubit : Qubit) : Unit
is Adj + Ctl {
    body (...) { R(PauliX, theta, qubit); }
    adjoint (...) { R(PauliX, -theta, qubit); }
}
```

_*_

## <a name="formatting-conventions"></a><span data-ttu-id="a5fa6-384">서식 지정 규칙</span><span class="sxs-lookup"><span data-stu-id="a5fa6-384">Formatting Conventions</span></span> ##

<span data-ttu-id="a5fa6-385">앞의 제안 사항 외에도 일관 된 서식 지정 규칙을 사용 하는 코드를 가능한 한 이해 하기 쉽게 만드는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-385">In addition to the preceding suggestions, it is helpful to help make code as legible as possible to use consistent formatting rules.</span></span>
<span data-ttu-id="a5fa6-386">이러한 서식 지정 규칙은 본질적으로 임의로 임의적 이며 개인용 미관에 게 매우 강력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-386">Such formatting rules by nature tend to be somewhat arbitrary and strongly up to personal aesthetics.</span></span>
<span data-ttu-id="a5fa6-387">그럼에도 불구 하 고 작업자 그룹 내에 일관 된 서식 규칙 집합을 유지 하는 것이 좋습니다 :::no-loc(Q#)::: . 특히 퀀텀 개발 키트 자체와 같은 규모가 많은 프로젝트의 경우에는 특히 그렇습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-387">Nonetheless, we recommend maintaining a consistent set of formatting conventions within a group of collaborators, and especially for large :::no-loc(Q#)::: projects such as the Quantum Development Kit itself.</span></span>
<span data-ttu-id="a5fa6-388">이러한 규칙은 컴파일러와 통합 된 서식 지정 도구를 사용 하 여 자동으로 적용할 수 있습니다 :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-388">These rules can be automatically applied by using the formatting tool integrated with the :::no-loc(Q#)::: compiler.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="a5fa6-389">지침</span><span class="sxs-lookup"><span data-stu-id="a5fa6-389">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="a5fa6-390">다음을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-390">We suggest:</span></span>

- <span data-ttu-id="a5fa6-391">이식성을 위해 탭 대신 4 개의 공백을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-391">Use four spaces instead of tabs for portability.</span></span>
  <span data-ttu-id="a5fa6-392">예를 들어 VS Code에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-392">For instance, in VS Code:</span></span>
  ```json
    "editor.insertSpaces": true,
    "editor.tabSize": 4
  ```
- <span data-ttu-id="a5fa6-393">줄 바꿈이 적당 한 79 문자입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-393">Line wrap at 79 characters where reasonable.</span></span>
- <span data-ttu-id="a5fa6-394">이항 연산자 주위의 공백을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-394">Use spaces around binary operators.</span></span>
- <span data-ttu-id="a5fa6-395">형식 주석에 사용 되는 콜론의 양쪽에 공백을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-395">Use spaces on either side of colons used for type annotations.</span></span>
- <span data-ttu-id="a5fa6-396">배열 및 튜플 리터럴 (예: 함수 및 작업에 대 한 입력)에서 쉼표 뒤에 사용 되는 단일 공백을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-396">Use a single space after commas used in array and tuple literals (e.g.: in inputs to functions and operations).</span></span>
- <span data-ttu-id="a5fa6-397">함수, 작업 또는 UDT 이름 뒤에 공백을 사용 하거나 in 특성 선언 뒤에 공백을 사용 하지 마십시오 `@` .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-397">Do not use spaces after function, operation, or UDT names, or after the `@` in attribute declarations.</span></span>
- <span data-ttu-id="a5fa6-398">각 특성 선언은 별도의 줄에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-398">Each attribute declaration should be on its own line.</span></span>

# <a name="examples"></a>[<span data-ttu-id="a5fa6-399">예</span><span class="sxs-lookup"><span data-stu-id="a5fa6-399">Examples</span></span>](#tab/examples)

| &nbsp; | <span data-ttu-id="a5fa6-400">코드 조각</span><span class="sxs-lookup"><span data-stu-id="a5fa6-400">Snippet</span></span> | <span data-ttu-id="a5fa6-401">Description</span><span class="sxs-lookup"><span data-stu-id="a5fa6-401">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="a5fa6-402">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-402">☒</span></span> | <s>`2+3`</s> | <span data-ttu-id="a5fa6-403">이항 연산자 주위의 공백을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-403">Use spaces around binary operators.</span></span> |
| <span data-ttu-id="a5fa6-404">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-404">☒</span></span> | <s>`target:Qubit`</s> | <span data-ttu-id="a5fa6-405">형식 주석 콜론 앞뒤에 공백을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-405">Use spaces around type annotation colons.</span></span> |
| <span data-ttu-id="a5fa6-406">☑</span><span class="sxs-lookup"><span data-stu-id="a5fa6-406">☑</span></span> | `Example(a, b, c)` | <span data-ttu-id="a5fa6-407">입력 튜플의 항목은 가독성을 위해 정확 하 게 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-407">Items in input tuple are correctly spaced for readability.</span></span> |
| <span data-ttu-id="a5fa6-408">☒</span><span class="sxs-lookup"><span data-stu-id="a5fa6-408">☒</span></span> | <s>`Example (a, b, c)`</s> | <span data-ttu-id="a5fa6-409">함수, 작업 또는 UDT 이름 뒤에는 공백을 표시 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-409">Spaces should be suppressed after function, operation, or UDT names.</span></span> |

<span data-ttu-id="a5fa6-410">_\*\*</span><span class="sxs-lookup"><span data-stu-id="a5fa6-410">_\*\*</span></span>
