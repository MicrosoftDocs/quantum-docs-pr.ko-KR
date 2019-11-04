---
title: Broombridge 스키마 사양
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_1
ms.openlocfilehash: a950e04d44e5de8091b034214258d2c2fa663f58
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185361"
---
# <a name="broombridge-specification-v01"></a><span data-ttu-id="8279e-102">Broombridge 사양 v 0.1</span><span class="sxs-lookup"><span data-stu-id="8279e-102">Broombridge Specification v0.1</span></span> #

<span data-ttu-id="8279e-103">이 문서에서 "REQUIRED", "NOT", "REQUIRED", "be", "not", "REQUIRED", "be", "REQUIRED", "be" 및 "OPTIONAL"은 [RFC 2119](https://tools.ietf.org/html/rfc2119)에 설명 된 대로 해석 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-103">The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span></span>

<span data-ttu-id="8279e-104">"참고", "정보" 또는 "경고"와 같은 제목이 있는 모든 사이드바는 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-104">Any sidebar with the headings "NOTE," "INFORMATION," or "WARNING" is informative.</span></span>

## <a name="introduction"></a><span data-ttu-id="8279e-105">소개</span><span class="sxs-lookup"><span data-stu-id="8279e-105">Introduction</span></span> ##

<span data-ttu-id="8279e-106">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-106">This section is informative.</span></span>

<span data-ttu-id="8279e-107">Broombridge 문서는 퀀텀 시뮬레이션 및 프로그래밍 도구 체인을 사용 하 여 처리 하기 위해 퀀텀 화학의 시뮬레이션 문제를 전달 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-107">Broombridge documents are intended to communicate instances of simulation problems in quantum chemistry for processing using quantum simulation and programming toolchains.</span></span>

## <a name="serialization"></a><span data-ttu-id="8279e-108">직렬화</span><span class="sxs-lookup"><span data-stu-id="8279e-108">Serialization</span></span> ##

<span data-ttu-id="8279e-109">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-109">This section is normative.</span></span>

<span data-ttu-id="8279e-110">Broombridge 문서는 [RFC 4627](https://tools.ietf.org/html/rfc4627) 섹션 2.2에 설명 된 대로 JSON 개체를 나타내는 [yaml 1.2 문서로](http://yaml.org/spec/) serialize 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-110">A Broombridge document MUST be serialized as a [YAML 1.2 document](http://yaml.org/spec/) representing a JSON object as described in [RFC 4627](https://tools.ietf.org/html/rfc4627) section 2.2.</span></span>
<span data-ttu-id="8279e-111">YAML로 serialize 된 개체에는 값이 `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"`되 고 JSON 스키마 초안-06 사양 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)]에 따라 유효 해야 하는 속성 `"$schema"` 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-111">The object serialized to YAML MUST have a property `"$schema"` whose value is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"`, and MUST be valid according to the JSON Schema draft-06 specifications [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span></span>

<span data-ttu-id="8279e-112">이 사양의 나머지 부분에서는 "Broombridge 개체"가 Broombridge YAML 문서에서 deserialize 된 JSON 개체를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-112">For the remainder of this specification, "the Broombridge object" will refer to the JSON object deserialized from a Broombridge YAML document.</span></span>

<span data-ttu-id="8279e-113">별도로 명시 하지 않는 한 개체에는이 문서에서 명시적으로 지정 된 속성 이외의 추가 속성을 포함 해서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-113">Unless otherwise explicitly noted, objects MUST NOT have additional properties beyond those specified explicitly in this document.</span></span>

## <a name="additional-definitions"></a><span data-ttu-id="8279e-114">추가 정의</span><span class="sxs-lookup"><span data-stu-id="8279e-114">Additional Definitions</span></span> ##

<span data-ttu-id="8279e-115">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-115">This section is normative.</span></span>

### <a name="quantity-objects"></a><span data-ttu-id="8279e-116">Quantity 개체</span><span class="sxs-lookup"><span data-stu-id="8279e-116">Quantity Objects</span></span> ###

<span data-ttu-id="8279e-117">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-117">This section is normative.</span></span>

<span data-ttu-id="8279e-118">_Quantity 개체_ 는 JSON 개체이 고 해당 값이 표 1에 나열 된 허용 되는 값 중 하나인 속성 `units` 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-118">A _quantity object_ is a JSON object, and MUST have a property `units` whose value is one of the allowed values listed in Table 1.</span></span>

<span data-ttu-id="8279e-119">Quantity 개체는 `units` 속성 외에도 `value` 단일 속성을 포함 하는 _단순 수량 개체_ 입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-119">A quantity object is a _simple quantity object_ if it has a single property `value` in addition to its `units` property.</span></span>
<span data-ttu-id="8279e-120">`value` 속성의 값은 숫자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-120">The value of the `value` property MUST be a number.</span></span>

<span data-ttu-id="8279e-121">Quantity 개체는 `units` 속성 외에도 `lower` 및 `upper` 속성이 있는 경우 _제한 된 수량 개체_ 입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-121">A quantity object is a _bounded quantity object_ if it has the properties `lower` and `upper` in addition to its `units` property.</span></span>
<span data-ttu-id="8279e-122">`lower` 및 `upper` 속성의 값은 숫자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-122">The values of the `lower` and `upper` properties MUST be numbers.</span></span>
<span data-ttu-id="8279e-123">제한 된 수량 개체에는 값이 숫자 인 속성 `value` 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-123">A bounded quantity object MAY have a property `value` whose value is a number.</span></span>

<span data-ttu-id="8279e-124">Quantity 개체는 속성 `format` 있고 속성 `values` `units` 속성 외에도 있는 경우 _스파스 배열 수량 개체_ 입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-124">A quantity object is a _sparse array quantity object_ if it has the property `format` and a property `values` in addition to its `units` property.</span></span>
<span data-ttu-id="8279e-125">`format` 값은 `sparse`문자열 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-125">The value of `format` MUST be the string `sparse`.</span></span>
<span data-ttu-id="8279e-126">`values` 속성의 값은 배열 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-126">The value of the `values` property MUST be an array.</span></span>
<span data-ttu-id="8279e-127">`values`의 각 요소는 스파스 배열 수량의 인덱스 및 값을 나타내는 배열 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-127">Each element of `values` MUST be an array representing the indices and value of the sparse array quantity.</span></span>

<span data-ttu-id="8279e-128">스파스 배열 수량 개체의 각 요소에 대 한 인덱스는 전체 스파스 배열 수량 개체에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-128">The indices for each element of a sparse array quantity object MUST be unique across the entire sparse array quantity object.</span></span>
<span data-ttu-id="8279e-129">`0`값이 포함 된 인덱스가 있는 경우 파서는 스파스 배열 수량 개체를 해당 인덱스가 전혀 없는 스파스 배열 수량 개체와 동일 하 게 처리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-129">If an index is present with a value of `0`, a parser MUST treat the sparse array quantity object identically to a sparse array quantity object in which that index is not present at all.</span></span>


<span data-ttu-id="8279e-130">Quantity 개체는 다음 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-130">A quantity object MUST either be</span></span>

- <span data-ttu-id="8279e-131">단순 수량 개체</span><span class="sxs-lookup"><span data-stu-id="8279e-131">a simple quantity object,</span></span>
- <span data-ttu-id="8279e-132">제한 된 수량 개체 또는</span><span class="sxs-lookup"><span data-stu-id="8279e-132">a bounded quantity object, or</span></span>
- <span data-ttu-id="8279e-133">스파스 배열 수량 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-133">a sparse array quantity object.</span></span>


### <a name="examples"></a><span data-ttu-id="8279e-134">예시</span><span class="sxs-lookup"><span data-stu-id="8279e-134">Examples</span></span> ###

<span data-ttu-id="8279e-135">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-135">This section is informative.</span></span>

<span data-ttu-id="8279e-136">$1.9844146837\,\mathrm{Ha} $를 나타내는 단순 수량입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-136">A simple quantity representing $1.9844146837\,\mathrm{Ha}$:</span></span>

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

<span data-ttu-id="8279e-137">간격 $ [-7,-6]\,\mathrm{Ha} $에 대 한 균일 분포를 나타내는 제한 된 수량입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-137">A bounded quantity representing a uniform distribution over the interval $[-7, -6]\,\mathrm{Ha}$:</span></span>

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

<span data-ttu-id="8279e-138">다음은 요소가 `hello`와 동일 `[1, 2]` 스파스 배열 수량과 `world`와 같은 요소 `[3, 4]`입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-138">The following is a sparse array quantity with an element `[1, 2]` equal to `hello` and an element `[3, 4]` equal to `world`:</span></span>

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a><span data-ttu-id="8279e-139">서식 섹션</span><span class="sxs-lookup"><span data-stu-id="8279e-139">Format Section</span></span> ##

<span data-ttu-id="8279e-140">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-140">This section is normative.</span></span>

<span data-ttu-id="8279e-141">Broombridge 개체에는 값이 `version`라는 하나의 속성이 있는 JSON 개체인 속성 `format` 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-141">The Broombridge object MUST have a property `format` whose value is a JSON object with one property called `version`.</span></span>
<span data-ttu-id="8279e-142">`version` 속성에 `"0.1"`값이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-142">The `version` property MUST have the value `"0.1"`.</span></span>

### <a name="example"></a><span data-ttu-id="8279e-143">예제</span><span class="sxs-lookup"><span data-stu-id="8279e-143">Example</span></span> ###

<span data-ttu-id="8279e-144">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-144">This section is informative.</span></span>

```yaml
format:                        # required
    version: "0.1"             # must match exactly
