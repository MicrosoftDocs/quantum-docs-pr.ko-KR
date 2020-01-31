---
title: 파일 구조 | Microsoft Docs
description: 'Q # 파일 구조'
author: QuantumWriter
uid: microsoft.quantum.language.file-structure
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 364d353c55bda38f227456909755d13dc7e67080
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76821085"
---
# <a name="file-structure"></a><span data-ttu-id="8d5b8-103">파일 구조</span><span class="sxs-lookup"><span data-stu-id="8d5b8-103">File Structure</span></span>

<span data-ttu-id="8d5b8-104">Q # 파일은 네임 스페이스 선언 시퀀스로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-104">A Q# file consists of a sequence of namespace declarations.</span></span>
<span data-ttu-id="8d5b8-105">각 네임 스페이스 선언에는 사용자 정의 형식, 작업 및 함수에 대 한 선언이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-105">Each namespace declaration contains declarations for user-defined types, operations, and functions.</span></span>
<span data-ttu-id="8d5b8-106">네임 스페이스 선언에는 임의의 순서 대로 각 선언 형식이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-106">A namespace declaration may contain any number of each type of declaration, and in any order.</span></span>
<span data-ttu-id="8d5b8-107">네임 스페이스 선언 외부에 나타날 수 있는 유일한 텍스트는 주석입니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-107">The only text that can appear outside of a namespace declaration is comments.</span></span>
<span data-ttu-id="8d5b8-108">특히 네임 스페이스에 대 한 문서 주석은 선언 앞에 나옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-108">In particular, documentation comments for a namespace precede the declaration.</span></span>

## <a name="namespace-declarations"></a><span data-ttu-id="8d5b8-109">네임스페이스 선언</span><span class="sxs-lookup"><span data-stu-id="8d5b8-109">Namespace Declarations</span></span>

<span data-ttu-id="8d5b8-110">Q # 파일은 일반적으로 정확히 하나의 네임 스페이스 선언을 포함 하지만, 없거나 비어 있거나 주석을 포함 하거나, 여러 네임 스페이스를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-110">A Q# file will typically have exactly one namespace declaration, but may have none (and be empty or just contain comments) or may contain multiple namespaces.</span></span>
<span data-ttu-id="8d5b8-111">네임 스페이스 선언은 중첩 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-111">Namespace declarations may not be nested.</span></span>

<span data-ttu-id="8d5b8-112">동일한 네임 스페이스는 동일한 이름을 가진 형식, 작업 또는 함수 선언이 없으면 함께 컴파일되는 여러 Q # 파일에 선언할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-112">The same namespace may be declared in multiple Q# files that are compiled together, as long as there are no type, operation, or function declarations with the same name.</span></span>
<span data-ttu-id="8d5b8-113">특히 선언이 동일한 경우에도 여러 파일에서 동일한 네임 스페이스에 동일한 형식을 정의 하는 것은 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-113">In particular, it is invalid to define the same type in the same namespace in multiple files, even if the declarations are identical.</span></span>

<span data-ttu-id="8d5b8-114">네임 스페이스 선언은 `namespace`키워드와 네임 스페이스 이름, 여는 중괄호 `{`, 네임 스페이스에 포함 된 선언 및 닫는 중괄호 `}`으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-114">A namespace declaration consists of the keyword `namespace`, followed by the name of the namespace, an open brace `{`, the declarations contained in the namespace, and a close brace `}`.</span></span>
<span data-ttu-id="8d5b8-115">네임 스페이스 이름은 마침표로 구분 된 하나 이상의 법적 기호 시퀀스의 .NET 패턴을 따릅니다 `.`.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-115">Namespace names follow the .NET pattern of a sequence of one or more legal symbols separated by periods `.`.</span></span>
<span data-ttu-id="8d5b8-116">예를 들어 `MyQuantumStuff` 및 `Microsoft.Quantum.Canon`는 유효한 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-116">For instance, `MyQuantumStuff` and `Microsoft.Quantum.Canon` are valid namespace names.</span></span>
<span data-ttu-id="8d5b8-117">규칙에 따라 네임 스페이스 이름의 기호는 대문자로 되어 있지만 반드시 필요한 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-117">By convention, the symbols in a namespace name are capitalized, but this is not required.</span></span>

