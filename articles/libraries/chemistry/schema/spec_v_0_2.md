---
title: Broombridge 스키마 사양 (ver 0.2)
description: Microsoft 퀀텀 화학 library에 대 한 Broombridge 퀀텀 화학 schema v 0.2의 사양에 대해 자세히 설명 합니다.
author: guanghaolow
ms.author: gulow@microsoft.com
ms.date: 05/28/2019
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_2
ms.openlocfilehash: df7e651b7d32e672c6e83346ff603132bd55c1a2
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907276"
---
# <a name="broombridge-specification-v02"></a><span data-ttu-id="b482c-103">Broombridge 사양 v 0.2</span><span class="sxs-lookup"><span data-stu-id="b482c-103">Broombridge Specification v0.2</span></span> #

<span data-ttu-id="b482c-104">이 문서에서 "REQUIRED", "NOT", "REQUIRED", "be", "not", "REQUIRED", "be", "REQUIRED", "be" 및 "OPTIONAL"은 [RFC 2119](https://tools.ietf.org/html/rfc2119)에 설명 된 대로 해석 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-104">The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span></span>

<span data-ttu-id="b482c-105">"참고", "정보" 또는 "경고"와 같은 제목이 있는 모든 사이드바는 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-105">Any sidebar with the headings "NOTE," "INFORMATION," or "WARNING" is informative.</span></span>

## <a name="introduction"></a><span data-ttu-id="b482c-106">소개</span><span class="sxs-lookup"><span data-stu-id="b482c-106">Introduction</span></span> ##

<span data-ttu-id="b482c-107">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-107">This section is informative.</span></span>

<span data-ttu-id="b482c-108">Broombridge 문서는 퀀텀 시뮬레이션 및 프로그래밍 도구 체인을 사용 하 여 처리 하기 위해 퀀텀 화학의 시뮬레이션 문제를 전달 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-108">Broombridge documents are intended to communicate instances of simulation problems in quantum chemistry for processing using quantum simulation and programming toolchains.</span></span>

## <a name="serialization"></a><span data-ttu-id="b482c-109">직렬화</span><span class="sxs-lookup"><span data-stu-id="b482c-109">Serialization</span></span> ##

<span data-ttu-id="b482c-110">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-110">This section is normative.</span></span>

<span data-ttu-id="b482c-111">Broombridge 문서는 [RFC 4627](https://tools.ietf.org/html/rfc4627) 섹션 2.2에 설명 된 대로 JSON 개체를 나타내는 [yaml 1.2 문서로](http://yaml.org/spec/) serialize 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-111">A Broombridge document MUST be serialized as a [YAML 1.2 document](http://yaml.org/spec/) representing a JSON object as described in [RFC 4627](https://tools.ietf.org/html/rfc4627) section 2.2.</span></span>
<span data-ttu-id="b482c-112">YAML로 serialize 된 개체에는 값이 `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"`되 고 JSON 스키마 초안-06 사양 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)]에 따라 유효 해야 하는 속성 `"$schema"` 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-112">The object serialized to YAML MUST have a property `"$schema"` whose value is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"`, and MUST be valid according to the JSON Schema draft-06 specifications [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span></span>

<span data-ttu-id="b482c-113">이 사양의 나머지 부분에서는 "Broombridge 개체"가 Broombridge YAML 문서에서 deserialize 된 JSON 개체를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-113">For the remainder of this specification, "the Broombridge object" will refer to the JSON object deserialized from a Broombridge YAML document.</span></span>

<span data-ttu-id="b482c-114">별도로 명시 하지 않는 한 개체에는이 문서에서 명시적으로 지정 된 속성 이외의 추가 속성을 포함 해서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-114">Unless otherwise explicitly noted, objects MUST NOT have additional properties beyond those specified explicitly in this document.</span></span>

## <a name="additional-definitions"></a><span data-ttu-id="b482c-115">추가 정의</span><span class="sxs-lookup"><span data-stu-id="b482c-115">Additional Definitions</span></span> ##

<span data-ttu-id="b482c-116">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-116">This section is normative.</span></span>

### <a name="quantity-objects"></a><span data-ttu-id="b482c-117">Quantity 개체</span><span class="sxs-lookup"><span data-stu-id="b482c-117">Quantity Objects</span></span> ###

<span data-ttu-id="b482c-118">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-118">This section is normative.</span></span>

<span data-ttu-id="b482c-119">_Quantity 개체_ 는 JSON 개체이 고 해당 값이 표 1에 나열 된 허용 되는 값 중 하나인 속성 `units` 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-119">A _quantity object_ is a JSON object, and MUST have a property `units` whose value is one of the allowed values listed in Table 1.</span></span>

<span data-ttu-id="b482c-120">Quantity 개체는 `units` 속성 외에도 `value` 단일 속성을 포함 하는 _단순 수량 개체_ 입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-120">A quantity object is a _simple quantity object_ if it has a single property `value` in addition to its `units` property.</span></span>
<span data-ttu-id="b482c-121">`value` 속성의 값은 숫자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-121">The value of the `value` property MUST be a number.</span></span>

<span data-ttu-id="b482c-122">Quantity 개체는 `units` 속성 외에도 `lower` 및 `upper` 속성이 있는 경우 _제한 된 수량 개체_ 입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-122">A quantity object is a _bounded quantity object_ if it has the properties `lower` and `upper` in addition to its `units` property.</span></span>
<span data-ttu-id="b482c-123">`lower` 및 `upper` 속성의 값은 숫자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-123">The values of the `lower` and `upper` properties MUST be numbers.</span></span>
<span data-ttu-id="b482c-124">제한 된 수량 개체에는 값이 숫자 인 속성 `value` 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-124">A bounded quantity object MAY have a property `value` whose value is a number.</span></span>

<span data-ttu-id="b482c-125">Quantity 개체는 속성 `format` 있고 속성 `values` `units` 속성 외에도 있는 경우 _스파스 배열 수량 개체_ 입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-125">A quantity object is a _sparse array quantity object_ if it has the property `format` and a property `values` in addition to its `units` property.</span></span>
<span data-ttu-id="b482c-126">`format` 값은 `sparse`문자열 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-126">The value of `format` MUST be the string `sparse`.</span></span>
<span data-ttu-id="b482c-127">`values` 속성의 값은 배열 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-127">The value of the `values` property MUST be an array.</span></span>
<span data-ttu-id="b482c-128">`values`의 각 요소는 스파스 배열 수량의 인덱스 및 값을 나타내는 배열 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-128">Each element of `values` MUST be an array representing the indices and value of the sparse array quantity.</span></span>

<span data-ttu-id="b482c-129">스파스 배열 수량 개체의 각 요소에 대 한 인덱스는 전체 스파스 배열 수량 개체에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-129">The indices for each element of a sparse array quantity object MUST be unique across the entire sparse array quantity object.</span></span>
<span data-ttu-id="b482c-130">`0`값이 포함 된 인덱스가 있는 경우 파서는 스파스 배열 수량 개체를 해당 인덱스가 전혀 없는 스파스 배열 수량 개체와 동일 하 게 처리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-130">If an index is present with a value of `0`, a parser MUST treat the sparse array quantity object identically to a sparse array quantity object in which that index is not present at all.</span></span>


<span data-ttu-id="b482c-131">Quantity 개체는 다음 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-131">A quantity object MUST either be</span></span>

- <span data-ttu-id="b482c-132">단순 수량 개체</span><span class="sxs-lookup"><span data-stu-id="b482c-132">a simple quantity object,</span></span>
- <span data-ttu-id="b482c-133">제한 된 수량 개체 또는</span><span class="sxs-lookup"><span data-stu-id="b482c-133">a bounded quantity object, or</span></span>
- <span data-ttu-id="b482c-134">스파스 배열 수량 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-134">a sparse array quantity object.</span></span>


### <a name="examples"></a><span data-ttu-id="b482c-135">예</span><span class="sxs-lookup"><span data-stu-id="b482c-135">Examples</span></span> ###

<span data-ttu-id="b482c-136">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-136">This section is informative.</span></span>

<span data-ttu-id="b482c-137">$1.9844146837\,\mathrm{Ha} $를 나타내는 단순 수량입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-137">A simple quantity representing $1.9844146837\,\mathrm{Ha}$:</span></span>

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

<span data-ttu-id="b482c-138">간격 $ [-7,-6]\,\mathrm{Ha} $에 대 한 균일 분포를 나타내는 제한 된 수량입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-138">A bounded quantity representing a uniform distribution over the interval $[-7, -6]\,\mathrm{Ha}$:</span></span>

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

<span data-ttu-id="b482c-139">다음은 요소가 `hello`와 동일 `[1, 2]` 스파스 배열 수량과 `world`와 같은 요소 `[3, 4]`입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-139">The following is a sparse array quantity with an element `[1, 2]` equal to `hello` and an element `[3, 4]` equal to `world`:</span></span>

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a><span data-ttu-id="b482c-140">서식 섹션</span><span class="sxs-lookup"><span data-stu-id="b482c-140">Format Section</span></span> ##

<span data-ttu-id="b482c-141">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-141">This section is normative.</span></span>

<span data-ttu-id="b482c-142">Broombridge 개체에는 값이 `version`라는 하나의 속성이 있는 JSON 개체인 속성 `format` 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-142">The Broombridge object MUST have a property `format` whose value is a JSON object with one property called `version`.</span></span>
<span data-ttu-id="b482c-143">`version` 속성에 `"0.2"`값이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-143">The `version` property MUST have the value `"0.2"`.</span></span>

### <a name="example"></a><span data-ttu-id="b482c-144">예제</span><span class="sxs-lookup"><span data-stu-id="b482c-144">Example</span></span> ###

<span data-ttu-id="b482c-145">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-145">This section is informative.</span></span>

```yaml
format:                        # required
    version: "0.2"             # must match exactly