```

## <a name="integral-sets-section"></a><span data-ttu-id="8279e-145">정수 집합 섹션</span><span class="sxs-lookup"><span data-stu-id="8279e-145">Integral Sets Section</span></span> ##

<span data-ttu-id="8279e-146">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-146">This section is normative.</span></span>

<span data-ttu-id="8279e-147">Broombridge 개체에는 값이 JSON 배열인 속성 `integral_sets` 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-147">The Broombridge object MUST have a property `integral_sets` whose value is a JSON array.</span></span>
<span data-ttu-id="8279e-148">`integral_sets` 속성 값의 각 항목은이 섹션의 나머지 부분에 설명 된 대로 하나의 정수 집합을 설명 하는 JSON 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-148">Each item in the value of the `integral_sets` property MUST be a JSON object describing one set of integrals, as described in the remainder of this section.</span></span>
<span data-ttu-id="8279e-149">이 섹션의 나머지 부분에서 "정수 집합 개체" 라는 용어는 Broombridge 개체의 `integral_sets` 속성 값에 있는 항목을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-149">In the remainder of this section, the term "integral set object" will refer to an item in the value of the `integral_sets` property of the Broombridge object.</span></span>

<span data-ttu-id="8279e-150">각 정수 계열 집합 개체에는 해당 값이 JSON 개체인 속성 `metadata` 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-150">Each integral set object MUST have a property `metadata` whose value is a JSON object.</span></span>
<span data-ttu-id="8279e-151">`metadata` 값은 빈 JSON 개체 (`{}`) 이거나 구현자에서 정의 된 추가 속성을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-151">The value of `metadata` MAY be the empty JSON object (that is, `{}`), or MAY contain additional properties defined by the implementor.</span></span>

### <a name="hamiltonian-section"></a><span data-ttu-id="8279e-152">Hamiltonian 섹션</span><span class="sxs-lookup"><span data-stu-id="8279e-152">Hamiltonian Section</span></span> ###

#### <a name="overview"></a><span data-ttu-id="8279e-153">개요</span><span class="sxs-lookup"><span data-stu-id="8279e-153">Overview</span></span> ####

<span data-ttu-id="8279e-154">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-154">This section is informative.</span></span>

<span data-ttu-id="8279e-155">각 정수 계열 집합 개체의 `hamiltonian` 속성은 특정 퀀텀 화학 문제에 대 한 Hamiltonian에 대 한 설명으로, 한 개 및 두 개의 본문 용어를 실수의 스파스 배열로 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-155">The `hamiltonian` property of each integral set object describes the Hamiltonian for a particular quantum chemistry problem by listing out its one- and two-body terms as sparse arrays of real numbers.</span></span>
<span data-ttu-id="8279e-156">각 정수 계열 집합 개체에 설명 된 Hamiltonian 연산자는 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-156">The Hamiltonian operators described by each integral set object take the form</span></span>

<span data-ttu-id="8279e-157">$ $ H = \sum\_\{i, j\}\sum\_{\sigma\in\\{\uparrow, \down화살표\\}} H\_\{ij\} a ^\{\aa\}\_{i , \sigma} a\_{j, \sigma} + \frac{1}{2}\sum\_\{i, j, k, l\}\sum\_{\시그마, \rho\in\\{\uparrow, \frac\\}} h\_{ijkl} a ^ \\_{i , \sigma} a ^ \dagger\_{k, \rho} a\_{l, \rho} a\_{j,, $ $</span><span class="sxs-lookup"><span data-stu-id="8279e-157">$$ H = \sum\_\{i,j\}\sum\_{\sigma\in\\{\uparrow,\downarrow\\}} h\_\{ij\} a^\{\dagger\}\_{i,\sigma} a\_{j,\sigma} + \frac{1}{2}\sum\_\{i,j,k,l\}\sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}} h\_{ijkl} a^\dagger\_{i,\sigma} a^\dagger\_{k,\rho} a\_{l,\rho} a\_{j,\sigma}, $$</span></span>

<span data-ttu-id="8279e-158">여기에서 _ {ijkl} = (ij | kl) $ in Mulliken 규칙을 $h 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-158">here $h_{ijkl}= (ij|kl)$ in Mulliken convention.</span></span>

<span data-ttu-id="8279e-159">명확 하 게 하기 위해 1-전자 용어는</span><span class="sxs-lookup"><span data-stu-id="8279e-159">For clarity, the one-electron term is</span></span>

<span data-ttu-id="8279e-160">$ $ h_ {ij} = \int {\mathrm d} x \int ^ \*\_i (x) \int (\frac{1}{2}\nabla ^ 2 + \int\_{A} \frac{Z\_A} {| x-x\_A |}  \right) \right\_j (x), $ $</span><span class="sxs-lookup"><span data-stu-id="8279e-160">$$ h_{ij} = \int {\mathrm d}x \psi^\*\_i(x) \left(\frac{1}{2}\nabla^2 + \sum\_{A}\frac{Z\_A}{|x-x\_A|}  \right) \psi\_j(x), $$</span></span>

<span data-ttu-id="8279e-161">그리고 두 전자 단어는</span><span class="sxs-lookup"><span data-stu-id="8279e-161">and the two-electron term is</span></span>

<span data-ttu-id="8279e-162">$ $ h\_\{ijkl\} = \iint \{\mathrm d\}x ^ 2 \psi ^\{\*\}\_\_i (x\_1) \psi\_j (x\{1) \iint 1\}\{\|x\_1-x\_2\|\}\psi\_k ^\{\*\}(x\_2) \psi\_l (x\_2).</span><span class="sxs-lookup"><span data-stu-id="8279e-162">$$ h\_\{ijkl\} = \iint \{\mathrm d\}x^2 \psi^\{\*\}\_i(x\_1)\psi\_j(x\_1) \frac\{1\}\{\|x\_1 -x\_2\|\}\psi\_k^\{\*\}(x\_2) \psi\_l(x\_2).</span></span>
$$

<span data-ttu-id="8279e-163">`integral_sets` 속성의 각 요소에 대 한 [`basis_set` 속성](#basis-set-object) 에 대 한 설명에 설명 된 대로, 사용 되는 기본 함수는 실제 값 이라고 명확 하 게 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-163">As noted in our description of the [`basis_set` property](#basis-set-object) of each element of the `integral_sets` property, we further explicitly assume that the basis functions used are real-valued.</span></span>
<span data-ttu-id="8279e-164">이를 통해 용어 사이에 다음 symmetries를 사용 하 여 Hamiltonian 표현을 압축할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-164">This allows us to use the following symmetries between the terms to compress the representation of the Hamiltonian.</span></span>

<span data-ttu-id="8279e-165">$ $ h_ {ijkl} = h_ {ijlk} = h_ {jikl} = h_ {jilk} = h_ {klij} = h_ {klji} = h_ {lkij} = h_ {lkji}.</span><span class="sxs-lookup"><span data-stu-id="8279e-165">$$ h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkij}=h_{lkji}.</span></span>
$$


#### <a name="contents"></a><span data-ttu-id="8279e-166">콘텐츠</span><span class="sxs-lookup"><span data-stu-id="8279e-166">Contents</span></span> ####

<span data-ttu-id="8279e-167">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-167">This section is normative.</span></span>

<span data-ttu-id="8279e-168">각 정수 계열 집합에는 해당 값이 JSON 개체인 속성 `hamiltonian` 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-168">Each integral set MUST have a property `hamiltonian` whose value is a JSON object.</span></span>
<span data-ttu-id="8279e-169">`hamiltonian` 속성의 값은 Hamiltonian 개체 라고 하며,이 섹션의 나머지 부분에 설명 된 대로 `one_electron_integrals` 및 `two_electron_integrals` 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-169">The value of the `hamiltonian` property is known as a Hamiltonian object, and MUST have the properties `one_electron_integrals` and `two_electron_integrals` as described in the remainder of this section.</span></span>
<span data-ttu-id="8279e-170">Hamiltonian 개체에도 `particle_hole_representation`속성이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-170">A Hamiltonian object MAY also have a property `particle_hole_representation`.</span></span>
<span data-ttu-id="8279e-171">`particle_hole_representation` 값은이 섹션의 나머지 부분에 설명 된 형식을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-171">If present, the value of `particle_hole_representation` MUST follow the format described in the remainder of this section.</span></span>

##### <a name="one-electron-integrals-object"></a><span data-ttu-id="8279e-172">1-전자 정수 개체</span><span class="sxs-lookup"><span data-stu-id="8279e-172">One-Electron Integrals Object</span></span> #####

<span data-ttu-id="8279e-173">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-173">This section is normative.</span></span>

<span data-ttu-id="8279e-174">Hamiltonian 개체의 `one_electron_integrals` 속성은 인덱스가 두 정수이 고 해당 값이 숫자인 스파스 배열 수량 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-174">The `one_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity whose indices are two integers and whose values are numbers.</span></span>
<span data-ttu-id="8279e-175">모든 용어에는 `i >= j``[i, j]` 인덱스가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-175">Every term MUST have indices `[i, j]` where `i >= j`.</span></span>