<span data-ttu-id="8d5b8-118">선언은 네임 스페이스 선언에서 임의의 순서로 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-118">Declarations may appear in any order in a namespace declaration.</span></span>
<span data-ttu-id="8d5b8-119">파일에서 나중에 선언 된 형식 또는 callables에 대 한 참조가 제대로 확인 됩니다. 형식, 작업 또는 함수 선언이 참조 앞에 오지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-119">References to types or callables declared further down in a file are resolved properly; there is no need for the type, operation, or function declaration to precede a reference to it.</span></span>

## <a name="open-directives"></a><span data-ttu-id="8d5b8-120">지시문 열기</span><span class="sxs-lookup"><span data-stu-id="8d5b8-120">Open Directives</span></span>

<span data-ttu-id="8d5b8-121">네임 스페이스 블록 내에서 `open` 지시어를 사용 하 여 특정 네임 스페이스에 정의 된 모든 형식 및 callables을 가져와서 정규화 되지 않은 이름으로 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-121">Within a namespace block, the `open` directive may be used to import all types and callables defined in a certain namespace and refer to them by their unqualified name.</span></span> 

<span data-ttu-id="8d5b8-122">이러한 `open` 지시어는 `open` 키워드로 구성 된 다음 열 네임 스페이스와 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-122">Such an `open` directive consists of the `open` keyword, followed by the namespace to be opened and a terminating semicolon.</span></span>

<span data-ttu-id="8d5b8-123">예를 들어</span><span class="sxs-lookup"><span data-stu-id="8d5b8-123">For instance,</span></span>

```qsharp
open Microsoft.Quantum.Canon;
```

<span data-ttu-id="8d5b8-124">필요에 따라 열린 네임 스페이스의 짧은 이름을 정의 하 여 해당 네임 스페이스의 모든 요소를 정의 된 약식 이름으로 정규화 하 고 필요에 따라 정규화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-124">Optionally, a short name for the opened namespace may be defined such that all elements from that namespace can (and need) to be qualified by the defined short name.</span></span> <span data-ttu-id="8d5b8-125">이러한 짧은 이름은 `open` 지시문에서 세미콜론 앞에 `as` 키워드를 추가 하 여 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-125">Such a short name is defined by adding the keyword `as` followed by the desired short name before the semicolon in an `open` directive:</span></span>

```qsharp
open Microsoft.Quantum.Math as Math;
```

<span data-ttu-id="8d5b8-126">모든 `open` 지시문은 네임 스페이스 블록의 `function`, `operation`또는 `newtype` 선언 앞에 나와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-126">All `open` directives must appear before any `function`, `operation`, or `newtype` declarations in the namespace block.</span></span>
<span data-ttu-id="8d5b8-127">`open` 지시문은 파일 내의 전체 네임 스페이스 블록에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-127">The `open` directive applies to the entire namespace block within a file.</span></span>

## <a name="user-defined-type-declarations"></a><span data-ttu-id="8d5b8-128">사용자 정의 형식 선언</span><span class="sxs-lookup"><span data-stu-id="8d5b8-128">User-Defined Type Declarations</span></span>

<span data-ttu-id="8d5b8-129">Q #에서는 [q # 형식 모델](xref:microsoft.quantum.language.type-model) 섹션에 설명 된 대로 사용자가 새 사용자 정의 형식을 선언할 수 있는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-129">Q# provides a way for users to declare new user-defined types, as described in the [Q# type model](xref:microsoft.quantum.language.type-model) section.</span></span>
<span data-ttu-id="8d5b8-130">사용자 정의 형식은 기본 형식이 동일한 경우에도 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-130">User-defined types are distinct even if the base types are identical.</span></span>
<span data-ttu-id="8d5b8-131">특히 기본 형식이 동일한 경우에도 두 사용자 정의 형식의 값 사이에 자동 변환이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-131">In particular, there is no automatic conversion between values of two user-defined types even if the underlying types are identical.</span></span>

<span data-ttu-id="8d5b8-132">사용자 정의 형식 선언은 `newtype`키워드로 구성 된 다음 사용자 정의 형식 이름, `=`, 유효한 형식 사양 및 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-132">A user-defined type declaration consists of the keyword `newtype`, followed by the name of the user-defined type, an `=`, a valid type specification, and a terminating semicolon.</span></span>

