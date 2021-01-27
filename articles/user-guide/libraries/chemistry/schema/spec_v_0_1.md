---
title: Broombridge 스키마 사양 (ver 0.1)
description: Microsoft 퀀텀 화학 library에 대 한 Broombridge 퀀텀 화학 schema v 0.1의 사양에 대해 자세히 설명 합니다.
author: cgranade
ms.author: chgranad
ms.date: 10/17/2018
ms.topic: conceptual
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_1
no-loc:
- Q#
- $$v
ms.openlocfilehash: 0a306f59a823e76ba0518d023a41f1f9d5670e7a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858188"
---
# <a name="broombridge-specification-v01"></a><span data-ttu-id="adb6f-103">Broombridge 사양 v 0.1</span><span class="sxs-lookup"><span data-stu-id="adb6f-103">Broombridge Specification v0.1</span></span> #

<span data-ttu-id="adb6f-104">이 문서에서 "REQUIRED", "NOT", "REQUIRED", "be", "not", "REQUIRED", "be", "REQUIRED", "be" 및 "OPTIONAL"은 [RFC 2119](https://tools.ietf.org/html/rfc2119)에 설명 된 대로 해석 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-104">The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span></span>

<span data-ttu-id="adb6f-105">"참고", "정보" 또는 "경고"와 같은 제목이 있는 모든 사이드바는 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-105">Any sidebar with the headings "NOTE," "INFORMATION," or "WARNING" is informative.</span></span>

## <a name="introduction"></a><span data-ttu-id="adb6f-106">소개</span><span class="sxs-lookup"><span data-stu-id="adb6f-106">Introduction</span></span> ##

<span data-ttu-id="adb6f-107">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-107">This section is informative.</span></span>

<span data-ttu-id="adb6f-108">Broombridge 문서는 퀀텀 시뮬레이션 및 프로그래밍 도구 체인을 사용 하 여 처리 하기 위해 퀀텀 화학의 시뮬레이션 문제를 전달 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-108">Broombridge documents are intended to communicate instances of simulation problems in quantum chemistry for processing using quantum simulation and programming toolchains.</span></span>

## <a name="serialization"></a><span data-ttu-id="adb6f-109">Serialization</span><span class="sxs-lookup"><span data-stu-id="adb6f-109">Serialization</span></span> ##

<span data-ttu-id="adb6f-110">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-110">This section is normative.</span></span>

<span data-ttu-id="adb6f-111">Broombridge 문서는 [RFC 4627](https://tools.ietf.org/html/rfc4627) 섹션 2.2에 설명 된 대로 JSON 개체를 나타내는 [yaml 1.2 문서로](http://yaml.org/spec/) serialize 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-111">A Broombridge document MUST be serialized as a [YAML 1.2 document](http://yaml.org/spec/) representing a JSON object as described in [RFC 4627](https://tools.ietf.org/html/rfc4627) section 2.2.</span></span>
<span data-ttu-id="adb6f-112">YAML로 serialize 된 개체에는 값이 인 속성이 있어야 하며 `"$schema"` `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"` JSON 스키마 초안-06 사양 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)]에 따라 유효 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-112">The object serialized to YAML MUST have a property `"$schema"` whose value is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"`, and MUST be valid according to the JSON Schema draft-06 specifications [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span></span>

<span data-ttu-id="adb6f-113">이 사양의 나머지 부분에서는 "Broombridge 개체"가 Broombridge YAML 문서에서 deserialize 된 JSON 개체를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-113">For the remainder of this specification, "the Broombridge object" will refer to the JSON object deserialized from a Broombridge YAML document.</span></span>

<span data-ttu-id="adb6f-114">별도로 명시 하지 않는 한 개체에는이 문서에서 명시적으로 지정 된 속성 이외의 추가 속성을 포함 해서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-114">Unless otherwise explicitly noted, objects MUST NOT have additional properties beyond those specified explicitly in this document.</span></span>

## <a name="additional-definitions"></a><span data-ttu-id="adb6f-115">추가 정의</span><span class="sxs-lookup"><span data-stu-id="adb6f-115">Additional Definitions</span></span> ##

<span data-ttu-id="adb6f-116">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-116">This section is normative.</span></span>

### <a name="quantity-objects"></a><span data-ttu-id="adb6f-117">Quantity 개체</span><span class="sxs-lookup"><span data-stu-id="adb6f-117">Quantity Objects</span></span> ###

<span data-ttu-id="adb6f-118">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-118">This section is normative.</span></span>

<span data-ttu-id="adb6f-119">_Quantity 개체_ 는 JSON 개체 이며 `units` 값이 표 1에 나열 된 허용 되는 값 중 하나인 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-119">A _quantity object_ is a JSON object, and MUST have a property `units` whose value is one of the allowed values listed in Table 1.</span></span>

<span data-ttu-id="adb6f-120">Quantity 개체는 속성 외에도 단일 속성을 포함 하는 경우 _단순 수량 개체_ 입니다 `value` `units` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-120">A quantity object is a _simple quantity object_ if it has a single property `value` in addition to its `units` property.</span></span>
<span data-ttu-id="adb6f-121">속성의 값은 `value` 숫자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-121">The value of the `value` property MUST be a number.</span></span>

<span data-ttu-id="adb6f-122">Quantity 개체는 속성이  `lower` 있고 `upper` 속성 외에도 바인딩된 수량 개체입니다 `units` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-122">A quantity object is a _bounded quantity object_ if it has the properties `lower` and `upper` in addition to its `units` property.</span></span>
<span data-ttu-id="adb6f-123">및 속성의 값은 숫자 여야 합니다 `lower` `upper` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-123">The values of the `lower` and `upper` properties MUST be numbers.</span></span>
<span data-ttu-id="adb6f-124">제한 된 수량 개체에는 `value` 값이 숫자 인 속성이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-124">A bounded quantity object MAY have a property `value` whose value is a number.</span></span>

<span data-ttu-id="adb6f-125">Quantity 개체는 속성 및 속성을 포함 하는 _스파스 배열 수량 개체_ 입니다 `format` `values` `units` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-125">A quantity object is a _sparse array quantity object_ if it has the property `format` and a property `values` in addition to its `units` property.</span></span>
<span data-ttu-id="adb6f-126">값은 `format` 문자열 이어야 합니다 `sparse` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-126">The value of `format` MUST be the string `sparse`.</span></span>
<span data-ttu-id="adb6f-127">속성의 값은 `values` 배열 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-127">The value of the `values` property MUST be an array.</span></span>
<span data-ttu-id="adb6f-128">의 각 요소는 `values` 스파스 배열 수량의 인덱스 및 값을 나타내는 배열 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-128">Each element of `values` MUST be an array representing the indices and value of the sparse array quantity.</span></span>

<span data-ttu-id="adb6f-129">스파스 배열 수량 개체의 각 요소에 대 한 인덱스는 전체 스파스 배열 수량 개체에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-129">The indices for each element of a sparse array quantity object MUST be unique across the entire sparse array quantity object.</span></span>
<span data-ttu-id="adb6f-130">값을 포함 하는 인덱스가 있는 경우 `0` 파서는 스파스 배열 수량 개체를 해당 인덱스가 없는 스파스 배열 수량 개체와 동일 하 게 처리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-130">If an index is present with a value of `0`, a parser MUST treat the sparse array quantity object identically to a sparse array quantity object in which that index is not present at all.</span></span>


<span data-ttu-id="adb6f-131">Quantity 개체는 다음 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-131">A quantity object MUST either be</span></span>

- <span data-ttu-id="adb6f-132">단순 수량 개체</span><span class="sxs-lookup"><span data-stu-id="adb6f-132">a simple quantity object,</span></span>
- <span data-ttu-id="adb6f-133">제한 된 수량 개체 또는</span><span class="sxs-lookup"><span data-stu-id="adb6f-133">a bounded quantity object, or</span></span>
- <span data-ttu-id="adb6f-134">스파스 배열 수량 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-134">a sparse array quantity object.</span></span>


### <a name="examples"></a><span data-ttu-id="adb6f-135">예제</span><span class="sxs-lookup"><span data-stu-id="adb6f-135">Examples</span></span> ###

<span data-ttu-id="adb6f-136">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-136">This section is informative.</span></span>

<span data-ttu-id="adb6f-137">$1.9844146837 \Mathrm{Ha} $를 나타내는 단순 수량 \, :</span><span class="sxs-lookup"><span data-stu-id="adb6f-137">A simple quantity representing $1.9844146837\,\mathrm{Ha}$:</span></span>

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

<span data-ttu-id="adb6f-138">간격 $ [-7,-6] \Mathrm{Ha} $에 대 한 균일 한 분포를 나타내는 제한 된 수량입니다 \, .</span><span class="sxs-lookup"><span data-stu-id="adb6f-138">A bounded quantity representing a uniform distribution over the interval $[-7, -6]\,\mathrm{Ha}$:</span></span>

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

<span data-ttu-id="adb6f-139">다음은 요소가이 고 요소가와 같은 스파스 배열 수량입니다 `[1, 2]` `hello` `[3, 4]` `world` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-139">The following is a sparse array quantity with an element `[1, 2]` equal to `hello` and an element `[3, 4]` equal to `world`:</span></span>

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a><span data-ttu-id="adb6f-140">서식 섹션</span><span class="sxs-lookup"><span data-stu-id="adb6f-140">Format Section</span></span> ##

<span data-ttu-id="adb6f-141">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-141">This section is normative.</span></span>

<span data-ttu-id="adb6f-142">Broombridge 개체에는 라는 속성을 `format` 가진 JSON 개체인 속성이 있어야 합니다 `version` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-142">The Broombridge object MUST have a property `format` whose value is a JSON object with one property called `version`.</span></span>
<span data-ttu-id="adb6f-143">속성에는 `version` 값이 있어야 합니다 `"0.1"` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-143">The `version` property MUST have the value `"0.1"`.</span></span>

### <a name="example"></a><span data-ttu-id="adb6f-144">예</span><span class="sxs-lookup"><span data-stu-id="adb6f-144">Example</span></span> ###

<span data-ttu-id="adb6f-145">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-145">This section is informative.</span></span>

```yaml
format:                        # required
    version: "0.1"             # must match exactly