```

## <a name="problem-description-section"></a><span data-ttu-id="b482c-146">문제 설명 섹션</span><span class="sxs-lookup"><span data-stu-id="b482c-146">Problem Description Section</span></span> ##

<span data-ttu-id="b482c-147">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-147">This section is normative.</span></span>

<span data-ttu-id="b482c-148">Broombridge 개체에는 값이 JSON 배열인 속성 `problem_description` 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-148">The Broombridge object MUST have a property `problem_description` whose value is a JSON array.</span></span>
<span data-ttu-id="b482c-149">`problem_description` 속성 값의 각 항목은이 섹션의 나머지 부분에 설명 된 대로 하나의 정수 집합을 설명 하는 JSON 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-149">Each item in the value of the `problem_description` property MUST be a JSON object describing one set of integrals, as described in the remainder of this section.</span></span>
<span data-ttu-id="b482c-150">이 섹션의 나머지 부분에서 "문제 설명 개체" 라는 용어는 Broombridge 개체의 `problem_description` 속성 값에 있는 항목을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-150">In the remainder of this section, the term "problem description object" will refer to an item in the value of the `problem_description` property of the Broombridge object.</span></span>

<span data-ttu-id="b482c-151">각 문제 설명 개체에는 해당 값이 JSON 개체인 속성 `metadata` 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-151">Each problem description object MUST have a property `metadata` whose value is a JSON object.</span></span>
<span data-ttu-id="b482c-152">`metadata` 값은 빈 JSON 개체 (`{}`) 이거나 구현자에서 정의 된 추가 속성을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-152">The value of `metadata` MAY be the empty JSON object (that is, `{}`), or MAY contain additional properties defined by the implementor.</span></span>

### <a name="hamiltonian-section"></a><span data-ttu-id="b482c-153">Hamiltonian 섹션</span><span class="sxs-lookup"><span data-stu-id="b482c-153">Hamiltonian Section</span></span> ###

#### <a name="overview"></a><span data-ttu-id="b482c-154">개요</span><span class="sxs-lookup"><span data-stu-id="b482c-154">Overview</span></span> ####

<span data-ttu-id="b482c-155">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-155">This section is informative.</span></span>

<span data-ttu-id="b482c-156">각 문제 설명 개체의 `hamiltonian` 속성은 특정 퀀텀 화학 문제에 대 한 Hamiltonian에 대 한 설명으로, 한 개 및 두 개의 본문 용어를 실수의 스파스 배열로 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-156">The `hamiltonian` property of each problem description object describes the Hamiltonian for a particular quantum chemistry problem by listing out its one- and two-body terms as sparse arrays of real numbers.</span></span>
<span data-ttu-id="b482c-157">각 문제 설명 개체에서 설명 하는 Hamiltonian 연산자는 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-157">The Hamiltonian operators described by each problem description object take the form</span></span>

<span data-ttu-id="b482c-158">$ $ H = \sum\_\{i, j\}\sum\_{\sigma\in\\{\uparrow, \down화살표\\}} H\_\{ij\} a ^\{\sum\}\_{i, \sigma} a\_{j, \sigma} + \frac{1}{2}\sum\_\{i, j, k, l\}\sum\_{\sum, \rho\in\\{ijkl, \down화살표\\}} H\_{} a ^ \sum\_{i , \sigma} a ^ \dagger\_{k, \rho} a\_{l, \rho} a\_{j,, $ $</span><span class="sxs-lookup"><span data-stu-id="b482c-158">$$ H = \sum\_\{i,j\}\sum\_{\sigma\in\\{\uparrow,\downarrow\\}} h\_\{ij\} a^\{\dagger\}\_{i,\sigma} a\_{j,\sigma} + \frac{1}{2}\sum\_\{i,j,k,l\}\sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}} h\_{ijkl} a^\dagger\_{i,\sigma} a^\dagger\_{k,\rho} a\_{l,\rho} a\_{j,\sigma}, $$</span></span>

<span data-ttu-id="b482c-159">여기에서 _ {ijkl} = (ij | kl) $ in Mulliken 규칙을 $h 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-159">here $h_{ijkl}= (ij|kl)$ in Mulliken convention.</span></span>

<span data-ttu-id="b482c-160">명확 하 게 하기 위해 1-전자 용어는</span><span class="sxs-lookup"><span data-stu-id="b482c-160">For clarity, the one-electron term is</span></span>

<span data-ttu-id="b482c-161">$ $ h_ {ij} = \int {\mathrm d} x \int ^ \*\_i (x) \int (\frac{1}{2}\nabla ^ 2 + \int\_{A} \frac{Z\_A} {| x-x\_A |}  \right) \right\_j (x), $ $</span><span class="sxs-lookup"><span data-stu-id="b482c-161">$$ h_{ij} = \int {\mathrm d}x \psi^\*\_i(x) \left(\frac{1}{2}\nabla^2 + \sum\_{A}\frac{Z\_A}{|x-x\_A|}  \right) \psi\_j(x), $$</span></span>

<span data-ttu-id="b482c-162">그리고 두 전자 단어는</span><span class="sxs-lookup"><span data-stu-id="b482c-162">and the two-electron term is</span></span>

<span data-ttu-id="b482c-163">$ $ h\_\{ijkl\} = \iint \{\mathrm d\}x ^ 2 \psi ^\{\*\}\_\_i (x\_1) \psi\_j (x 1) \iint\{1\}\{\|x\_1-x\_2\|\}\_psi\{k ^ \*\}\_(x\_2) \psi\_l (x 2).</span><span class="sxs-lookup"><span data-stu-id="b482c-163">$$ h\_\{ijkl\} = \iint \{\mathrm d\}x^2 \psi^\{\*\}\_i(x\_1)\psi\_j(x\_1) \frac\{1\}\{\|x\_1 -x\_2\|\}\psi\_k^\{\*\}(x\_2) \psi\_l(x\_2).</span></span>
$$

<span data-ttu-id="b482c-164">`integral_sets` 속성의 각 요소에 대 한 [`basis_set` 속성](#basis-set-object) 에 대 한 설명에 설명 된 대로, 사용 되는 기본 함수는 실제 값 이라고 명확 하 게 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-164">As noted in our description of the [`basis_set` property](#basis-set-object) of each element of the `integral_sets` property, we further explicitly assume that the basis functions used are real-valued.</span></span>
<span data-ttu-id="b482c-165">이를 통해 용어 사이에 다음 symmetries를 사용 하 여 Hamiltonian 표현을 압축할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-165">This allows us to use the following symmetries between the terms to compress the representation of the Hamiltonian.</span></span>

<span data-ttu-id="b482c-166">$ $ h_ {ijkl} = h_ {ijlk} = h_ {jikl} = h_ {jilk} = h_ {klij} = h_ {klji} = h_ {lkij} = h_ {lkji}.</span><span class="sxs-lookup"><span data-stu-id="b482c-166">$$ h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkij}=h_{lkji}.</span></span>
$$


#### <a name="contents"></a><span data-ttu-id="b482c-167">콘텐츠</span><span class="sxs-lookup"><span data-stu-id="b482c-167">Contents</span></span> ####

<span data-ttu-id="b482c-168">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-168">This section is normative.</span></span>

<span data-ttu-id="b482c-169">각 문제 설명 개체에는 해당 값이 JSON 개체인 속성 `hamiltonian` 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-169">Each problem description object MUST have a property `hamiltonian` whose value is a JSON object.</span></span>
<span data-ttu-id="b482c-170">`hamiltonian` 속성의 값은 Hamiltonian 개체 라고 하며,이 섹션의 나머지 부분에 설명 된 대로 `one_electron_integrals` 및 `two_electron_integrals` 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-170">The value of the `hamiltonian` property is known as a Hamiltonian object, and MUST have the properties `one_electron_integrals` and `two_electron_integrals` as described in the remainder of this section.</span></span>

<span data-ttu-id="b482c-171">각 문제 설명 개체에는 값이 단순 수량 개체 인 속성 `coulomb_repulsion` 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-171">Each problem description object MUST have a property `coulomb_repulsion` whose value is a simple quantity object.</span></span>
<span data-ttu-id="b482c-172">각 문제 설명 개체에는 값이 단순 수량 개체 인 속성 `energy_offet` 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-172">Each problem description object MUST have a property `energy_offet` whose value is a simple quantity object.</span></span>
> <span data-ttu-id="b482c-173">두고 `coulomb_repulsion` 및 `energy_offet` 값을 함께 추가 하 여 Hamiltonian의 id 용어를 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-173">[NOTE] The values of `coulomb_repulsion` and `energy_offet` added together capture the identity term of the Hamiltonian.</span></span>

##### <a name="one-electron-integrals-object"></a><span data-ttu-id="b482c-174">1-전자 정수 개체</span><span class="sxs-lookup"><span data-stu-id="b482c-174">One-Electron Integrals Object</span></span> #####

<span data-ttu-id="b482c-175">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-175">This section is normative.</span></span>

<span data-ttu-id="b482c-176">Hamiltonian 개체의 `one_electron_integrals` 속성은 인덱스가 두 정수이 고 해당 값이 숫자인 스파스 배열 수량 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-176">The `one_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity whose indices are two integers and whose values are numbers.</span></span>
<span data-ttu-id="b482c-177">모든 용어에는 `i >= j``[i, j]` 인덱스가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-177">Every term MUST have indices `[i, j]` where `i >= j`.</span></span>