<span data-ttu-id="8d5b8-133">예:</span><span class="sxs-lookup"><span data-stu-id="8d5b8-133">For example:</span></span>

```qsharp
newtype PairOfInts = (Int, Int);
```

<span data-ttu-id="8d5b8-134">각 Q # 소스 파일은 원하는 수의 사용자 정의 형식을 선언할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-134">Each Q# source file may declare any number of user-defined types.</span></span>
<span data-ttu-id="8d5b8-135">형식 이름은 네임 스페이스 내에서 고유 해야 하며 작업 및 함수 이름과 충돌 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-135">Type names must be unique within a namespace and may not conflict with operation and function names.</span></span>

<span data-ttu-id="8d5b8-136">사용자 정의 형식 간에 순환 종속성을 정의할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-136">It is not possible to define circular dependencies between user defined types.</span></span> <span data-ttu-id="8d5b8-137">따라서 Q # 내에서 재귀 형식을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-137">Recursive types are thus not possible within Q#.</span></span>

## <a name="operation-declarations"></a><span data-ttu-id="8d5b8-138">작업 선언</span><span class="sxs-lookup"><span data-stu-id="8d5b8-138">Operation Declarations</span></span>

<span data-ttu-id="8d5b8-139">작업은 Q #의 핵심 이며, 다른 언어의 함수와 거의 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-139">Operations are the core of Q#, roughly analogous to functions in other languages.</span></span>
<span data-ttu-id="8d5b8-140">각 Q # 소스 파일은 원하는 수의 작업을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-140">Each Q# source file may define any number of operations.</span></span>

<span data-ttu-id="8d5b8-141">작업 이름은 네임 스페이스 내에서 고유 해야 하며 형식 및 함수 이름과 충돌 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-141">Operation names must be unique within a namespace and may not conflict with type and function names.</span></span>

<span data-ttu-id="8d5b8-142">작업 선언은 `operation`키워드, 작업의 인수를 정의 하는 형식화 된 식별자 튜플, 작업에 대 한 인수를 정의 하는 형식화 된 식별자 튜플, 콜론 `:`, 작업의 결과 형식에 대 한 인수를 정의 하는 형식 주석, 선택적인 중괄호 `{`, 작업 선언 본문, 최종 닫는 중괄호 `}`로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-142">An operation declarations consists of the keyword `operation`, followed by the symbol that is the operation’s name, a typed identifier tuple that defines the arguments to the operation, a colon `:`, a type annotation that describes the operation’s result type, optionally an annotation with the operation characteristics, an open brace `{`, the body of the operation declaration, and a final closing brace `}`.</span></span>

<span data-ttu-id="8d5b8-143">작업 선언의 본문은 기본 구현 또는 특수화 목록으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-143">The body of the operation declaration either consists of the default implementation or of a list of specializations.</span></span>
<span data-ttu-id="8d5b8-144">기본 본문 특수화의 구현만 명시적으로 지정 해야 하는 경우에는 선언 내에서 직접 기본 구현을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-144">The default implementation can be specified directly within the declaration if only the implementation of the default body specialization needs to specified explicitly.</span></span>
<span data-ttu-id="8d5b8-145">이 경우 선언에서 작업 특성이 포함 된 주석은 컴파일러가 기본 구현을 기반으로 하 여 다른 특수화를 자동으로 생성 하는지 확인 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-145">In this case, an annotation with the operation characteristics in the declaration is useful to ensure that the compiler auto-generates other specializations based on the default implementation.</span></span> 

<span data-ttu-id="8d5b8-146">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-146">For example</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```

<span data-ttu-id="8d5b8-147">작업 특성은 선언 된 작업에 적용할 수 있는 함수의 종류와 적용 되는 결과를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-147">Operation characteristics define what kinds of functors can be applied to the declared operation, and what effect they have.</span></span> <span data-ttu-id="8d5b8-148">작업에서 단일 변환을 구현 하는 경우 *adjointed* 또는 *제어*될 때 작업이 작동 하는 방식을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-148">If an operation implements a unitary transformation, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span>
<span data-ttu-id="8d5b8-149">이러한 특수화의 존재는 작업 시그니처의 일부로 선언할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-149">The existence of these specializations can be declared as part of the operation signature.</span></span> <span data-ttu-id="8d5b8-150">이렇게 암시적으로 선언 된 각 특수화에 해당 하는 구현은 컴파일러에 의해 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-150">The corresponding implementation for each such implicitly declared specialization is then generated by the compiler.</span></span> <span data-ttu-id="8d5b8-151">위의 예제에서 adjoint, 제어 된 adjoint 특수화는 컴파일러에 의해 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-151">In the example above, an adjoint, a controlled, and a controlled adjoint specialization are generated by the compiler.</span></span> 