```

## <a name="integral-sets-section"></a><span data-ttu-id="adb6f-146">정수 집합 섹션</span><span class="sxs-lookup"><span data-stu-id="adb6f-146">Integral Sets Section</span></span> ##

<span data-ttu-id="adb6f-147">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-147">This section is normative.</span></span>

<span data-ttu-id="adb6f-148">Broombridge 개체에는 해당 `integral_sets` 값이 JSON 배열인 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-148">The Broombridge object MUST have a property `integral_sets` whose value is a JSON array.</span></span>
<span data-ttu-id="adb6f-149">속성 값의 각 항목은 `integral_sets` 이 섹션의 나머지 부분에 설명 된 대로 하나의 정수 집합을 설명 하는 JSON 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-149">Each item in the value of the `integral_sets` property MUST be a JSON object describing one set of integrals, as described in the remainder of this section.</span></span>
<span data-ttu-id="adb6f-150">이 섹션의 나머지 부분에서 "정수 집합 개체" 라는 용어는 `integral_sets` Broombridge 개체의 속성 값에 있는 항목을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-150">In the remainder of this section, the term "integral set object" will refer to an item in the value of the `integral_sets` property of the Broombridge object.</span></span>

<span data-ttu-id="adb6f-151">각 정수 계열 집합 개체에는 `metadata` 값이 JSON 개체 인 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-151">Each integral set object MUST have a property `metadata` whose value is a JSON object.</span></span>
<span data-ttu-id="adb6f-152">값은 `metadata` 빈 JSON 개체 (즉, `{}` ) 이거나 구현자에서 정의한 추가 속성을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-152">The value of `metadata` MAY be the empty JSON object (that is, `{}`), or MAY contain additional properties defined by the implementor.</span></span>

### <a name="hamiltonian-section"></a><span data-ttu-id="adb6f-153">Hamiltonian 섹션</span><span class="sxs-lookup"><span data-stu-id="adb6f-153">Hamiltonian Section</span></span> ###

#### <a name="overview"></a><span data-ttu-id="adb6f-154">개요</span><span class="sxs-lookup"><span data-stu-id="adb6f-154">Overview</span></span> ####

<span data-ttu-id="adb6f-155">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-155">This section is informative.</span></span>

<span data-ttu-id="adb6f-156">`hamiltonian`각 정수 계열 집합 개체의 속성은 특정 퀀텀 화학 문제에 대 한 Hamiltonian에 대 한 설명으로, 한 개 및 두 개의 본문 용어를 실수의 스파스 배열로 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-156">The `hamiltonian` property of each integral set object describes the Hamiltonian for a particular quantum chemistry problem by listing out its one- and two-body terms as sparse arrays of real numbers.</span></span>
<span data-ttu-id="adb6f-157">각 정수 계열 집합 개체에 설명 된 Hamiltonian 연산자는 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-157">The Hamiltonian operators described by each integral set object take the form</span></span>

<span data-ttu-id="adb6f-158">$ $ H = \sum \_ \{ i, j \} \sum \_ {\sigma\in \\ {\uparrow, \down화살표 \\ }} H \_ \{ ij \} a ^ \{ \aate{ \} \_ i, \sigma} a \_ {j, \sigma} + \frac {1} {2} \sum \_ \{ i, j, k, _l \} \sum \_ {\sum, \rho\in \\ {\uparrow, \downum} \\ } H \_ {ijkl} a ^ \sum \_ {i, \rho} a ^ \sum \_ {k, \sigma} a \_ {l, a \_ {j,, $ $</span><span class="sxs-lookup"><span data-stu-id="adb6f-158">$$ H = \sum\_\{i,j\}\sum\_{\sigma\in\\{\uparrow,\downarrow\\}} h\_\{ij\} a^\{\dagger\}\_{i,\sigma} a\_{j,\sigma} + \frac{1}{2}\sum\_\{i,j,k,l\}\sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}} h\_{ijkl} a^\dagger\_{i,\sigma} a^\dagger\_{k,\rho} a\_{l,\rho} a\_{j,\sigma}, $$</span></span>

<span data-ttu-id="adb6f-159">여기에서 _ {ijkl} = (ij | kl) $ in Mulliken 규칙을 $h 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-159">here $h_{ijkl}= (ij|kl)$ in Mulliken convention.</span></span>

<span data-ttu-id="adb6f-160">명확 하 게 하기 위해 1-전자 용어는</span><span class="sxs-lookup"><span data-stu-id="adb6f-160">For clarity, the one-electron term is</span></span>

<span data-ttu-id="adb6f-161">$ $ h_ {ij} = \int {\mathrm d} x \int ^ \* \_ i (x) \int (\frac {1} {2} \nabla ^ 2 + \_ \Int {A} \_ a} {| x-x \_ A |})  \right) \right \_ j (x), $ $</span><span class="sxs-lookup"><span data-stu-id="adb6f-161">$$ h_{ij} = \int {\mathrm d}x \psi^\*\_i(x) \left(\frac{1}{2}\nabla^2 + \sum\_{A}\frac{Z\_A}{|x-x\_A|}  \right) \psi\_j(x), $$</span></span>

<span data-ttu-id="adb6f-162">그리고 두 전자 단어는</span><span class="sxs-lookup"><span data-stu-id="adb6f-162">and the two-electron term is</span></span>

<span data-ttu-id="adb6f-163">$ $ h \_ \{ ijkl \} = \iint \{ \mathrm d \} x ^ 2 \psi ^ \{ \* \} \_ i (x \_ 1) \psi \_ j (x \_ 1) \iint \{ 1 \} \{ \| x \_ 1-x \_ 2 \| \} \psi \_ k \{ \* \} (x \_ 2) \psi \_ l (x \_ 2).</span><span class="sxs-lookup"><span data-stu-id="adb6f-163">$$ h\_\{ijkl\} = \iint \{\mathrm d\}x^2 \psi^\{\*\}\_i(x\_1)\psi\_j(x\_1) \frac\{1\}\{\|x\_1 -x\_2\|\}\psi\_k^\{\*\}(x\_2) \psi\_l(x\_2).</span></span>
$$

<span data-ttu-id="adb6f-164">속성의 각 요소에 대 한 [ `basis_set` 속성](#basis-set-object) 설명에서 언급 했 듯이 `integral_sets` , 사용 되는 기본 함수는 실제 값 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-164">As noted in our description of the [`basis_set` property](#basis-set-object) of each element of the `integral_sets` property, we further explicitly assume that the basis functions used are real-valued.</span></span>
<span data-ttu-id="adb6f-165">이를 통해 용어 사이에 다음 symmetries를 사용 하 여 Hamiltonian 표현을 압축할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-165">This allows us to use the following symmetries between the terms to compress the representation of the Hamiltonian.</span></span>

<span data-ttu-id="adb6f-166">$ $ h_ {ijkl} = h_ {ijlk} = h_ {jikl} = h_ {jilk} = h_ {klij} = h_ {klji} = h_ {lkij} = h_ {lkji}.</span><span class="sxs-lookup"><span data-stu-id="adb6f-166">$$ h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkij}=h_{lkji}.</span></span>
$$


#### <a name="contents"></a><span data-ttu-id="adb6f-167">콘텐츠</span><span class="sxs-lookup"><span data-stu-id="adb6f-167">Contents</span></span> ####

<span data-ttu-id="adb6f-168">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-168">This section is normative.</span></span>

<span data-ttu-id="adb6f-169">각 정수 계열 집합에는 `hamiltonian` 값이 JSON 개체 인 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-169">Each integral set MUST have a property `hamiltonian` whose value is a JSON object.</span></span>
<span data-ttu-id="adb6f-170">속성의 값은 `hamiltonian` Hamiltonian 개체 라고 하며, `one_electron_integrals` `two_electron_integrals` 이 섹션의 나머지 부분에 설명 된 대로 및 속성을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-170">The value of the `hamiltonian` property is known as a Hamiltonian object, and MUST have the properties `one_electron_integrals` and `two_electron_integrals` as described in the remainder of this section.</span></span>
<span data-ttu-id="adb6f-171">Hamiltonian 개체에도 속성이 있을 수 있습니다 `particle_hole_representation` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-171">A Hamiltonian object MAY also have a property `particle_hole_representation`.</span></span>
<span data-ttu-id="adb6f-172">값이 있는 경우 `particle_hole_representation` 이 섹션의 나머지 부분에 설명 된 형식을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-172">If present, the value of `particle_hole_representation` MUST follow the format described in the remainder of this section.</span></span>

##### <a name="one-electron-integrals-object"></a><span data-ttu-id="adb6f-173">One-Electron 적분 개체</span><span class="sxs-lookup"><span data-stu-id="adb6f-173">One-Electron Integrals Object</span></span> #####

<span data-ttu-id="adb6f-174">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-174">This section is normative.</span></span>

<span data-ttu-id="adb6f-175">`one_electron_integrals`Hamiltonian 개체의 속성은 인덱스가 두 정수이 고 해당 값이 숫자인 스파스 배열 수량 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-175">The `one_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity whose indices are two integers and whose values are numbers.</span></span>
<span data-ttu-id="adb6f-176">모든 용어에는 인덱스를 포함 해야 합니다 `[i, j]` `i >= j` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-176">Every term MUST have indices `[i, j]` where `i >= j`.</span></span>