> <span data-ttu-id="b482c-178">두고 이는 Hamiltonian가 Hermitian의 결과로 _ {ij} = h_ {ji} $ $h 하는 대칭을 반영 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-178">[NOTE] This reflects the symmetry that $h_{ij} = h_{ji}$ which is a consequence of the fact that the Hamiltonian is Hermitian.</span></span>


###### <a name="example"></a><span data-ttu-id="b482c-179">예제</span><span class="sxs-lookup"><span data-stu-id="b482c-179">Example</span></span> ######

<span data-ttu-id="b482c-180">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-180">This section is informative.</span></span>

<span data-ttu-id="b482c-181">다음 스파스 배열 수량은 Hamiltonian $ $ H = \left (-5.0 (a ^\{\left \_{1을 나타냅니다.\_{1, \uparrow} + a ^\{\left\}\_{1, \downarrow} a\_{1, \downarrow}) + 0.17 (a ^\{\left\}\_{2, \uparrow} a\_{1, \uparrow} + a ^\{\left\}\_{1, a\_{2, + a ^\{\left\}\_{2 , \downarrow} a\_{1, \downarrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{2, \downarrow}) \dagger)\\,\}</span><span class="sxs-lookup"><span data-stu-id="b482c-181">The following sparse array quantity represents the Hamiltonian $$ H = \left(-5.0  (a^\{\dagger\}\_{1,\uparrow} a\_{1,\uparrow}+a^\{\dagger\}\_{1,\downarrow} a\_{1,\downarrow})+ 0.17 (a^\{\dagger\}\_{2,\uparrow} a\_{1,\uparrow}+ a^\{\dagger\}\_{1,\uparrow} a\_{2,\uparrow}+a^\{\dagger\}\_{2,\downarrow} a\_{1,\downarrow}+ a^\{\dagger\}\_{1,\downarrow} a\_{2,\downarrow})\right)\\,\mathrm{Ha}.</span></span>
$$

```yaml
one_electron_integrals:     # required
    units: hartree          # required
    format: sparse          # required
    values:                 # required
        # i j f(i,j)
        - [1, 1, -5.0]
        - [2, 1,  0.17]
```
> [!NOTE]
> <span data-ttu-id="b482c-182">Broombridge는 1부터 기반으로 하는 인덱싱을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-182">Broombridge uses 1-based indexing.</span></span>


##### <a name="two-electron-integrals-object"></a><span data-ttu-id="b482c-183">2-전자 정수 개체</span><span class="sxs-lookup"><span data-stu-id="b482c-183">Two-Electron Integrals Object</span></span> #####

<span data-ttu-id="b482c-184">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-184">This section is normative.</span></span>

<span data-ttu-id="b482c-185">Hamiltonian 개체의 `two_electron_integrals` 속성은 `index_convention`라는 하나 이상의 추가 속성이 있는 스파스 배열 수량 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-185">The `two_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity with one additional property called `index_convention`.</span></span>
<span data-ttu-id="b482c-186">`two_electron_integrals` 값의 각 요소에는 네 개의 인덱스가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-186">Each element of the value of `two_electron_integrals` MUST have four indices.</span></span>

<span data-ttu-id="b482c-187">각 `two_electron_integrals` 속성에는 `index_convention` 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-187">Each `two_electron_integrals` property MUST have a `index_convention` property.</span></span>
<span data-ttu-id="b482c-188">`index_convention` 속성의 값은 표 1에 나열 된 허용 되는 값 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-188">The value of the `index_convention` property MUST be one of the allowed values listed in Table 1.</span></span>
<span data-ttu-id="b482c-189">`index_convention` 값이 `mulliken`되는 경우 스파스 배열 수량 `two_electron_integrals`의 각 요소에 대해 Broombridge 문서를 로드 하는 파서는 두 전자 $h 연산자 (_ {i)와 같은 Hamiltonian 항을 인스턴스화해야 합니다. j, k, l} a ^ \ dagger_i a ^ \ dagger_j a_k a_l $. 여기서 $i $, $j $, $k $ 및 $l $는 값의 정수 여야 하며, 여기서 $h _ {i, j, k, l} $은 스파스 배열 수량의 요소 `[i, j, k, l, h(i, j, k, l)]`입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-189">If the value of `index_convention` is `mulliken`, then for each element of the `two_electron_integrals` sparse array quantity, a parser loading a Broombridge document MUST instantiate a Hamiltonian term equal to the two-electron operator $h_{i, j, k, l} a^\dagger_i a^\dagger_j a_k a_l$, where $i$, $j$, $k$, and $l$ MUST be integers of value at least 1, and where $h_{i, j, k, l}$ is the element `[i, j, k, l, h(i, j, k, l)]` of the sparse array quantity.</span></span>

###### <a name="symmetries"></a><span data-ttu-id="b482c-190">Symmetries</span><span class="sxs-lookup"><span data-stu-id="b482c-190">Symmetries</span></span> ######

<span data-ttu-id="b482c-191">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-191">This section is normative.</span></span>

<span data-ttu-id="b482c-192">`two_electron_integrals` 개체의 `index_convention` 속성이 `mulliken`와 같으면 인덱스가 `[i, j, k, l]` 인 요소가 있는 경우 다음 인덱스는 `[i, j, k, l]`와 같지 않은 경우에는 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-192">If the `index_convention` property of a `two_electron_integrals` object is equal to `mulliken`, then if an element with indices `[i, j, k, l]` is present, the following indices MUST NOT be present unless they are equal to `[i, j, k, l]`:</span></span>

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> <span data-ttu-id="b482c-193">`index_convention` 속성이 스파스 수량 개체 이기 때문에 다른 요소에 대해 인덱스가 반복 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-193">Because the `index_convention` property is a sparse quantity object, no indices may be repeated on different elements.</span></span>
> <span data-ttu-id="b482c-194">특히 `[i, j, k, l]` 인덱스를 사용 하는 요소가 있는 경우 다른 요소는 해당 인덱스를 가질 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-194">In particular, if an element with indices `[i, j, k, l]` is present, no other element may have those indices.</span></span>


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a><span data-ttu-id="b482c-195">예제</span><span class="sxs-lookup"><span data-stu-id="b482c-195">Example</span></span> #######

<span data-ttu-id="b482c-196">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-196">This section is informative.</span></span>

<span data-ttu-id="b482c-197">다음 개체는 Hamiltonian를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-197">The following object specifies the Hamiltonian</span></span>

<span data-ttu-id="b482c-198">$ $ H = \frac12 \sum\_{\sum, \rho\in\\{\uparrow, \downi\\}} \Ampgr (1.6 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{1, \rho} a\_{1, \rho} a\_{1, \sigma}-0.1 a ^ {\dagger}\_{6, \sigma} a ^ {\dagger}\_{1, \rho} a\_{3, \rho} a\_{2, \sigma}-0.1 a ^ {\dagger}\_{6, \sigma} a ^ {\dagger}\_{1, \rho} a\_{2 , \rho} a\_{3, \sigma}-0.1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{3, \rho} a\_{2, \sigma}-0.1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{2, \rho} a\_{3, \sigma} $ $ $ $-0.1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2, \rho} a\_{6, \rho} a\_{1, \sigma}-0.1 a ^ {\dagger}\_{3 , \sigma} a ^ {\dagger}\_{2, \rho} a\_{1, \rho}\_{6, \sigma}-0.1 a ^ {\dagger}\_{2, \sigma} a ^ {\dagger}\_{3, \rho} a\_{6, \rho} a\_{1, \sigma}-0.1 a ^ {\dagger}\_{2, \sigma} a ^ {\dagger}\_{3, \rho} a\_{1, \rho} a\_{6, \sigma}\Biggr)\\, \textrm{Ha}.</span><span class="sxs-lookup"><span data-stu-id="b482c-198">$$ H = \frac12 \sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}}\Biggr( 1.6 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{1,\rho} a\_{1,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{2,\rho} a\_{3,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{2,\rho} a\_{3,\sigma} $$ $$- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{1,\rho} a\_{6,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{1,\rho} a\_{6,\sigma}\Biggr)\\,\textrm{Ha}.</span></span>
$$

```yaml
two_electron_integrals:
    index_convention: mulliken
    units: hartree
    format: sparse
    values:
        - [1, 1, 1, 1,  1.6]
        - [6, 1, 3, 2, -0.1]
```

### <a name="initial-state-section"></a><span data-ttu-id="b482c-199">초기 상태 섹션</span><span class="sxs-lookup"><span data-stu-id="b482c-199">Initial State Section</span></span> ###

<span data-ttu-id="b482c-200">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-200">This section is normative.</span></span>

<span data-ttu-id="b482c-201">값이 JSON 배열인 `initial_state_suggestion` 개체는 지정 된 Hamiltonian에 대 한 관심의 초기 퀀텀 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-201">The `initial_state_suggestion` object whose value is a JSON array specifies initial quantum states of interest to the specified Hamiltonian.</span></span> <span data-ttu-id="b482c-202">`initial_state_suggestion` 속성 값의 각 항목은이 섹션의 나머지 부분에 설명 된 대로 하나의 퀀텀 상태를 설명 하는 JSON 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-202">Each item in the value of the `initial_state_suggestion` property MUST be a JSON object describing one quantum state, as described in the remainder of this section.</span></span>
<span data-ttu-id="b482c-203">이 섹션의 나머지 부분에서 "상태 개체" 라는 용어는 Broombridge 개체의 `initial_state_suggestion` 속성 값에 있는 항목을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-203">In the remainder of this section, the term "state object" will refer to an item in the value of the `initial_state_suggestion` property of the Broombridge object.</span></span>

#### <a name="state-object"></a><span data-ttu-id="b482c-204">상태 개체</span><span class="sxs-lookup"><span data-stu-id="b482c-204">State object</span></span> ####

<span data-ttu-id="b482c-205">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-205">This section is normative.</span></span>

<span data-ttu-id="b482c-206">각 상태 개체에는 문자열을 포함 하는 `label` 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-206">Each state object MUST have a `label` property containing a string.</span></span> <span data-ttu-id="b482c-207">각 상태 개체에는 `method` 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-207">Each state object MUST have a `method` property.</span></span> <span data-ttu-id="b482c-208">`method` 속성의 값은 표 3에 나열 된 허용 되는 값 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-208">The value of the `method` property MUST be one of the allowed values listed in Table 3.</span></span>
<span data-ttu-id="b482c-209">각 상태 개체에는 값이 단순 수량 개체 여야 하는 `energy` 속성이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-209">Each state object MAY have a property `energy` whose value MUST be a simple quantity object.</span></span>

<span data-ttu-id="b482c-210">`method` 속성의 값이 `sparse_multi_configurational`인 경우 상태 개체에는 기본 상태 배열과 정규화 되지 않은 amplitudes을 포함 하는 `superposition` 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-210">If the value of the `method` property is `sparse_multi_configurational`, the state object MUST have a `superposition` property containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="b482c-211">예를 들어 초기 상태 $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0} $ $ $ $ \ket{E} = \frac{0.1 (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) + 0.2 (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \uparrow}a ^ {\dagger}\_{2, \downarrow})} {\sqrt{| 0.1 | ^ 2 + | 0.2 | ^ 2}} \ket{0}, $ $ where $ \ket{E} $에는 에너지 $0.987 \textrm{Ha} $가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-211">For example, the initial states $$ \ket{G0}=\ket{G1}=\ket{G2}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0} $$ $$ \ket{E}=\frac{0.1 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})+0.2 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\uparrow}a^{\dagger}\_{2,\downarrow})}{\sqrt{|0.1|^2+|0.2|^2}}\ket{0}, $$ where $\ket{E}$ has energy $0.987 \textrm{Ha}$, are represented by</span></span>
```yaml
initial_state_suggestions: # optional. If not provided, spin-orbitals will be filled to minimize one-body diagonal term energies.
  - label: "|G0>"
    method: sparse_multi_configurational
    superposition:
      - [1.0, "(1a)+","(2a)+","(2b)+","|vacuum>"]
  - label: "|G1>"
    method: sparse_multi_configurational
    superposition:
      - [-1.0, "(2a)+","(1a)+","(2b)+","|vacuum>"]
  - label: "|G2>"
    method: sparse_multi_configurational
    superposition:
      - [1.0, "(3a)","(1a)+","(2a)+","(3a)+","(2b)+","|vacuum>"]
  - label: "|E>"
    energy: {units: hartree, value: 0.987}
    method: sparse_multi_configurational
    superposition:
      - [0.1, "(1a)+","(2a)+","(2b)+","|vacuum>"]
      - [0.2, "(1a)+","(3a)+","(2b)+","|vacuum>"]
```