<span data-ttu-id="8d5b8-152">컴파일러가 구현을 생성할 수 없는 경우에는 명시적으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-152">In the case where the implementation cannot be generated by the compiler, it can be explicitly specified.</span></span> <span data-ttu-id="8d5b8-153">이러한 명시적 특수화 선언은 특정 특수화를 빌드하는 방법이 나 사용자 정의 구현을 명확 하 게 하는 적절 한 세대 지시문으로 구성 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-153">Such explicit specialization declarations can either consist of a suitable generation directive that clarify how a certain specialization is to be built, or a user defined implementation.</span></span> <span data-ttu-id="8d5b8-154">위의 `PrepareEntangledPair` 코드는 다음 코드와 같이 명시적 특수화 선언이 포함 된 코드와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-154">The code in `PrepareEntangledPair` above for example is equivalent to the code below containing explicit specialization declarations:</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
<span data-ttu-id="8d5b8-155">키워드 `auto`은 컴파일러가 특수화 구현을 생성 하는 방법을 결정 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-155">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>
<span data-ttu-id="8d5b8-156">컴파일러가 더 정확한 생성 지시문과 같은 추가 지침 없이 특정 특수화에 대 한 구현을 생성할 수 없는 경우 또는 보다 효율적인 구현을 지정할 수 있는 경우에도 구현이 수동으로 정의 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-156">If the compiler cannot generate the implementation for a certain specialization without further instructions - like a more precise generation directive -, or if a more efficient implementation can be given, then the implementation may also be manually defined.</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```

<span data-ttu-id="8d5b8-157">위의 예제에서 `adjoint invert;`는 본문 구현을 반전 하 여 adjoint 특수화가 생성 되 고 `controlled adjoint invert;`는 제어 된 특수화의 지정 된 구현을 반전 하 여 제어 된 adjoint 특수화가 생성 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-157">In the example above, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="8d5b8-158">`Adjoint` 및/또는 `Controlled` 함수의 응용 프로그램을 지 원하는 작업의 경우 반환 형식은 반드시 `Unit`해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-158">For an operation to support application of the `Adjoint` and/or `Controlled` functor, its return type necessarily needs to be `Unit`.</span></span> 


### <a name="explicit-specialization-declarations"></a><span data-ttu-id="8d5b8-159">명시적 특수화 선언</span><span class="sxs-lookup"><span data-stu-id="8d5b8-159">Explicit Specialization Declarations</span></span>

<span data-ttu-id="8d5b8-160">Q # 작업에는 다음과 같은 명시적 특수화 선언이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-160">Q# operations may contain the following explicit specialization declarations:</span></span>

- <span data-ttu-id="8d5b8-161">`body` 특수화는 함수 적용 되지 않은 작업의 구현을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-161">The `body` specialization specifies the implementation of the operation with no functors applied.</span></span>
- <span data-ttu-id="8d5b8-162">`adjoint` 특수화는 적용 된 `Adjoint` 함수를 사용 하 여 작업의 구현을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-162">The `adjoint` specialization specifies the implementation of the operation with the `Adjoint` functor applied.</span></span>
- <span data-ttu-id="8d5b8-163">`controlled` 특수화는 적용 된 `Controlled` 함수를 사용 하 여 작업의 구현을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-163">The `controlled` specialization specifies the implementation of the operation with the `Controlled` functor applied.</span></span>
- <span data-ttu-id="8d5b8-164">`controlled adjoint` 특수화는 `Adjoint` 및 `Controlled` 함수 적용 된 작업의 구현을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-164">The `controlled adjoint` specialization specifies the implementation of the operation with both the `Adjoint` and `Controlled` functors applied.</span></span>
  <span data-ttu-id="8d5b8-165">두 함수 commute 이후이 특수화의 이름을 `adjoint controlled`로 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-165">This specialization can also be named `adjoint controlled`, since the two functors commute.</span></span>