> <span data-ttu-id="adb6f-177">두고 이는 Hamiltonian가 Hermitian의 결과로 _ {ij} = h_ {ji} $ $h 하는 대칭을 반영 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-177">[NOTE] This reflects the symmetry that $h_{ij} = h_{ji}$ which is a consequence of the fact that the Hamiltonian is Hermitian.</span></span>


###### <a name="example"></a><span data-ttu-id="adb6f-178">예</span><span class="sxs-lookup"><span data-stu-id="adb6f-178">Example</span></span> ######

<span data-ttu-id="adb6f-179">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-179">This section is informative.</span></span>

<span data-ttu-id="adb6f-180">다음 스파스 배열 수량은 Hamiltonian $ $ H = \left (-5.0 (a ^ \{ \aa{ \} \_ 1, \uparrow} a \_ {1, \uparrow} + a ^ \{ \aa{1)를 나타냅니다. \} \_ \downarrow} a \_ {1, \downarrow}) + 0.17 (a ^ \{ \left \} \_ {2, \uparrow} a \_ {1, \uparrow} + a ^ \{ \left { \} \_ 1, \uparrow} a { \_ 2, \downarrow} + a ^ \{ \} \_ \left {2, \downarrow} a { \_ 1, \downarrow} + a ^ \{ \} \_ \left {1, a \_ {2,) \left) \\ ,</span><span class="sxs-lookup"><span data-stu-id="adb6f-180">The following sparse array quantity represents the Hamiltonian $$ H = \left(-5.0  (a^\{\dagger\}\_{1,\uparrow} a\_{1,\uparrow}+a^\{\dagger\}\_{1,\downarrow} a\_{1,\downarrow})+ 0.17 (a^\{\dagger\}\_{2,\uparrow} a\_{1,\uparrow}+ a^\{\dagger\}\_{1,\uparrow} a\_{2,\uparrow}+a^\{\dagger\}\_{2,\downarrow} a\_{1,\downarrow}+ a^\{\dagger\}\_{1,\downarrow} a\_{2,\downarrow})\right)\\,\mathrm{Ha}.</span></span>
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
> <span data-ttu-id="adb6f-181">Broombridge는 1부터 기반으로 하는 인덱싱을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-181">Broombridge uses 1-based indexing.</span></span>


##### <a name="two-electron-integrals-object"></a><span data-ttu-id="adb6f-182">Two-Electron 적분 개체</span><span class="sxs-lookup"><span data-stu-id="adb6f-182">Two-Electron Integrals Object</span></span> #####

<span data-ttu-id="adb6f-183">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-183">This section is normative.</span></span>

<span data-ttu-id="adb6f-184">`two_electron_integrals`Hamiltonian 개체의 속성은 라는 추가 속성을 포함 한 스파스 배열 수량 이어야 합니다 `index_convention` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-184">The `two_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity with one additional property called `index_convention`.</span></span>
<span data-ttu-id="adb6f-185">값의 각 요소에는 `two_electron_integrals` 네 개의 인덱스가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-185">Each element of the value of `two_electron_integrals` MUST have four indices.</span></span>

<span data-ttu-id="adb6f-186">각 `two_electron_integrals` 속성에는 속성이 있어야 합니다 `index_convention` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-186">Each `two_electron_integrals` property MUST have a `index_convention` property.</span></span>
<span data-ttu-id="adb6f-187">속성의 값은 `index_convention` 표 1에 나열 된 허용 되는 값 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-187">The value of the `index_convention` property MUST be one of the allowed values listed in Table 1.</span></span>
<span data-ttu-id="adb6f-188">의 값 `index_convention` 이 인 경우 `mulliken` 스파스 배열 수량의 각 요소에 대해 `two_electron_integrals` Broombridge 문서를 로드 하는 파서는 Hamiltonian 항을 두 개의 전자 $h 연산자 (_ {i, j)와 동일 하 게 인스턴스화해야 합니다. k, l} a ^ \ dagger_i a ^ \ dagger_j a_k a_l $. 여기서 $i $, $j $, $k $ 및 $l $는 포괄 범위에서 정수 집합 개체의 속성에 지정 된 파괴의 정수 여야 `n_electrons` 하며, 여기서 $h _ {i, j, k, l} $은 `[i, j, k, l, h(i, j, k, l)]` 스파스 배열 수량의 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-188">If the value of `index_convention` is `mulliken`, then for each element of the `two_electron_integrals` sparse array quantity, a parser loading a Broombridge document MUST instantiate a Hamiltonian term equal to the two-electron operator $h_{i, j, k, l} a^\dagger_i a^\dagger_j a_k a_l$, where $i$, $j$, $k$, and $l$ MUST be integers in the inclusive range from 1 to the number of electrons specified by the `n_electrons` property of the integral set object, and where $h_{i, j, k, l}$ is the element `[i, j, k, l, h(i, j, k, l)]` of the sparse array quantity.</span></span>

###### <a name="symmetries"></a><span data-ttu-id="adb6f-189">Symmetries</span><span class="sxs-lookup"><span data-stu-id="adb6f-189">Symmetries</span></span> ######

<span data-ttu-id="adb6f-190">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-190">This section is normative.</span></span>

<span data-ttu-id="adb6f-191">`index_convention`개체의 속성이와 `two_electron_integrals` 같으면 인덱스를 사용 하는 `mulliken` 요소가 있는 경우와 같지 않으면 `[i, j, k, l]` 다음 인덱스가 표시 되지 않아야 합니다 `[i, j, k, l]` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-191">If the `index_convention` property of a `two_electron_integrals` object is equal to `mulliken`, then if an element with indices `[i, j, k, l]` is present, the following indices MUST NOT be present unless they are equal to `[i, j, k, l]`:</span></span>

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> <span data-ttu-id="adb6f-192">`index_convention`속성이 스파스 수량 개체 이기 때문에 다른 요소에 대해 인덱스가 반복 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-192">Because the `index_convention` property is a sparse quantity object, no indices may be repeated on different elements.</span></span>
> <span data-ttu-id="adb6f-193">특히 인덱스가 있는 요소가 있으면 `[i, j, k, l]` 해당 인덱스를 가질 수 있는 다른 요소가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-193">In particular, if an element with indices `[i, j, k, l]` is present, no other element may have those indices.</span></span>


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a><span data-ttu-id="adb6f-194">예</span><span class="sxs-lookup"><span data-stu-id="adb6f-194">Example</span></span> #######

<span data-ttu-id="adb6f-195">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-195">This section is informative.</span></span>

<span data-ttu-id="adb6f-196">다음 개체는 Hamiltonian를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-196">The following object specifies the Hamiltonian</span></span>

<span data-ttu-id="adb6f-197">$ $ H = \frac12 | sum \_ {\sum, \rho\in \\ {\uparrow, \downage} \\ } \sum gr (1.6 a ^ {\dagger} \_ {1, \dagger} a ^ {\rho} \_ {1, a \_ {1, \rho} a \_ {1, \sigma}-0.1 a ^ {\dagger} \_ {6, \sigma} a ^ {\dagger} {1, \rho} a { \_ \_ 3, \rho} a \_ {2, \sigma}-0.1 a ^ {\dagger} \_ {6, \sigma} a ^ {\dagger} \_ {1, \rho} a \_ {2, \rho} a \_ {3, \sigma}-0.1 a ^ {\dagger} \_ {1, \sigma} a ^ {\dagger} \_ {6, \rho} a { \_ 3, \rho} a \_ {2, \sigma}-0.1 a ^ {\dagger} \_ {1, \sigma} a ^ {\dagger} \_ {6, \rho} a \_ {2, \rho} a \_ {3, \sigma} $ $ $ $-0.1 a ^ {\dagger} \_ {3, \sigma} a ^ {\dagger} \_ {2, \rho} a \_ {6, \rho} a \_ {1, \sigma}-0.1 a ^ {\dagger} \_ {3, \sigma} a ^ {\dagger} \_ {2, \rho} a \_ {1, \rho} a \_ {6, \sigma}-0.1 a ^ {\dagger} \_ {2, \sigma} a ^ {\dagger} \_ {3 , \rho} a \_ {6, \rho} a \_ {1, \sigma}-0.1 a ^ {\dagger} \_ {2, \sigma} a ^ {\dagger} \_ {3, \rho} a \_ {1, \Rho} a \_ {6, \sigma}\Biggr) \\ , \textrm{Ha}.</span><span class="sxs-lookup"><span data-stu-id="adb6f-197">$$ H = \frac12 \sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}}\Biggr( 1.6 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{1,\rho} a\_{1,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{2,\rho} a\_{3,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{2,\rho} a\_{3,\sigma} $$ $$- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{1,\rho} a\_{6,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{1,\rho} a\_{6,\sigma}\Biggr)\\,\textrm{Ha}.</span></span>
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

##### <a name="particlehole-representation-object"></a><span data-ttu-id="adb6f-198">파티클-구멍 표현 개체</span><span class="sxs-lookup"><span data-stu-id="adb6f-198">Particle–Hole Representation Object</span></span> #####

<span data-ttu-id="adb6f-199">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-199">This section is normative.</span></span>

<span data-ttu-id="adb6f-200">파티클-구멍 표현 개체는 생성 및 annihilation 연산자가 Hartree – Fock 상태와 같은 사용 된 참조 상태에서 excitations를 설명 하는 파티클 구멍 표현과 관련 하 여 저장 된 정수를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-200">The particle–hole representation object specifies that the integrals stored are defined with respect to particle hole representation wherein the creation and annihilation operators describe excitations away from the reference state used, such as a Hartree–Fock state.</span></span>
<span data-ttu-id="adb6f-201">개체는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-201">The object is OPTIONAL.</span></span>
<span data-ttu-id="adb6f-202">개체를 지정 하지 않으면 Hamiltonian는 파티클 구멍 표현에 지정 되지 않은 것으로 해석 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-202">If the object is not specified then the Hamiltonian is to be interpreted as not given in particle-hole representation.</span></span>
<span data-ttu-id="adb6f-203">있는 경우 값은 `particle_hole_representation` 인덱스가 4 개의 정수이 고 값이 숫자 및 문자열인 스파스 배열 수량 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-203">If present, the value of `particle_hole_representation` MUST be a sparse array quantity object whose indices are four integers, and whose values are a number and a string.</span></span>
<span data-ttu-id="adb6f-204">각 요소 값의 문자열 부분에는 문자만 포함 해야 `'+'` 하며, `'-'` 용어의 지정 된 인수가 파티클-구멍 표현의 생성 또는 annihilation 연산자 인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-204">The string portion of the value of each element MUST contain only the characters `'+'` and `'-'` which specifies whether a given factor in the term is a creation or annihilation operator in the particle–hole representation.</span></span>  <span data-ttu-id="adb6f-205">예를 들어 `"-+++"` 사이트 $i $에서 생성 되는 구멍과 해당 사이트 $j, k $ 및 $l $에서 생성 되는 파티클에 대 한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-205">For example `"-+++"` coresponds to a hole being created at site $i$ and particles being created at sites $j,k$ and $l$.</span></span>

> [!NOTE]
> <span data-ttu-id="adb6f-206">의 값 `particle_hole_representation` 이 스파스 배열 수량 개체 이므로 `unit` 및 `format` 속성을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-206">As the value of the `particle_hole_representation` is a sparse array quantity object, the `unit` and `format` properties must be specified.</span></span>
> <span data-ttu-id="adb6f-207">허용 되는 단위는 표 1에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-207">Acceptable units include are listed in Table 1.</span></span>
> <span data-ttu-id="adb6f-208">`format`속성은 필수 이며 Hamiltonian 계수가 조밀한 또는 스파스 배열로 지정 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-208">The `format` property is required, and indicates whether the Hamiltonian coefficients are specified as a dense or sparse array.</span></span>
> <span data-ttu-id="adb6f-209">현재 버전에서는 지정 되지 않은 모든 요소를 $0 $로 해석 하 여 스파스 배열만 지원 되지만 이후 버전에서는 속성의 추가 값에 대 한 지원을 추가할 수 있습니다 `format` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-209">In the current version, only sparse arrays are supported, with interpretation that all unspecified elements are $0$, but future versions may add support for additional values of the `format` property.</span></span>

### <a name="initial-state-section"></a><span data-ttu-id="adb6f-210">초기 상태 섹션</span><span class="sxs-lookup"><span data-stu-id="adb6f-210">Initial State Section</span></span> ###

<span data-ttu-id="adb6f-211">Initial_state_suggestion 개체는 지정 된 Hamiltonian에 대 한 관심의 초기 퀀텀 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-211">The initial_state_suggestion object specifies initial quantum states of interest to the specified Hamiltonian.</span></span> <span data-ttu-id="adb6f-212">이 개체는 JSON 개체의 배열 이어야 합니다 `state` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-212">This object must be an array of JSON `state` objects.</span></span>

#### <a name="state-object"></a><span data-ttu-id="adb6f-213">상태 개체</span><span class="sxs-lookup"><span data-stu-id="adb6f-213">State object</span></span> ####

<span data-ttu-id="adb6f-214">각 상태는 차지한 superposition을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-214">Each states represents a superposition of occupied orbitals.</span></span> <span data-ttu-id="adb6f-215">각 상태 개체에는 `label` 문자열을 포함 하는 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-215">Each state object MUST have a `label` property containing a string.</span></span> <span data-ttu-id="adb6f-216">각 상태 개체에는 `superposition` 기준 상태의 배열과 정규화 되지 않은 amplitudes을 포함 하는 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-216">Each state object MUST have a `superposition` property containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="adb6f-217">예를 들어 초기 상태 $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) \ket $ $ $ {0} $ \ket{E} = \frac{0.1 (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) + 0.2 (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {3, \uparrow}a ^ {\dagger} \_ {2, \downarrow})} {\sqrt{| 0.1 | ^ 2 + | 0.2 | ^ 2}} \ket {0} $ $는 다음으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-217">For example, the initial states $$ \ket{G0}=\ket{G1}=\ket{G2}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0} $$ $$ \ket{E}=\frac{0.1 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})+0.2 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\uparrow}a^{\dagger}\_{2,\downarrow})}{\sqrt{|0.1|^2+|0.2|^2}}\ket{0} $$ are represented by</span></span>
```yaml
initial_state_suggestions: # optional. If not provided, spin-orbitals will be filled to minimize one-body diagonal term energies.
    - state:
        label: "|G0>"
        superposition:
            - [1.0, "(1a)+","(2a)+","(2b)+","|vacuum>"]
    - state:
        label: "|G1>"
        superposition:
            - [-1.0, "(2a)+","(1a)+","(2b)+","|vacuum>"]
    - state:
        label: "|G2>"
        superposition:
            - [1.0, "(3a)","(1a)+","(2a)+","(3a)+","(2b)+","|vacuum>"]
    - state:
        label: "|E>"
        superposition:
            - [0.1, "(1a)+","(2a)+","(2b)+","|vacuum>"]
            - [0.2, "(1a)+","(3a)+","(2b)+","|vacuum>"]
```