<span data-ttu-id="b482c-212">`method` 속성의 값이 `unitary_coupled_cluster`인 경우 상태 개체에는 JSON 개체인 값을 갖는 `cluster_operator` 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-212">If the value of the `method` property is `unitary_coupled_cluster`, the state object MUST have a `cluster_operator` property whose value is a JSON object.</span></span>
<span data-ttu-id="b482c-213">JSON 개체에는 값이 기본 상태 인 `reference_state` 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-213">The JSON object MUST have a `reference_state` property whose value is a basis state.</span></span>
<span data-ttu-id="b482c-214">JSON 개체에는 값이 하나의 본문 클러스터 연산자와 해당 amplitudes 인 `one_body_amplitudes` 속성이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-214">The JSON object MAY have a `one_body_amplitudes` property whose value is an array of one-body cluster operators and their amplitudes.</span></span>
<span data-ttu-id="b482c-215">JSON 개체에는 두 개의 본문 클러스터 연산자와 해당 amplitudes의 배열인 값을 가진 `two_body_amplitudes` 속성이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-215">The JSON object MAY have a `two_body_amplitudes` property whose value is an array of two-body cluster operators and their amplitudes.</span></span>
<span data-ttu-id="b482c-216">기반 상태의 배열과 정규화 되지 않은 amplitudes을 포함 하는입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-216">containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="b482c-217">예를 들어 상태 $ $ \ket{\text{reference}} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0}, $ $</span><span class="sxs-lookup"><span data-stu-id="b482c-217">For example, the state $$ \ket{\text{reference}}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0}, $$</span></span>