<span data-ttu-id="8d5b8-166">작업 특수화는 특수화 태그 (예: `body`, `adjoint`등)와 다음 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-166">An operation specialization consists of the specialization tag (like e.g. `body`, or `adjoint`, etc.) followed by one of:</span></span>

- <span data-ttu-id="8d5b8-167">아래에 설명 된 명시적 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-167">An explicit declaration as described below.</span></span>
- <span data-ttu-id="8d5b8-168">다음 중 하나에 해당 하는 특수화를 생성 하는 방법을 컴파일러에 지시 하는 지시문입니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-168">A directive that tells the compiler how to generate the specialization, one of:</span></span>
  - <span data-ttu-id="8d5b8-169">`intrinsic`는 대상 컴퓨터에서 특수화가 제공 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-169">`intrinsic`, which indicates that the specialization is provided by the target machine.</span></span>
  - <span data-ttu-id="8d5b8-170">`distribute``controlled` 및 `controlled adjoint` 특수화와 함께 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-170">`distribute`, which may be used with the `controlled` and `controlled adjoint` specializations.</span></span>
    <span data-ttu-id="8d5b8-171">`controlled`와 함께 사용 하는 경우 `body`의 모든 작업에 `Controlled`를 적용 하 여 컴파일러가 특수화를 계산 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-171">When used with `controlled`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `body`.</span></span>
    <span data-ttu-id="8d5b8-172">`controlled adjoint`와 함께 사용 하는 경우 컴파일러는 `adjoint` 특수화의 모든 작업에 `Controlled`를 적용 하 여 특수화를 계산 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-172">When used with `controlled adjoint`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `adjoint` specialization.</span></span>
  - <span data-ttu-id="8d5b8-173">`invert`: 컴파일러가 `body`를 반전 하 여 `adjoint` 특수화를 계산 해야 함을 나타냅니다. 즉, 작업 순서를 반대로 하 고 각 항목에 adjoint를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-173">`invert`, which indicates that the compiler should compute the `adjoint` specialization by inverting the `body`, i.e. reversing the order of operations and applying the adjoint to each one.</span></span>
    <span data-ttu-id="8d5b8-174">`adjoint controlled`와 함께 사용 하는 경우 컴파일러에서 `controlled` 특수화를 반전 하 여 특수화를 계산 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-174">When used with `adjoint controlled`, this indicates that the compiler should compute the specialization by inverting the `controlled` specialization.</span></span>
  - <span data-ttu-id="8d5b8-175">`self`adjoint 특수화가 `body` 특수화와 동일 함을 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-175">`self`, to indicate that the adjoint specialization is the the same as the `body` specialization.</span></span>
    <span data-ttu-id="8d5b8-176">이는 `adjoint` 및 `adjoint controlled` 특수화에 대해 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-176">This is legal for the `adjoint` and `adjoint controlled` specializations.</span></span>
    <span data-ttu-id="8d5b8-177">`adjoint controlled`에서 `self` `adjoint controlled` 특수화가 `controlled` 특수화와 동일 하다는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-177">For `adjoint controlled`, `self` implies that the `adjoint controlled` specialization is the same as the `controlled` specialization.</span></span>
  - <span data-ttu-id="8d5b8-178">`auto`컴파일러에서 적용할 적절 한 지시문을 선택 해야 함을 나타내려면입니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-178">`auto`, to indicate that the compiler should select an appropriate directive to apply.</span></span>
    <span data-ttu-id="8d5b8-179">`auto` `body` 특수화에 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-179">`auto` may not be used for the `body` specialization.</span></span>

<span data-ttu-id="8d5b8-180">지시문과 `auto` 모두에는 닫는 세미콜론 `;`필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-180">The directives and `auto` all require a closing semi-colon `;`.</span></span>
<span data-ttu-id="8d5b8-181">`body`의 명시적 선언이 제공 되는 경우 `auto` 지시문은 다음 세대 지시문으로 확인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-181">The `auto` directive resolves to the following generation directive if an explicit declaration of the `body` is provided:</span></span>