> <span data-ttu-id="8279e-176">두고 이는 Hamiltonian가 Hermitian 임을 나타내는 _ {ij} = h_ {ji} $ $h 하는 대칭을 반영 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-176">[NOTE] This reflects the symmetry that $h_{ij} = h_{ji}$ which is a consequence of the fact that the Hamiltonian is Hermitian.</span></span>


###### <a name="example"></a><span data-ttu-id="8279e-177">예제</span><span class="sxs-lookup"><span data-stu-id="8279e-177">Example</span></span> ######

<span data-ttu-id="8279e-178">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-178">This section is informative.</span></span>

<span data-ttu-id="8279e-179">다음 스파스 배열 수량은 Hamiltonian $ $ H = \left (-5.0 (a ^\{\left\}\_{1, \uparrow} a\_{1, \uparrow} + a ^\{\left\}\_{1, a\_{1입니다. , \downarrow}) + 0.17 (a ^\{\dagger\}\_{2, \uparrow} a\_{1, \uparrow} + a ^\{\dagger\}\_{1, \uparrow} a\_{2, + a ^\{\dagger\}\_{2 , \downarrow} a\_{1, \downarrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{2, \downarrow}) \dagger)\\,</span><span class="sxs-lookup"><span data-stu-id="8279e-179">The following sparse array quantity represents the Hamiltonian $$ H = \left(-5.0  (a^\{\dagger\}\_{1,\uparrow} a\_{1,\uparrow}+a^\{\dagger\}\_{1,\downarrow} a\_{1,\downarrow})+ 0.17 (a^\{\dagger\}\_{2,\uparrow} a\_{1,\uparrow}+ a^\{\dagger\}\_{1,\uparrow} a\_{2,\uparrow}+a^\{\dagger\}\_{2,\downarrow} a\_{1,\downarrow}+ a^\{\dagger\}\_{1,\downarrow} a\_{2,\downarrow})\right)\\,\mathrm{Ha}.</span></span>
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
> <span data-ttu-id="8279e-180">Broombridge는 1부터 기반으로 하는 인덱싱을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-180">Broombridge uses 1-based indexing.</span></span>


##### <a name="two-electron-integrals-object"></a><span data-ttu-id="8279e-181">2-전자 정수 개체</span><span class="sxs-lookup"><span data-stu-id="8279e-181">Two-Electron Integrals Object</span></span> #####

<span data-ttu-id="8279e-182">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-182">This section is normative.</span></span>

<span data-ttu-id="8279e-183">Hamiltonian 개체의 `two_electron_integrals` 속성은 `index_convention`라는 하나 이상의 추가 속성이 있는 스파스 배열 수량 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-183">The `two_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity with one additional property called `index_convention`.</span></span>
<span data-ttu-id="8279e-184">`two_electron_integrals` 값의 각 요소에는 네 개의 인덱스가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-184">Each element of the value of `two_electron_integrals` MUST have four indices.</span></span>

<span data-ttu-id="8279e-185">각 `two_electron_integrals` 속성에는 `index_convention` 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-185">Each `two_electron_integrals` property MUST have a `index_convention` property.</span></span>
<span data-ttu-id="8279e-186">`index_convention` 속성의 값은 표 1에 나열 된 허용 되는 값 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-186">The value of the `index_convention` property MUST be one of the allowed values listed in Table 1.</span></span>
<span data-ttu-id="8279e-187">`index_convention` 값이 `mulliken`되는 경우에는 `two_electron_integrals` 스파스 배열 수량의 각 요소에 대해 Broombridge 문서를 로드 하는 파서는 두 전자 $h 연산자 (_ {i, j, k, l} a ^ \dagger_i a ^ \dagger_j a_k a_l $)와 같은 Hamiltonian 항을 인스턴스화해야 합니다. , 여기서 $i $, $j $, $k $ 및 $l $은 포괄 범위의 정수 (정수 집합 개체의 `n_electrons` 속성으로 지정 된 파괴)의 정수 여야 하며, 여기서 $h _ {i, j, k, l} $는 스파스 배열 수량 `[i, j, k, l, h(i, j, k, l)]` 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-187">If the value of `index_convention` is `mulliken`, then for each element of the `two_electron_integrals` sparse array quantity, a parser loading a Broombridge document MUST instantiate a Hamiltonian term equal to the two-electron operator $h_{i, j, k, l} a^\dagger_i a^\dagger_j a_k a_l$, where $i$, $j$, $k$, and $l$ MUST be integers in the inclusive range from 1 to the number of electrons specified by the `n_electrons` property of the integral set object, and where $h_{i, j, k, l}$ is the element `[i, j, k, l, h(i, j, k, l)]` of the sparse array quantity.</span></span>

###### <a name="symmetries"></a><span data-ttu-id="8279e-188">Symmetries</span><span class="sxs-lookup"><span data-stu-id="8279e-188">Symmetries</span></span> ######

<span data-ttu-id="8279e-189">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-189">This section is normative.</span></span>

<span data-ttu-id="8279e-190">`two_electron_integrals` 개체의 `index_convention` 속성이 `mulliken`와 같으면 인덱스가 `[i, j, k, l]` 인 요소가 있는 경우 다음 인덱스는 `[i, j, k, l]`와 같지 않은 경우에는 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-190">If the `index_convention` property of a `two_electron_integrals` object is equal to `mulliken`, then if an element with indices `[i, j, k, l]` is present, the following indices MUST NOT be present unless they are equal to `[i, j, k, l]`:</span></span>

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> <span data-ttu-id="8279e-191">`index_convention` 속성이 스파스 수량 개체 이기 때문에 다른 요소에 대해 인덱스가 반복 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-191">Because the `index_convention` property is a sparse quantity object, no indices may be repeated on different elements.</span></span>
> <span data-ttu-id="8279e-192">특히 `[i, j, k, l]` 인덱스를 사용 하는 요소가 있는 경우 다른 요소는 해당 인덱스를 가질 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-192">In particular, if an element with indices `[i, j, k, l]` is present, no other element may have those indices.</span></span>


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a><span data-ttu-id="8279e-193">예제</span><span class="sxs-lookup"><span data-stu-id="8279e-193">Example</span></span> #######

<span data-ttu-id="8279e-194">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-194">This section is informative.</span></span>

<span data-ttu-id="8279e-195">다음 개체는 Hamiltonian를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-195">The following object specifies the Hamiltonian</span></span>

<span data-ttu-id="8279e-196">$ $ H = \frac12 \sum\_{\sum, \rho\in\\{\uparrow, \downix\\}} \sum \dagger} (1.6 a ^ {\dagger}\_{1, \rho} a ^ {\rho}\_{1, \sigma}-a\_{1, \dagger} a\_{1, 0.1 a ^ {\_{6 , \sigma} a ^ {\dagger}\_{1, \rho} a\_{3, \rho} a\_{2, \sigma}-0.1 a ^ {\dagger}\_{6, \sigma} a ^ {\dagger}\_{1, \rho} a\_{2, \rho} a\_{3 , \sigma}-0.1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{3, \rho} a\_{2, \sigma}-0.1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{2 , \rho}\_{3, \sigma} $ $ $ $-0.1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2, \rho} a\_{6, \rho} a\_{1, \sigma}-0.1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2 , \rho} a\_{1, \rho} a\_{6, \sigma}-0.1 a ^ {\dagger}\_{2, \sigma} a ^ {\dagger}\_{3, \rho} a\_{6, \rho} a\_{1, \sigma}-0.1 a ^ {\dagger}\_{2 , \sigma} a ^ {\dagger}\_{3, \rho} a\_{1, \rho} a\_{6, \sigma}\Biggr)\\, \textrm{Ha}.</span><span class="sxs-lookup"><span data-stu-id="8279e-196">$$ H = \frac12 \sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}}\Biggr( 1.6 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{1,\rho} a\_{1,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{2,\rho} a\_{3,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{2,\rho} a\_{3,\sigma} $$ $$- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{1,\rho} a\_{6,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{1,\rho} a\_{6,\sigma}\Biggr)\\,\textrm{Ha}.</span></span>
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

##### <a name="particlehole-representation-object"></a><span data-ttu-id="8279e-197">파티클-구멍 표현 개체</span><span class="sxs-lookup"><span data-stu-id="8279e-197">Particle–Hole Representation Object</span></span> #####

<span data-ttu-id="8279e-198">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-198">This section is normative.</span></span>

<span data-ttu-id="8279e-199">파티클-구멍 표현 개체는 생성 및 annihilation 연산자가 Hartree와 같은 사용 된 참조 상태에서 excitations를 설명 하는 파티클 구멍 표현과 관련 하 여 저장 된 정수를 지정 합니다. Fock 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-199">The particle–hole representation object specifies that the integrals stored are defined with respect to particle hole representation wherein the creation and annihilation operators describe excitations away from the reference state used, such as a Hartree–Fock state.</span></span>
<span data-ttu-id="8279e-200">개체는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-200">The object is OPTIONAL.</span></span>
<span data-ttu-id="8279e-201">개체를 지정 하지 않으면 Hamiltonian는 파티클 구멍 표현에 지정 되지 않은 것으로 해석 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-201">If the object is not specified then the Hamiltonian is to be interpreted as not given in particle-hole representation.</span></span>
<span data-ttu-id="8279e-202">`particle_hole_representation`의 값은 인덱스가 4 개의 정수이 고 해당 값이 숫자 및 문자열인 스파스 배열 수량 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-202">If present, the value of `particle_hole_representation` MUST be a sparse array quantity object whose indices are four integers, and whose values are a number and a string.</span></span>
<span data-ttu-id="8279e-203">각 요소 값의 문자열 부분에는 `'+'` 및 `'-'` 문자만 포함 해야 합니다 .이 값은 용어의 지정 된 인수가 파티클-구멍 표현에서 생성 또는 annihilation 연산자 인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-203">The string portion of the value of each element MUST contain only the characters `'+'` and `'-'` which specifies whether a given factor in the term is a creation or annihilation operator in the particle–hole representation.</span></span>  <span data-ttu-id="8279e-204">예를 들어 사이트 $i $에서 생성 되는 해당 및 사이트 $j, k $ 및 $l $에 생성 되는 파티클에를 `"-+++"` 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-204">For example `"-+++"` coresponds to a hole being created at site $i$ and particles being created at sites $j,k$ and $l$.</span></span>

> [!NOTE]
> <span data-ttu-id="8279e-205">`particle_hole_representation`의 값이 스파스 배열 수량 개체 이기 때문에 `unit` 및 `format` 속성을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-205">As the value of the `particle_hole_representation` is a sparse array quantity object, the `unit` and `format` properties must be specified.</span></span>
> <span data-ttu-id="8279e-206">허용 되는 단위는 표 1에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-206">Acceptable units include are listed in Table 1.</span></span>
> <span data-ttu-id="8279e-207">`format` 속성은 필수 이며 Hamiltonian 계수가 조밀한 또는 스파스 배열로 지정 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-207">The `format` property is required, and indicates whether the Hamiltonian coefficients are specified as a dense or sparse array.</span></span>
> <span data-ttu-id="8279e-208">현재 버전에서는 지정 되지 않은 모든 요소를 $0 $로 해석 하 여 스파스 배열만 지원 되지만 이후 버전에서는 `format` 속성의 추가 값에 대 한 지원을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-208">In the current version, only sparse arrays are supported, with interpretation that all unspecified elements are $0$, but future versions may add support for additional values of the `format` property.</span></span>

### <a name="initial-state-section"></a><span data-ttu-id="8279e-209">초기 상태 섹션</span><span class="sxs-lookup"><span data-stu-id="8279e-209">Initial State Section</span></span> ###

<span data-ttu-id="8279e-210">Initial_state_suggestion 개체는 지정 된 Hamiltonian에 대 한 관심의 초기 퀀텀 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-210">The initial_state_suggestion object specifies initial quantum states of interest to the specified Hamiltonian.</span></span> <span data-ttu-id="8279e-211">이 개체는 JSON `state` 개체의 배열 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-211">This object must be an array of JSON `state` objects.</span></span>

#### <a name="state-object"></a><span data-ttu-id="8279e-212">상태 개체</span><span class="sxs-lookup"><span data-stu-id="8279e-212">State object</span></span> ####

<span data-ttu-id="8279e-213">각 상태는 차지한 superposition을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-213">Each states represents a superposition of occupied orbitals.</span></span> <span data-ttu-id="8279e-214">각 상태 개체에는 문자열을 포함 하는 `label` 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-214">Each state object MUST have a `label` property containing a string.</span></span> <span data-ttu-id="8279e-215">각 상태 개체에는 기준 상태의 배열과 정규화 되지 않은 amplitudes을 포함 하는 `superposition` 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-215">Each state object MUST have a `superposition` property containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="8279e-216">예를 들어 초기 상태 $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0} $ $ $ $ \ket{E} = \frac{0.1 (a ^ {\dagger}\_{1) , \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) + 0.2 (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \uparrow}a ^ {\dagger}\_{2, \downarrow})} {\sqrt{| 0.1 | ^ 2 + | 0.2 | ^ 2}} \ket{0} $ $입니다. 표시 되는</span><span class="sxs-lookup"><span data-stu-id="8279e-216">For example, the initial states $$ \ket{G0}=\ket{G1}=\ket{G2}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0} $$ $$ \ket{E}=\frac{0.1 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})+0.2 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\uparrow}a^{\dagger}\_{2,\downarrow})}{\sqrt{|0.1|^2+|0.2|^2}}\ket{0} $$ are represented by</span></span>
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

#### <a name="basis-set-object"></a><span data-ttu-id="8279e-217">기본 설정 개체</span><span class="sxs-lookup"><span data-stu-id="8279e-217">Basis Set Object</span></span> ####

<span data-ttu-id="8279e-218">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-218">This section is normative.</span></span>

<span data-ttu-id="8279e-219">각 정수 계열 집합 개체에는 `basis_set` 속성이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-219">Each integral set object MAY have a `basis_set` property.</span></span>
<span data-ttu-id="8279e-220">`basis_set` 속성 값이 있는 경우 `type` 및 `name`라는 두 개의 속성이 있는 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-220">If present, the value of the `basis_set` property MUST be an object with two properties, `type` and `name`.</span></span>

<span data-ttu-id="8279e-221">`basis_set` 속성 값으로 식별 되는 기본 함수는 실제 값 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-221">The basis functions identified by the value of the `basis_set` property MUST be real-valued.</span></span>

> [!NOTE]
> <span data-ttu-id="8279e-222">이 사양의 이후 버전에서는 모든 기본 함수가 실제 값 이라고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-222">The assumption that all basis functions are real-valued may be relaxed in future versions of this specification.</span></span>

## <a name="tables-and-lists"></a><span data-ttu-id="8279e-223">테이블 및 목록</span><span class="sxs-lookup"><span data-stu-id="8279e-223">Tables and Lists</span></span> ##

### <a name="table-1-allowed-physical-units"></a><span data-ttu-id="8279e-224">표 1.</span><span class="sxs-lookup"><span data-stu-id="8279e-224">Table 1.</span></span> <span data-ttu-id="8279e-225">허용 된 물리적 단위</span><span class="sxs-lookup"><span data-stu-id="8279e-225">Allowed Physical Units</span></span> ###

<span data-ttu-id="8279e-226">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-226">This section is normative.</span></span>

<span data-ttu-id="8279e-227">단위를 지정 하는 문자열은 다음 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-227">Any string specifying a unit MUST be one of the following:</span></span>

- `hartree`
- `ev`

<span data-ttu-id="8279e-228">파서 및 생산자는 다음과 같은 단순 수량 개체를 동일 하 게 처리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-228">Parsers and producers MUST treat the following simple quantity objects as equivalent:</span></span>

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a><span data-ttu-id="8279e-229">표 2.</span><span class="sxs-lookup"><span data-stu-id="8279e-229">Table 2.</span></span> <span data-ttu-id="8279e-230">허용 되는 인덱스 규칙</span><span class="sxs-lookup"><span data-stu-id="8279e-230">Allowed Index Conventions</span></span> ###

<span data-ttu-id="8279e-231">이 섹션은 규범입니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-231">This section is normative.</span></span>

<span data-ttu-id="8279e-232">인덱스 규칙을 지정 하는 문자열은 다음 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-232">Any string specifying an index convention MUST be one of the following:</span></span>

- `mulliken`

<span data-ttu-id="8279e-233">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-233">This section is informative.</span></span>

<span data-ttu-id="8279e-234">이 사양의 이후 버전에는 추가 인덱스 규칙이 도입 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-234">Additional index conventions may be introduced in future versions of this specification.</span></span>

#### <a name="interpretation-of-index-conventions"></a><span data-ttu-id="8279e-235">인덱스 규칙의 해석</span><span class="sxs-lookup"><span data-stu-id="8279e-235">Interpretation of Index Conventions</span></span> ####

<span data-ttu-id="8279e-236">이 섹션은 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8279e-236">This section is informative.</span></span>