<span data-ttu-id="b482c-218">$ $ \ket{\text{UCCSD}} = e ^ {T-T ^ \dagger}\ket{\text{reference}}, $ $</span><span class="sxs-lookup"><span data-stu-id="b482c-218">$$ \ket{\text{UCCSD}}=e^{T-T^\dagger}\ket{\text{reference}}, $$</span></span>

<span data-ttu-id="b482c-219">$ $ T = 0.1 a ^ {\dagger}\_{3, \uparrow}a\_{2, \downarrow} + 0.2 a ^ {\dagger}\_{2, \uparrow}a\_{2, \downarrow}-0.3 a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \downarrow}a\_{3, \uparrow}a\_{2, \downarrow} $ $는 다음으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-219">$$ T = 0.1 a^{\dagger}\_{3,\uparrow}a\_{2,\downarrow} + 0.2 a^{\dagger}\_{2,\uparrow}a\_{2,\downarrow} - 0.3 a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\downarrow}a\_{3,\uparrow}a\_{2,\downarrow} $$ is represented by</span></span>
```yaml
initial_state_suggestions: # optional. If not provided, spin-orbitals will be filled to minimize one-body diagonal term energies.
  - label: "UCCSD"
    method: unitary_coupled_cluster
    cluster_operator: # Initial state that cluster operator is applied to.
        reference_state: 
          [1.0, "(1a)+", "(2a)+", "(2b)+", '|vacuum>']
        one_body_amplitudes: # A one-body cluster term is t^{q}_{p} a^\dag_p a_q   
            - [0.1, "(3a)+", "(2b)"]
            - [-0.2, "(2a)+", "(2b)"]
        two_body_amplitudes: # A two-body unitary cluster term is t^{rs}_{pq} a^\dag_p a^\dag_q a_r a_s
            - [-0.3, "(1a)+", "(3b)+", "(3a)", "(2b)"]
```