- <span data-ttu-id="8d5b8-182">`adjoint` 특수화는 지시문 `invert`에 따라 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-182">The `adjoint` specialization is generated according to the directive `invert`.</span></span>
- <span data-ttu-id="8d5b8-183">`controlled` 특수화는 지시문 `distribute`에 따라 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-183">The `controlled` specialization is generated according to the directive `distribute`.</span></span>
- <span data-ttu-id="8d5b8-184">`adjoint controlled` 특수화는 `controlled`에 대 한 명시적 선언이 `adjoint`에 대해 지정 되지 않은 경우 `invert` 지시문에 따라 생성 되 고 그렇지 않은 경우 `distribute`.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-184">The `adjoint controlled` specialization is generated according to the directive `invert` if an explicit declaration for `controlled` is given but not one for `adjoint`, and `distribute` otherwise.</span></span>

> [!TIP]   
> <span data-ttu-id="8d5b8-185">작업이 자체 adjoint 인 경우 생성 `self` 지시문을 통해 adjoint 또는 제어 된 adjoint 특수화를 명시적으로 지정 하 여 컴파일러가 최적화를 위해 해당 정보를 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-185">If an operation is self-adjoint, explicitly specify either the adjoint or the controlled adjoint specialization via the generation directive `self` to allow the compiler to make use of that information for optimization purposes.</span></span>

<span data-ttu-id="8d5b8-186">사용자 정의 구현을 포함 하는 특수화 선언은 인수 튜플 및 특수화를 구현 하는 Q # 코드가 포함 된 문 블록으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-186">A specialization declaration containing a user defined implementation consists of an argument tuple followed by a statement block with the Q# code that implements the specialization.</span></span>
<span data-ttu-id="8d5b8-187">인수 목록에서 `...`는 작업에 대해 전체적으로 선언 된 인수를 나타내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-187">In the argument list, `...` is used to represent the arguments declared for the operation as a whole.</span></span>
<span data-ttu-id="8d5b8-188">`body` 및 `adjoint`의 경우 인수 목록은 항상 `(...)`해야 합니다. `controlled` 및 `adjoint controlled`의 경우 인수 목록은 컨트롤의 배열을 표시 하 고 그 뒤에 `...`를 괄호로 묶어 나타내는 기호 여야 합니다. 예를 들어 `(controls,...)`합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-188">For `body` and `adjoint`, the argument list should always be `(...)`; for `controlled` and `adjoint controlled`, the argument list should be a symbol that represents the array of control qubits, followed by `...`, enclosed in parentheses; for example, `(controls,...)`.</span></span>

<span data-ttu-id="8d5b8-189">기본 본문 외에도 하나 이상의 특수화를 명시적으로 선언 해야 하는 경우 기본 본문의 구현은 적절 한 특수화 선언에도 래핑해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-189">If one or more specializations besides the default body need to be explicitly declared, then the implementation for the default body needs to be wrapped into a suitable specialization declaration as well:</span></span>

```qsharp
operation CountOnes(qubits: Qubit[]) : Int {

    body (...) // default body specialization
    {
        mutable n = 0;
        for (qubit in qubits) {
            set n += M(q) == One ? 1 | 0;
        }
        return n;
    }

    ...
```

### <a name="adjoint"></a><span data-ttu-id="8d5b8-190">Adjoint</span><span class="sxs-lookup"><span data-stu-id="8d5b8-190">Adjoint</span></span>

<span data-ttu-id="8d5b8-191">작업의 adjoint는 작업의 복합 복소수를 구현 하는 방법, 즉 "역방향으로 실행" 시 작업의 작동 방식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-191">The adjoint of an operation specifies how the complex conjugate transpose of the operation is implemented, i.e. how the operation acts when "run in reverse".</span></span>
<span data-ttu-id="8d5b8-192">Adjoint 없이 작업을 지정 하는 것은 유효 합니다. 예를 들어 측정 작업은 반전할 수 없으므로 adjoint를 갖지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-192">It is legal to specify an operation with no adjoint; for instance, measurement operations have no adjoint because they are not invertible.</span></span>
<span data-ttu-id="8d5b8-193">작업은 해당 선언에 adjoint 특수화의 암시적 또는 명시적 선언이 포함 된 경우 `Adjoint` 함수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-193">An operation supports the `Adjoint` functor if its declaration contains an implicit or explicit declaration of an adjoint specialization.</span></span>
<span data-ttu-id="8d5b8-194">명시적으로 선언 된 adjoint 특수화는 adjoint 특수화가 있음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-194">An explicitly declared controlled adjoint specialization implies the existence of an adjoint specialization.</span></span> 