#### <a name="basis-set-object"></a><span data-ttu-id="adb6f-218">기본 설정 개체</span><span class="sxs-lookup"><span data-stu-id="adb6f-218">Basis Set Object</span></span> ####

<span data-ttu-id="adb6f-219">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-219">This section is normative.</span></span>

<span data-ttu-id="adb6f-220">각 정수 계열 집합 개체에는 속성이 있을 수 있습니다 `basis_set` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-220">Each integral set object MAY have a `basis_set` property.</span></span>
<span data-ttu-id="adb6f-221">속성의 값이 있는 경우 속성의 값은 `basis_set` 및 라는 두 개의 속성이 있는 개체 여야 합니다 `type` `name` .</span><span class="sxs-lookup"><span data-stu-id="adb6f-221">If present, the value of the `basis_set` property MUST be an object with two properties, `type` and `name`.</span></span>

<span data-ttu-id="adb6f-222">속성 값으로 식별 되는 기본 함수는 `basis_set` 실제 값 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-222">The basis functions identified by the value of the `basis_set` property MUST be real-valued.</span></span>

> [!NOTE]
> <span data-ttu-id="adb6f-223">이 사양의 이후 버전에서는 모든 기본 함수가 실제 값 이라고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-223">The assumption that all basis functions are real-valued may be relaxed in future versions of this specification.</span></span>