#### <a name="basis-set-object"></a><span data-ttu-id="b482c-220">기본 설정 개체</span><span class="sxs-lookup"><span data-stu-id="b482c-220">Basis Set Object</span></span> ####

<span data-ttu-id="b482c-221">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-221">This section is normative.</span></span>

<span data-ttu-id="b482c-222">각 문제 설명 개체에 `basis_set` 속성이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-222">Each problem description object MAY have a `basis_set` property.</span></span>
<span data-ttu-id="b482c-223">`basis_set` 속성 값이 있는 경우 `type` 및 `name`라는 두 개의 속성이 있는 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-223">If present, the value of the `basis_set` property MUST be an object with two properties, `type` and `name`.</span></span>

<span data-ttu-id="b482c-224">`basis_set` 속성 값으로 식별 되는 기본 함수는 실제 값 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-224">The basis functions identified by the value of the `basis_set` property MUST be real-valued.</span></span>

> [!NOTE]
> <span data-ttu-id="b482c-225">이 사양의 이후 버전에서는 모든 기본 함수가 실제 값 이라고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-225">The assumption that all basis functions are real-valued may be relaxed in future versions of this specification.</span></span>

## <a name="tables-and-lists"></a><span data-ttu-id="b482c-226">테이블 및 목록</span><span class="sxs-lookup"><span data-stu-id="b482c-226">Tables and Lists</span></span> ##