<span data-ttu-id="8d5b8-195">본문이 반복 될 때까지 루프, set 문, 측정값, return 문 또는 `Adjoint` 함수를 지원 하지 않는 다른 작업에 대 한 호출을 포함 하는 작업의 경우에는 `invert` 또는 `auto` 지시문 다음에 adjoint 특수화 자동 생성이 가능 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-195">For operation whose body contains repeat-until-success loops, set statements, measurements, return statements, or calls to other operations that do not support the `Adjoint` functor, auto-generating an adjoint specialization following the `invert` or `auto` directive is not possible.</span></span>

### <a name="controlled"></a><span data-ttu-id="8d5b8-196">제어</span><span class="sxs-lookup"><span data-stu-id="8d5b8-196">Controlled</span></span>

<span data-ttu-id="8d5b8-197">작업의 제어 된 버전은 퀀텀 제어 버전의 작업을 구현 하는 방법을 지정 합니다. 즉, 조건 화 된 적용 될 때 작업의 작동 방식에는 퀀텀 레지스터가 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-197">The controlled version of an operation specifies how a quantum-controlled version of the operation is implemented, i.e. how an operation acts when applied conditioned on the state of a quantum register.</span></span>
<span data-ttu-id="8d5b8-198">자세한 내용은 [제어](xref:microsoft.quantum.language.type-model#controlled) 된 섹션에서 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-198">A more complete description is provided in the [Controlled](xref:microsoft.quantum.language.type-model#controlled) section.</span></span>

<span data-ttu-id="8d5b8-199">제어 된 버전이 없는 작업을 지정 하는 것은 유효 합니다. 예를 들어, 측정 작업은 제어할 수 없으므로 제어 되는 버전이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-199">It is legal to specify an operation with no controlled version; for instance, measurement operations have no controlled version because they are not controllable.</span></span>
<span data-ttu-id="8d5b8-200">작업은 해당 선언에 제어 된 특수화의 암시적 또는 명시적 선언이 포함 된 경우에만 `Controlled` 함수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-200">An operation supports the `Controlled` functor if and only if its declaration contains an implicit or explicit declaration of a controlled specialization.</span></span>
<span data-ttu-id="8d5b8-201">명시적으로 선언 된 제어 된 adjoint 특수화는 제어 된 특수화가 있음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-201">An explicitly declared controlled adjoint specialization implies the existence of a controlled specialization.</span></span> 

<span data-ttu-id="8d5b8-202">본문이 `Controlled` 함수를 지원 하지 않는 다른 작업에 대 한 호출을 포함 하는 작업의 경우에는 `distribute` 또는 `auto` 지시문 다음에 제어 된 특수화를 자동으로 생성할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-202">For an operation whose body contains calls to other operations that does not support the `Controlled` functor, auto-generating a controlled specialization following the `distribute` or `auto` directive is not possible.</span></span>

### <a name="controlled-adjoint"></a><span data-ttu-id="8d5b8-203">제어 된 Adjoint</span><span class="sxs-lookup"><span data-stu-id="8d5b8-203">Controlled Adjoint</span></span>

<span data-ttu-id="8d5b8-204">작업의 제어 된 adjoint 버전은 작업의 adjoint의 퀀텀 제어 버전을 구현 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-204">The controlled adjoint version of an operation specifies how a quantum-controlled version of the adjoint of the operation is implemented.</span></span>
<span data-ttu-id="8d5b8-205">제어 된 adjoint 버전이 없는 작업을 지정 하는 것은 유효 합니다. 예를 들어, 측정 작업은 제어 또는 반전할 수 없기 때문에 제어 되는 adjoint 버전이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-205">It is legal to specify an operation with no controlled adjoint version; for instance, measurement operations have no controlled adjoint version because they are neither controllable nor invertible.</span></span>

<span data-ttu-id="8d5b8-206">작업에 대 한 제어 된 adjoint 특수화는 adjoint와 제어 된 특수화가 모두 있는 경우에만 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-206">A controlled adjoint specialization for an operation needs to exist if and only if both an adjoint and a controlled specialization exist.</span></span> <span data-ttu-id="8d5b8-207">이 경우 제어 되는 adjoint 특수화가 유추 되 고 명시적으로 정의 된 구현이 없는 경우 컴파일러에서 적절 한 특수화가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-207">In that case, the existence of the controlled adjoint specialization is inferred and an appropriate specialization is generated by the compiler if no implementation has been defined explicitly.</span></span> 

<span data-ttu-id="8d5b8-208">해당 본문에 제어 된 adjoint 버전이 없는 다른 작업에 대 한 호출이 포함 된 작업의 경우, `invert``distribute` 또는 `auto` 지시문 다음에 adjoint 특수화를 자동으로 생성 하는 것은 불가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-208">For an operation whose body contains calls to other operations that do not have a controlled adjoint version, auto-generating an adjoint specialization following the `invert`, `distribute` or `auto` directive is not possible.</span></span>


### <a name="examples"></a><span data-ttu-id="8d5b8-209">예시</span><span class="sxs-lookup"><span data-stu-id="8d5b8-209">Examples</span></span>

<span data-ttu-id="8d5b8-210">작업 선언은 다음과 같이 간단할 수 있습니다 .이는 기본 Pauli X 작업을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-210">An operation declaration might be as simple as the following, which defines the primitive Pauli X operation:</span></span>

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```

<span data-ttu-id="8d5b8-211">다음은 텔레포트 작업을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-211">The following defines the teleport operation.</span></span>

```qsharp
// Entangle two qubits.
// Assumes that both qubits are in the |0> state.
operation EPR (q1 : Qubit, q2 : Qubit) : Unit 
is Adj + Ctl {
    H(q2);
    CNOT(q2, q1);
}

// Teleport the quantum state of the source to the target.
// Assumes that the target is in the |0> state.
operation Teleport (source : Qubit, target : Qubit) : Unit {

    // Get a temporary for the Bell pair
    using (ancilla = Qubit())
    {
        // Create a Bell pair between the temporary and the target
        EPR(target, ancilla);

        // Do the teleportation
        Adjoint EPR (ancilla, source);

        if (MResetZ(source) == One) {
            X(target);
        }
        if (MResetZ(ancilla) == One) {
            Z(target);
        }
    }
}
```

## <a name="function-declarations"></a><span data-ttu-id="8d5b8-212">함수 선언</span><span class="sxs-lookup"><span data-stu-id="8d5b8-212">Function Declarations</span></span>

<span data-ttu-id="8d5b8-213">함수는 Q #에서 순수 하 게 사용할 수 있는 루틴입니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-213">Functions are purely classical routines in Q#.</span></span>
<span data-ttu-id="8d5b8-214">각 Q # 소스 파일은 원하는 수의 함수를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-214">Each Q# source file may define any number of functions.</span></span>

<span data-ttu-id="8d5b8-215">함수 선언은 `function`키워드와 함수 이름, 형식화 된 식별자 튜플, 함수의 반환 형식을 설명 하는 형식 주석, 함수의 구현을 설명 하는 문 블록으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-215">A function declaration consists of the keyword `function`, followed by the symbol that is the function’s name, a typed identifier tuple, a type annotation that describes the function's return type, and a statement block that describes the implementation of the function.</span></span>

<span data-ttu-id="8d5b8-216">함수를 정의 하는 문 블록은 `{`로 묶어야 하 고 다른 문 블록과 같이 `}` 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-216">The statement block defining a function must be enclosed in `{` and `}` like any other statement block.</span></span>

<span data-ttu-id="8d5b8-217">함수 이름은 네임 스페이스 내에서 고유 해야 하며 작업 및 형식 이름과 충돌 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-217">Function names must be unique within a namespace and may not conflict with operation and type names.</span></span>
<span data-ttu-id="8d5b8-218">함수는 이러한 기능을 할당 하거나이 작업을 호출할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-218">Functions may not allocate or borrow qubits, or call operations.</span></span> <span data-ttu-id="8d5b8-219">부분적으로 작업을 적용 하거나 작업의 형식화 된 값을 전달 하는 것은 문제가 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-219">Partial application of operations or passing around operation typed values is fine.</span></span>

<span data-ttu-id="8d5b8-220">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8d5b8-220">For example,</span></span>

```qsharp
function DotProduct(a : Double[], b : Double[]) : Double {
    if (Length(a) != Length(b)) {
        fail "Arrays are not compatible";
    }

    mutable accum = 0.0;
    for (i in 0..Length(a)-1) {
        set accum += a[i] * b[i];
    }
    return accum;
}
```
