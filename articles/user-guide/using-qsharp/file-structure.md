---
title: 'Q # 파일 구조'
description: 'Q # 파일의 구조 및 구문에 대해 설명 합니다.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
ms.openlocfilehash: cbee92c6d7e765237a7a42532dd7012b51421708
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430971"
---
# <a name="q-file-structure"></a><span data-ttu-id="f68a2-103">Q # 파일 구조</span><span class="sxs-lookup"><span data-stu-id="f68a2-103">Q# File Structure</span></span>

<span data-ttu-id="f68a2-104">모든 Q # 작업, 함수 및 사용자 정의 형식은 네임 스페이스 내에서 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-104">Every Q# operation, function, and user-defined type is defined within a namespace.</span></span>

<span data-ttu-id="f68a2-105">Q # 파일은 *네임 스페이스 선언*시퀀스로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-105">A Q# file consists of a sequence of *namespace declarations*.</span></span>
<span data-ttu-id="f68a2-106">각 네임 스페이스 선언에는 사용자 정의 형식, 작업 및 함수에 대 한 선언이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-106">Each namespace declaration contains declarations for user-defined types, operations, and functions.</span></span>
<span data-ttu-id="f68a2-107">네임 스페이스 선언에는 임의의 순서 대로 각 선언 형식이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-107">A namespace declaration may contain any number of each type of declaration, and in any order.</span></span>
<span data-ttu-id="f68a2-108">네임 스페이스 내에서 [사용자 정의 형식](xref:microsoft.quantum.guide.types#user-defined-types), [작업](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)및 [함수](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) 를 선언 하는 방법에 대 한 자세한 내용은 다음 링크를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f68a2-108">Follow these links for more details on declaring [user-defined types](xref:microsoft.quantum.guide.types#user-defined-types), [operations](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations), and [functions](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) within a namespace.</span></span>

<span data-ttu-id="f68a2-109">네임 스페이스 선언 외부에 나타날 수 있는 유일한 텍스트는 주석입니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-109">The only text that can appear outside of a namespace declaration is comments.</span></span>
<span data-ttu-id="f68a2-110">특히 네임 스페이스에 대 한 문서 주석 (아래 세부 정보)이 선언 앞에 나옵니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-110">In particular, documentation comments (more details below) for a namespace precede the declaration.</span></span>

## <a name="namespace-declarations"></a><span data-ttu-id="f68a2-111">네임스페이스 선언</span><span class="sxs-lookup"><span data-stu-id="f68a2-111">Namespace Declarations</span></span>

<span data-ttu-id="f68a2-112">Q # 파일은 일반적으로 정확히 하나의 네임 스페이스 선언을 포함 하지만, 없거나 비어 있거나 주석을 포함 하거나, 여러 네임 스페이스를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-112">A Q# file will typically have exactly one namespace declaration, but may have none (and be empty or just contain comments) or may contain multiple namespaces.</span></span>
<span data-ttu-id="f68a2-113">네임 스페이스 선언은 중첩 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-113">Namespace declarations may not be nested.</span></span>

<span data-ttu-id="f68a2-114">동일한 네임 스페이스는 동일한 이름을 가진 형식, 작업 또는 함수 선언이 없으면 함께 컴파일되는 여러 Q # 파일에 선언할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-114">The same namespace may be declared in multiple Q# files that are compiled together, as long as there are no type, operation, or function declarations with the same name.</span></span>
<span data-ttu-id="f68a2-115">특히 선언이 동일한 경우에도 여러 파일에서 동일한 네임 스페이스에 동일한 형식을 정의 하는 것은 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-115">In particular, it is invalid to define the same type in the same namespace in multiple files, even if the declarations are identical.</span></span>

<span data-ttu-id="f68a2-116">네임 스페이스 선언은 키워드로 구성 됩니다 `namespace` . 그 다음에는 네임 스페이스 이름, 여는 중괄호 `{` , 네임 스페이스에 포함 된 선언 및 닫는 중괄호가 `}` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-116">A namespace declaration consists of the keyword `namespace`, followed by the name of the namespace, an open brace `{`, the declarations contained in the namespace, and a close brace `}`.</span></span>
<span data-ttu-id="f68a2-117">네임 스페이스 이름은 마침표로 구분 된 하나 이상의 법적 기호의 시퀀스에 대 한 .NET 패턴을 따릅니다 `.` .</span><span class="sxs-lookup"><span data-stu-id="f68a2-117">Namespace names follow the .NET pattern of a sequence of one or more legal symbols separated by periods `.`.</span></span>
<span data-ttu-id="f68a2-118">예를 들어 `MyQuantumStuff` 및 `Microsoft.Quantum.Intrinsic` 는 유효한 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-118">For instance, `MyQuantumStuff` and `Microsoft.Quantum.Intrinsic` are valid namespace names.</span></span>
<span data-ttu-id="f68a2-119">규칙에 따라 네임 스페이스 이름의 기호는 대문자로 되어 있지만 반드시 필요한 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-119">By convention, the symbols in a namespace name are capitalized, but this is not required.</span></span>

<span data-ttu-id="f68a2-120">파일에서 나중에 선언 된 형식 또는 callables에 대 한 참조가 제대로 확인 됩니다. 형식, 작업 또는 함수 선언이 참조 앞에 오지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-120">References to types or callables declared further down in a file are resolved properly; there is no need for the type, operation, or function declaration to precede a reference to it.</span></span>

## <a name="open-directives"></a><span data-ttu-id="f68a2-121">지시문 열기</span><span class="sxs-lookup"><span data-stu-id="f68a2-121">Open Directives</span></span>

<span data-ttu-id="f68a2-122">네임 스페이스 블록 내에서 `open` 지시문을 사용 하 여 특정 네임 스페이스에서 선언 된 모든 형식 및 callables을 가져와서 정규화 되지 않은 이름으로 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-122">Within a namespace block, the `open` directive may be used to import all types and callables declared in a certain namespace and refer to them by their unqualified name.</span></span>
<span data-ttu-id="f68a2-123">이러한 `open` 지시문은 키워드로 구성 된 `open` 다음 열 네임 스페이스와 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-123">Such an `open` directive consists of the `open` keyword, followed by the namespace to be opened and a terminating semicolon.</span></span>

> [!NOTE] 
> <span data-ttu-id="f68a2-124">모든 `open` 지시문은 `function` `operation` `newtype` 네임 스페이스 블록의, 또는 선언 앞에 나와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-124">All `open` directives must appear before any `function`, `operation`, or `newtype` declarations in the namespace block.</span></span>

<span data-ttu-id="f68a2-125">필요에 따라 열린 네임 스페이스의 짧은 이름을 정의 하 여 해당 네임 스페이스의 모든 요소를 정의 된 약식 이름으로 정규화 하 고 필요에 따라 정규화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-125">Optionally, a short name for the opened namespace may be defined such that all elements from that namespace can (and need) to be qualified by the defined short name.</span></span> <span data-ttu-id="f68a2-126">예를 들어 다음과 같은 네임 스페이스 선언 및 open 지시문이 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-126">For example, given the following namespace declaration and open directives,</span></span>

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

<span data-ttu-id="f68a2-127">선언 하는 작업이에서 작업을 사용 하는 경우를 `Op` `Microsoft.Quantum.Intrinsic` 사용 하 여 호출 `Op` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-127">if an operation we declare uses an operation `Op` from `Microsoft.Quantum.Intrinsic`, we would call it by simply using `Op`.</span></span>
<span data-ttu-id="f68a2-128">그러나에서 특정 함수를 호출 하려는 경우를 `Fn` `Microsoft.Quantum.Math` 사용 하 여 호출 해야 `Math.Fn` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-128">However, if we wanted a call a certain function `Fn` from `Microsoft.Quantum.Math`, we would need to call it using `Math.Fn`.</span></span>

<span data-ttu-id="f68a2-129">`open`지시문은 파일 내의 전체 네임 스페이스 블록에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-129">The `open` directive applies to the entire namespace block within a file.</span></span>
<span data-ttu-id="f68a2-130">따라서 위와 같은 Q # 파일에 추가 네임 스페이스를 정의 하는 경우에는 `NS` 두 번째 네임 스페이스에 정의 된 모든 작업/함수/형식이 열에 대 한 액세스 권한을 갖지 않습니다 `Microsoft.Quantum.Intrinsic` `Microsoft.Quantum.Math` .</span><span class="sxs-lookup"><span data-stu-id="f68a2-130">Hence, if we were to define an additional namespace in the same Q# file as `NS` above, then any operations/functions/types defined in the second namespace would not have access to anything from `Microsoft.Quantum.Intrinsic` or `Microsoft.Quantum.Math` unless we repeated the open directives therein.</span></span> 

<span data-ttu-id="f68a2-131">현재 네임 스페이스에서 열려 *있지* 않은 다른 네임 스페이스에 정의 된 형식 또는 호출 가능 이름은 정규화 된 이름으로 참조 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-131">A type or callable defined in another namespace that is *not* opened in the current namespace must be referenced by its fully-qualified name.</span></span>
<span data-ttu-id="f68a2-132">예를 들어 네임 스페이스가 `Op` `X.Y` `X.Y.Op` `X.Y` 현재 블록에서 이전에 열리지 않는 한 네임 스페이스에서 이름이 지정 된 작업은 정규화 된 이름으로 참조 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-132">For example, an operation named `Op` from the `X.Y` namespace must be referenced by its fully-qualified name `X.Y.Op`, unless the `X.Y` namespace has been opened earlier in the current block.</span></span> <span data-ttu-id="f68a2-133">위에서 설명한 것 처럼 네임 스페이스를 연 경우에도 `X` 작업을로 참조할 수 없습니다 `Y.Op` .</span><span class="sxs-lookup"><span data-stu-id="f68a2-133">As mentioned above, even if the `X` namespace has been opened, it is not possible to reference the operation as `Y.Op`.</span></span>
<span data-ttu-id="f68a2-134">의 약식 이름이 `Z` `X.Y` 해당 네임 스페이스 및 파일에 정의 된 경우에는를 `Op` 로 참조 해야 `Z.Op` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-134">If a short name `Z` for `X.Y` has been defined in that namespace and file, then `Op` needs to be referred to as `Z.Op`.</span></span> 

<span data-ttu-id="f68a2-135">일반적으로 지시문을 사용 하 여 네임 스페이스를 포함 하는 것이 좋습니다 `open` .</span><span class="sxs-lookup"><span data-stu-id="f68a2-135">It is usually better to include a namespace by using an `open` directive.</span></span>
<span data-ttu-id="f68a2-136">두 네임 스페이스가 같은 이름을 사용 하 여 구문을 정의 하 고 현재 소스가 양쪽에서 구문을 사용 하는 경우 정규화 된 이름을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-136">Using a fully-qualified name is required if two namespaces define constructs with the same name, and the current source uses constructs from both.</span></span>

<span data-ttu-id="f68a2-137">Q #은 다른 .NET 언어로 이름을 지정 하는 것과 동일한 규칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-137">Q# follows the same rules for naming as other .NET languages.</span></span>
<span data-ttu-id="f68a2-138">그러나 Q #에서는 네임 스페이스에 대 한 상대 참조를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-138">However, Q# does not support relative references to namespaces.</span></span>
<span data-ttu-id="f68a2-139">즉, 네임 스페이스를 연 경우 이름이 인 작업에 대 `a.b` 한 참조는 `c.d` 전체 이름이 있는 작업으로 확인 *되지* 않습니다 `a.b.c.d` .</span><span class="sxs-lookup"><span data-stu-id="f68a2-139">That is, if the namespace `a.b` has been opened, a reference to an operation named `c.d` will *not* be resolved to an operation with full name `a.b.c.d`.</span></span>

## <a name="formatting"></a><span data-ttu-id="f68a2-140">서식 지정</span><span class="sxs-lookup"><span data-stu-id="f68a2-140">Formatting</span></span>

<span data-ttu-id="f68a2-141">대부분의 Q # 문과 지시문은 종료 세미콜론 ()으로 끝납니다 `;` .</span><span class="sxs-lookup"><span data-stu-id="f68a2-141">Most Q# statements and directives end with a terminating semicolon, `;`.</span></span>
<span data-ttu-id="f68a2-142">문과 `for` `operation` 문 블록 (아래 참조)으로 끝나는 문과 선언에는 종료 세미콜론이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-142">Statements and declarations such as `for` and `operation` that end with a statement block (see below) do not require a terminating semicolon.</span></span>
<span data-ttu-id="f68a2-143">각 문 설명에는 종료 세미콜론이 필요한 지 여부에 대 한 설명이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-143">Each statement description notes whether the terminating semicolon is required.</span></span>

<span data-ttu-id="f68a2-144">식, 선언 및 지시문과 같은 문은 여러 줄에 걸쳐 분할 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-144">Statements, like expressions, declarations, and directives, may be broken out across multiple lines.</span></span>
<span data-ttu-id="f68a2-145">한 줄에 문이 여러 개 있는 것은 피해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-145">Having multiple statements on a single line should be avoided.</span></span>

## <a name="statement-blocks"></a><span data-ttu-id="f68a2-146">문 블록</span><span class="sxs-lookup"><span data-stu-id="f68a2-146">Statement Blocks</span></span>

<span data-ttu-id="f68a2-147">Q # 문은 문 블록으로 그룹화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-147">Q# statements are grouped into statement blocks.</span></span>
<span data-ttu-id="f68a2-148">문 블록은 여는 것으로 시작 하 `{` 고 닫는로 끝납니다 `}` .</span><span class="sxs-lookup"><span data-stu-id="f68a2-148">A statement block starts with an opening `{` and ends with a closing `}`.</span></span>

<span data-ttu-id="f68a2-149">다른 블록 내에 어휘를 싸인 문 블록은 포함 하는 블록의 하위 블록으로 간주 됩니다. 포함 및 하위 블록은 외부 및 내부 블록이 라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-149">A statement block that is lexically enclosed within another block is considered to be a sub-block of the containing block; containing and sub-blocks are also called outer and inner blocks.</span></span>

## <a name="comments"></a><span data-ttu-id="f68a2-150">의견</span><span class="sxs-lookup"><span data-stu-id="f68a2-150">Comments</span></span>

<span data-ttu-id="f68a2-151">주석은 두 개의 슬래시 ()로 시작 `//` 하 고 줄의 끝까지 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-151">Comments begin with two forward slashes, `//`, and continue until the end of line.</span></span>
<span data-ttu-id="f68a2-152">설명은 Q # 소스 파일의 어디에 나 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-152">A comment may appear anywhere in a Q# source file.</span></span>

## <a name="documentation-comments"></a><span data-ttu-id="f68a2-153">설명서 주석</span><span class="sxs-lookup"><span data-stu-id="f68a2-153">Documentation Comments</span></span>

<span data-ttu-id="f68a2-154">세 개의 슬래시 ()로 시작 하는 주석은 `///` 네임 스페이스, 작업, 특수화, 함수 또는 형식 정의 바로 앞에 표시 될 때 컴파일러에서 특수 하 게 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-154">Comments that begin with three forward slashes, `///`, are treated specially by the compiler when they appear immediately before a namespace, operation, specialization, function, or type definition.</span></span>
<span data-ttu-id="f68a2-155">이 경우 다른 .NET 언어의 경우와 같이 정의 된 호출 가능 또는 사용자 정의 형식에 대 한 설명서로 해당 내용이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-155">In that case, their contents are taken as documentation for the defined callable or user-defined type, as for other .NET languages.</span></span>

<span data-ttu-id="f68a2-156">주석 내에서 `///` API 설명서의 일부로 표시 되는 텍스트는 [Markdown](https://daringfireball.net/projects/markdown/syntax)로 형식이 지정 되 고 설명서의 다른 부분은 특수 하 게 명명 된 헤더로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-156">Within `///` comments, text to appear as a part of API documentation is formatted as [Markdown](https://daringfireball.net/projects/markdown/syntax), with different parts of the documentation being indicated by specially-named headers.</span></span>
<span data-ttu-id="f68a2-157">Markdown에 대 한 확장으로, Q #의 작업, 함수 및 사용자 정의 형식에 대 한 상호 참조는를 사용 하 여 포함할 수 있습니다 `@"<ref target>"` `<ref target>` . 여기서는 참조 되는 코드 개체의 정규화 된 이름으로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-157">As an extension to Markdown, cross references to operations, functions and user-defined types in Q# can be included using the `@"<ref target>"`, where `<ref target>` is replaced by the fully qualified name of the code object being referenced.</span></span>
<span data-ttu-id="f68a2-158">선택적으로 설명서 엔진에서 추가 Markdown 확장을 지원할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-158">Optionally, a documentation engine may also support additional Markdown extensions.</span></span>

<span data-ttu-id="f68a2-159">예들 들어 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-159">For example:</span></span>

```qsharp
/// # Summary
/// Given an operation and a target for that operation,
/// applies the given operation twice.
///
/// # Input
/// ## op
/// The operation to be applied.
/// ## target
/// The target to which the operation is to be applied.
///
/// # Type Parameters
/// ## 'T
/// The type expected by the given operation as its input.
///
/// # Example
/// ```Q#
/// // Should be equivalent to the identity.
/// ApplyTwice(H, qubit);
/// ```
///
/// # See Also
/// - Microsoft.Quantum.Intrinsic.H
operation ApplyTwice<'T>(op : ('T => Unit), target : 'T) : Unit {
    op(target);
    op(target);
}
```

<span data-ttu-id="f68a2-160">다음 이름은 문서 주석 헤더로 인식 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-160">The following names are recognized as documentation comment headers.</span></span>

- <span data-ttu-id="f68a2-161">**요약**: 함수 또는 작업의 동작에 대 한 간략 한 요약 또는 형식의 용도입니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-161">**Summary**: A short summary of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="f68a2-162">요약의 첫 번째 단락은 가리키기 정보에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-162">The first paragraph of the summary is used for hover information.</span></span> <span data-ttu-id="f68a2-163">일반 텍스트 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-163">It should be plain text.</span></span>
- <span data-ttu-id="f68a2-164">**설명**: 함수 또는 작업의 동작에 대 한 설명 또는 형식의 용도에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-164">**Description**: A description of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="f68a2-165">요약 및 설명은 함수, 작업 또는 형식에 대해 생성 된 설명서 파일을 구성 하기 위해 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-165">The summary and description are concatenated to form the generated documentation file for the function, operation, or type.</span></span>
  <span data-ttu-id="f68a2-166">설명에는 인라인 LaTeX 형식의 기호 및 수식이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-166">The description may contain in-line LaTeX-formatted symbols and equations.</span></span>
- <span data-ttu-id="f68a2-167">**Input**: 작업 또는 함수에 대 한 입력 튜플의 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-167">**Input**: A description of the input tuple for an operation or function.</span></span>
  <span data-ttu-id="f68a2-168">입력 튜플의 각 개별 요소를 나타내는 추가 Markdown 하위 섹션이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-168">May contain additional Markdown subsections indicating each individual element of the input tuple.</span></span>
- <span data-ttu-id="f68a2-169">**Output**: 작업 또는 함수에서 반환 된 튜플에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-169">**Output**: A description of the tuple returned by an operation or function.</span></span>
- <span data-ttu-id="f68a2-170">**형식 매개 변수**: 각 제네릭 형식 매개 변수에 대 한 추가 하위 섹션을 하나씩 포함 하는 빈 섹션입니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-170">**Type Parameters**: An empty section which contains one additional subsection for each generic type parameter.</span></span>
- <span data-ttu-id="f68a2-171">**예**: 사용 중인 작업, 함수 또는 형식에 대 한 간단한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-171">**Example**: A short example of the operation, function or type in use.</span></span>
- <span data-ttu-id="f68a2-172">**주의**: 작업, 함수 또는 형식에 대 한 몇 가지 측면을 설명 하는 기타 prose.</span><span class="sxs-lookup"><span data-stu-id="f68a2-172">**Remarks**: Miscellaneous prose describing some aspect of the operation, function, or type.</span></span>
- <span data-ttu-id="f68a2-173">**참고**항목: 관련 된 함수, 작업 또는 사용자 정의 형식을 나타내는 정규화 된 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-173">**See Also**: A list of fully qualified names indicating related functions, operations, or user-defined types.</span></span>
- <span data-ttu-id="f68a2-174">**참조**: 문서화 되는 항목에 대 한 참조 및 인용의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-174">**References**: A list of references and citations for the item being documented.</span></span>

## <a name="whats-next"></a><span data-ttu-id="f68a2-175">다음 단계</span><span class="sxs-lookup"><span data-stu-id="f68a2-175">What's Next?</span></span>
<span data-ttu-id="f68a2-176">Q #의 [작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions) 에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="f68a2-176">Learn about [Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions) in Q#.</span></span>