### <a name="table-1-allowed-physical-units"></a><span data-ttu-id="b482c-227">표 1.</span><span class="sxs-lookup"><span data-stu-id="b482c-227">Table 1.</span></span> <span data-ttu-id="b482c-228">허용 된 물리적 단위</span><span class="sxs-lookup"><span data-stu-id="b482c-228">Allowed Physical Units</span></span> ###

<span data-ttu-id="b482c-229">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-229">This section is normative.</span></span>

<span data-ttu-id="b482c-230">단위를 지정 하는 문자열은 다음 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-230">Any string specifying a unit MUST be one of the following:</span></span>

- `hartree`
- `ev`

<span data-ttu-id="b482c-231">파서 및 생산자는 다음과 같은 단순 수량 개체를 동일 하 게 처리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-231">Parsers and producers MUST treat the following simple quantity objects as equivalent:</span></span>

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a><span data-ttu-id="b482c-232">테이블 2.</span><span class="sxs-lookup"><span data-stu-id="b482c-232">Table 2.</span></span> <span data-ttu-id="b482c-233">허용 되는 인덱스 규칙</span><span class="sxs-lookup"><span data-stu-id="b482c-233">Allowed Index Conventions</span></span> ###

<span data-ttu-id="b482c-234">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-234">This section is normative.</span></span>