## <a name="tables-and-lists"></a><span data-ttu-id="adb6f-224">테이블 및 목록</span><span class="sxs-lookup"><span data-stu-id="adb6f-224">Tables and Lists</span></span> ##

### <a name="table-1-allowed-physical-units"></a><span data-ttu-id="adb6f-225">표 1.</span><span class="sxs-lookup"><span data-stu-id="adb6f-225">Table 1.</span></span> <span data-ttu-id="adb6f-226">허용 된 물리적 단위</span><span class="sxs-lookup"><span data-stu-id="adb6f-226">Allowed Physical Units</span></span> ###

<span data-ttu-id="adb6f-227">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-227">This section is normative.</span></span>

<span data-ttu-id="adb6f-228">단위를 지정 하는 문자열은 다음 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-228">Any string specifying a unit MUST be one of the following:</span></span>

- `hartree`
- `ev`

<span data-ttu-id="adb6f-229">파서 및 생산자는 다음과 같은 단순 수량 개체를 동일 하 게 처리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-229">Parsers and producers MUST treat the following simple quantity objects as equivalent:</span></span>

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a><span data-ttu-id="adb6f-230">표 2.</span><span class="sxs-lookup"><span data-stu-id="adb6f-230">Table 2.</span></span> <span data-ttu-id="adb6f-231">허용 되는 인덱스 규칙</span><span class="sxs-lookup"><span data-stu-id="adb6f-231">Allowed Index Conventions</span></span> ###

<span data-ttu-id="adb6f-232">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-232">This section is normative.</span></span>

<span data-ttu-id="adb6f-233">인덱스 규칙을 지정 하는 문자열은 다음 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-233">Any string specifying an index convention MUST be one of the following:</span></span>

- `mulliken`

<span data-ttu-id="adb6f-234">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-234">This section is informative.</span></span>

<span data-ttu-id="adb6f-235">이 사양의 이후 버전에는 추가 인덱스 규칙이 도입 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-235">Additional index conventions may be introduced in future versions of this specification.</span></span>

#### <a name="interpretation-of-index-conventions"></a><span data-ttu-id="adb6f-236">인덱스 규칙의 해석</span><span class="sxs-lookup"><span data-stu-id="adb6f-236">Interpretation of Index Conventions</span></span> ####

<span data-ttu-id="adb6f-237">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb6f-237">This section is informative.</span></span>