<span data-ttu-id="b482c-235">인덱스 규칙을 지정 하는 문자열은 다음 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-235">Any string specifying an index convention MUST be one of the following:</span></span>

- `mulliken`

<span data-ttu-id="b482c-236">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-236">This section is informative.</span></span>

<span data-ttu-id="b482c-237">이 사양의 이후 버전에는 추가 인덱스 규칙이 도입 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-237">Additional index conventions may be introduced in future versions of this specification.</span></span>

#### <a name="interpretation-of-index-conventions"></a><span data-ttu-id="b482c-238">인덱스 규칙의 해석</span><span class="sxs-lookup"><span data-stu-id="b482c-238">Interpretation of Index Conventions</span></span> ####

<span data-ttu-id="b482c-239">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-239">This section is informative.</span></span>

### <a name="table-3-allowed-state-methods"></a><span data-ttu-id="b482c-240">표 3.</span><span class="sxs-lookup"><span data-stu-id="b482c-240">Table 3.</span></span> <span data-ttu-id="b482c-241">허용 되는 상태 메서드</span><span class="sxs-lookup"><span data-stu-id="b482c-241">Allowed State methods</span></span> ###

<span data-ttu-id="b482c-242">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-242">This section is normative.</span></span>

<span data-ttu-id="b482c-243">상태 메서드를 지정 하는 문자열은 다음 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-243">Any string specifying a state method MUST be one of the following:</span></span>

- `sparse_multi_configurational`
- `unitary_coupled_cluster`

<span data-ttu-id="b482c-244">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-244">This section is informative.</span></span>

<span data-ttu-id="b482c-245">추가 상태 메서드는이 사양의 이후 버전에서 도입 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b482c-245">Additional state methods may be introduced in future versions of this specification.</span></span>
