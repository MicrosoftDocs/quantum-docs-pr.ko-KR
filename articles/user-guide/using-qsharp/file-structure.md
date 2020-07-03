---
title: 'Q # 파일 구조'
description: 'Q # 파일의 구조 및 구문에 대해 설명 합니다.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
ms.openlocfilehash: 54efc2b9d6b7f1956cdf9a335c88620b29f7729d
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2020
ms.locfileid: "85884174"
---
# <a name="q-file-structure"></a><span data-ttu-id="b1314-103">Q # 파일 구조</span><span class="sxs-lookup"><span data-stu-id="b1314-103">Q# File Structure</span></span>

<span data-ttu-id="b1314-104">Q # 파일은 *네임 스페이스 선언*시퀀스로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-104">A Q# file consists of a sequence of *namespace declarations*.</span></span>
<span data-ttu-id="b1314-105">각 네임 스페이스 선언에는 사용자 정의 형식, 작업 및 함수에 대 한 선언이 포함 되며, 각 선언 형식 및 순서에 관계 없이 임의 개수의 형식을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-105">Each namespace declaration contains declarations for user-defined types, operations, and functions, and can contain any number of each type of declaration and in any order.</span></span>
<span data-ttu-id="b1314-106">네임 스페이스의 선언에 대 한 자세한 내용은 [사용자 정의 형식](xref:microsoft.quantum.guide.types#user-defined-types), [작업](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)및 [함수](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b1314-106">For more information on declarations within a namespace, see [user-defined types](xref:microsoft.quantum.guide.types#user-defined-types), [operations](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations), and [functions](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions).</span></span>

<span data-ttu-id="b1314-107">네임 스페이스 선언 외부에 나타날 수 있는 유일한 텍스트는 주석입니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-107">The only text that can appear outside of a namespace declaration is comments.</span></span>
<span data-ttu-id="b1314-108">특히 네임 스페이스에 대 한 문서 주석은 선언 앞에 나옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-108">In particular, documentation comments for a namespace precede the declaration.</span></span> <span data-ttu-id="b1314-109">자세한 내용은이 문서의 [문서 주석](#documentation-comments) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b1314-109">For more information, see [Documentation comments](#documentation-comments) in this article.</span></span> 

## <a name="namespace-declarations"></a><span data-ttu-id="b1314-110">네임스페이스 선언</span><span class="sxs-lookup"><span data-stu-id="b1314-110">Namespace Declarations</span></span>

<span data-ttu-id="b1314-111">Q # 파일에는 일반적으로 네임 스페이스 선언이 하나만 포함 될 수 있지만, 빈 상태로 있거나 주석을 포함 하거나, 여러 네임 스페이스를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-111">A Q# file typically has just one namespace declaration, but could have none (and be empty or just contain comments) or could contain multiple namespaces.</span></span>
<span data-ttu-id="b1314-112">네임 스페이스 선언은 중첩할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-112">Namespace declarations can not be nested.</span></span>

<span data-ttu-id="b1314-113">동일한 이름을 가진 형식, 작업 또는 함수 선언이 없으면 함께 컴파일되는 여러 Q # 파일에서 동일한 네임 스페이스를 선언할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-113">You can declare the same namespace in multiple Q# files that are compiled together, as long as there are no type, operation, or function declarations with the same name.</span></span>
<span data-ttu-id="b1314-114">특히 선언이 동일한 경우에도 여러 파일에서 동일한 네임 스페이스에 동일한 형식을 정의 하는 것은 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-114">In particular, it is invalid to define the same type in the same namespace in multiple files, even if the declarations are identical.</span></span>

<span data-ttu-id="b1314-115">네임 스페이스 선언은 키워드로 구성 된 `namespace` 다음 네임 스페이스의 이름 및 중괄호로 묶인 네임 스페이스에 포함 된 선언으로 구성 됩니다 `{ }` .</span><span class="sxs-lookup"><span data-stu-id="b1314-115">A namespace declaration consists of the keyword `namespace`, followed by the name of the namespace, and the declarations contained in the namespace enclosed in braces `{ }`.</span></span>
<span data-ttu-id="b1314-116">네임 스페이스 이름은 마침표로 구분 된 하나 이상의 법적 기호의 시퀀스에 대 한 .NET 패턴을 따릅니다 `.` .</span><span class="sxs-lookup"><span data-stu-id="b1314-116">Namespace names follow the .NET pattern of a sequence of one or more legal symbols separated by periods `.`.</span></span>
<span data-ttu-id="b1314-117">예를 들어 `MyQuantumStuff` 및 `Microsoft.Quantum.Intrinsic` 는 유효한 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-117">For example, `MyQuantumStuff` and `Microsoft.Quantum.Intrinsic` are valid namespace names.</span></span>
<span data-ttu-id="b1314-118">규칙에 따라 네임 스페이스 이름에서 기호를 대문자로 표기 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-118">By convention, capitalize the symbols in a namespace name, however, this is not required.</span></span>

<span data-ttu-id="b1314-119">파일에서 나중에 선언 된 형식 또는 callables에 대 한 참조가 제대로 확인 됩니다. 형식, 작업 또는 함수 선언이 참조 앞에 오지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-119">References to types or callables declared further down in a file resolve properly; there is no need for the type, operation, or function declaration to precede a reference to it.</span></span>

## <a name="open-directives"></a><span data-ttu-id="b1314-120">지시문 열기</span><span class="sxs-lookup"><span data-stu-id="b1314-120">Open Directives</span></span>

<span data-ttu-id="b1314-121">네임 스페이스 블록 내에서 지시문을 사용 `open` 하 여 특정 네임 스페이스에서 선언 된 모든 형식 및 callables을 가져오고 정규화 되지 않은 이름으로 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-121">Within a namespace block, use the `open` directive to import all types and callables declared in a certain namespace and refer to them by their unqualified name.</span></span>
<span data-ttu-id="b1314-122">이러한 `open` 지시문은 키워드로 구성 된 `open` 다음 열 네임 스페이스와 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-122">Such an `open` directive consists of the `open` keyword, followed by the namespace to be opened and a terminating semicolon.</span></span>

> [!NOTE] 
> <span data-ttu-id="b1314-123">모든 `open` 지시문은 `function` `operation` `newtype` 네임 스페이스 블록의, 또는 선언 앞에 나와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-123">All `open` directives must appear before any `function`, `operation`, or `newtype` declarations in the namespace block.</span></span>

<span data-ttu-id="b1314-124">필요에 따라 열린 네임 스페이스의 짧은 이름을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-124">Optionally, you can define a short name for the opened namespace.</span></span> <span data-ttu-id="b1314-125">약식 이름이 정의 된 경우 해당 네임 스페이스의 모든 요소를 정의 된 짧은 이름으로 정규화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-125">If a short name is defined, you must qualify all elements from that namespace by the defined short name.</span></span> <span data-ttu-id="b1314-126">예를 들어 다음과 같은 네임 스페이스 선언 및 open 지시문이 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-126">For example, given the following namespace declaration and open directives,</span></span>

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

<span data-ttu-id="b1314-127">선언 된 작업에서의 작업을 사용 하는 경우 `Op` `Microsoft.Quantum.Intrinsic` 만 사용 하 여 호출 `Op` 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-127">if a declared operation uses an operation `Op` from `Microsoft.Quantum.Intrinsic`, you call it by simply using `Op`.</span></span>
<span data-ttu-id="b1314-128">그러나에서 특정 함수를 호출 하려면 `Fn` 를 `Microsoft.Quantum.Math` 사용 하 여 호출 해야 합니다 `Math.Fn` .</span><span class="sxs-lookup"><span data-stu-id="b1314-128">However, to call a certain function `Fn` from `Microsoft.Quantum.Math`, you must call it using `Math.Fn`.</span></span>

<span data-ttu-id="b1314-129">`open`지시문은 파일 내의 전체 네임 스페이스 블록에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-129">The `open` directive applies to the entire namespace block within a file.</span></span>
<span data-ttu-id="b1314-130">따라서 앞에서와 같은 Q # 파일에 추가 네임 스페이스를 정의 하는 경우, `NS` 두 번째 네임 스페이스에 정의 된 모든 작업/함수/형식은 `Microsoft.Quantum.Intrinsic` 열린 지시문을 반복 하지 않는 한 또는의 모든 항목에 액세스할 수 없습니다 `Microsoft.Quantum.Math` .</span><span class="sxs-lookup"><span data-stu-id="b1314-130">Hence, if you define an additional namespace in the same Q# file as `NS` earlier, then any operations/functions/types defined in the second namespace would not have access to anything from `Microsoft.Quantum.Intrinsic` or `Microsoft.Quantum.Math` unless you repeated the open directives therein.</span></span> 

<span data-ttu-id="b1314-131">현재 네임 스페이스 *에서 열리지 않는* 다른 네임 스페이스에 정의 된 형식 또는 호출 가능를 참조 하려면 정규화 된 이름으로 참조 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-131">To reference a type or callable defined in another namespace that is *not* opened in the current namespace, you must reference it by its fully-qualified name.</span></span>
<span data-ttu-id="b1314-132">예를 들어 `Op` 네임 스페이스에서 라는 작업이 지정 된 경우 `X.Y` :</span><span class="sxs-lookup"><span data-stu-id="b1314-132">For example, given an operation named `Op` from the `X.Y` namespace:</span></span>

* <span data-ttu-id="b1314-133">`X.Y.Op` `X.Y` 네임 스페이스가 현재 블록에서 이전에 열리지 않는 한 정규화 된 이름으로 참조 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-133">You must reference it by its fully-qualified name `X.Y.Op`, unless the `X.Y` namespace has been opened earlier in the current block.</span></span> 
* <span data-ttu-id="b1314-134">네임 스페이스를 열 때에도 `X` 작업을로 참조할 수 없습니다 `Y.Op` .</span><span class="sxs-lookup"><span data-stu-id="b1314-134">Even if the `X` namespace is opened, it is not possible to reference the operation as `Y.Op`.</span></span>
* <span data-ttu-id="b1314-135">`Z`해당 네임 스페이스 및 파일에서에 대 한 약식 이름을 정의한 경우를 `X.Y` 로 참조 해야 합니다 `Op` `Z.Op` .</span><span class="sxs-lookup"><span data-stu-id="b1314-135">If you defined the short name `Z` for `X.Y` in that namespace and file, you must reference `Op` as `Z.Op`.</span></span> 

<span data-ttu-id="b1314-136">일반적으로 지시문을 사용 하 여 네임 스페이스를 포함 하는 것이 좋습니다 `open` .</span><span class="sxs-lookup"><span data-stu-id="b1314-136">It is usually better to include a namespace by using an `open` directive.</span></span>
<span data-ttu-id="b1314-137">두 네임 스페이스가 같은 이름을 사용 하 여 구문을 정의 하 고 현재 소스가 양쪽에서 구문을 사용 하는 경우 정규화 된 이름을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-137">Using a fully-qualified name is required if two namespaces define constructs with the same name, and the current source uses constructs from both.</span></span>

<span data-ttu-id="b1314-138">Q #은 다른 .NET 언어로 이름을 지정 하는 것과 동일한 규칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-138">Q# follows the same rules for naming as other .NET languages.</span></span>
<span data-ttu-id="b1314-139">그러나 Q #에서는 네임 스페이스에 대 한 상대 참조를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-139">However, Q# does not support relative references to namespaces.</span></span>
<span data-ttu-id="b1314-140">예를 들어 네임 스페이스가 `a.b` 열려 있으면 이라는 작업에 대 한 참조는 `c.d` 전체 이름이 있는 작업으로 확인 *되지* 않습니다 `a.b.c.d` .</span><span class="sxs-lookup"><span data-stu-id="b1314-140">For example, if the namespace `a.b` is open, a reference to an operation named `c.d` does *not* resolve to an operation with full name `a.b.c.d`.</span></span>

## <a name="formatting"></a><span data-ttu-id="b1314-141">서식</span><span class="sxs-lookup"><span data-stu-id="b1314-141">Formatting</span></span>

<span data-ttu-id="b1314-142">대부분의 Q # 문과 지시문은 종료 세미콜론 ()으로 끝납니다 `;` .</span><span class="sxs-lookup"><span data-stu-id="b1314-142">Most Q# statements and directives end with a terminating semicolon, `;`.</span></span>
<span data-ttu-id="b1314-143">문 및 선언 (예 `for` : `operation` 다음 섹션 참조)으로 끝나는 문과 선언에는 종료 세미콜론이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-143">Statements and declarations such as `for` and `operation` that end with a statement block (see the following section) do not require a terminating semicolon.</span></span>
<span data-ttu-id="b1314-144">각 문 설명에는 종료 세미콜론이 필요한 지 여부에 대 한 설명이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-144">Each statement description notes whether the terminating semicolon is required.</span></span>

<span data-ttu-id="b1314-145">식, 선언 및 지시문과 같은 문을 여러 줄로 나눌 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-145">Statements, like expressions, declarations, and directives, can be broken out across multiple lines.</span></span>
<span data-ttu-id="b1314-146">여러 문을 한 줄에 배치 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="b1314-146">Avoid putting multiple statements on a single line.</span></span>

## <a name="statement-blocks"></a><span data-ttu-id="b1314-147">문 블록</span><span class="sxs-lookup"><span data-stu-id="b1314-147">Statement Blocks</span></span>

<span data-ttu-id="b1314-148">Q # 문은 중괄호에 포함 된 문 블록으로 그룹화 됩니다 `{ }` .</span><span class="sxs-lookup"><span data-stu-id="b1314-148">Q# statements are grouped into statement blocks, which are contained with braces `{ }`.</span></span> <span data-ttu-id="b1314-149">문 블록은 여는 것으로 시작 하 `{` 고 닫는로 끝납니다 `}` .</span><span class="sxs-lookup"><span data-stu-id="b1314-149">A statement block starts with an opening `{` and ends with a closing `}`.</span></span>

<span data-ttu-id="b1314-150">다른 블록 내에 어휘를 싸인 문 블록은 포함 하는 블록의 하위 블록으로 간주 됩니다. 포함 및 하위 블록은 외부 및 내부 블록이 라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-150">A statement block that is lexically enclosed within another block is considered to be a sub-block of the containing block; containing and sub-blocks are also called outer and inner blocks.</span></span>

## <a name="comments"></a><span data-ttu-id="b1314-151">의견</span><span class="sxs-lookup"><span data-stu-id="b1314-151">Comments</span></span>

<span data-ttu-id="b1314-152">주석은 두 개의 슬래시 ()로 시작 `//` 하 고 줄의 끝까지 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-152">Comments begin with two forward slashes, `//`, and continue until the end of the line.</span></span>
<span data-ttu-id="b1314-153">설명은 Q # 소스 파일의 어디에 나 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-153">A comment can appear anywhere in a Q# source file.</span></span>

## <a name="documentation-comments"></a><span data-ttu-id="b1314-154">설명서 주석</span><span class="sxs-lookup"><span data-stu-id="b1314-154">Documentation Comments</span></span>

<span data-ttu-id="b1314-155">세 개의 슬래시 ()로 시작 하는 주석은 `///` 네임 스페이스, 작업, 특수화, 함수 또는 형식 정의 바로 앞에 표시 될 때 컴파일러에서 특수 하 게 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-155">Comments that begin with three forward slashes, `///`, are treated specially by the compiler when they appear immediately before a namespace, operation, specialization, function, or type definition.</span></span>
<span data-ttu-id="b1314-156">이 경우 컴파일러는 다른 .NET 언어와 동일한 정의 된 호출 가능 또는 사용자 정의 형식에 대 한 설명서로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-156">In that case, the compiler treats them as documentation for the defined callable or user-defined type, the same as other .NET languages.</span></span>

<span data-ttu-id="b1314-157">주석 내에서 `///` API 설명서의 일부로 표시 되는 텍스트는 특수 하 게 명명 된 헤더로 표시 되는 설명서의 여러 부분을 사용 하 여 [Markdown](https://daringfireball.net/projects/markdown/syntax)로 형식이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-157">Within `///` comments, text to appear as a part of API documentation is formatted as [Markdown](https://daringfireball.net/projects/markdown/syntax), with different parts of the documentation indicated by specially-named headers.</span></span>
<span data-ttu-id="b1314-158">Markdown에서는 `@"<ref target>"` Q #에서 확장을 사용 하 여 상호 참조 작업, 함수 및 사용자 정의 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-158">In Markdown, use the `@"<ref target>"` extension to cross-reference operations, functions, and user-defined types in Q#.</span></span> <span data-ttu-id="b1314-159">`<ref target>`참조 된 코드 개체의 정규화 된 이름으로 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-159">Replace `<ref target>` with the fully qualified name of the referenced code object.</span></span>
<span data-ttu-id="b1314-160">다른 설명서 엔진은 추가 Markdown 확장을 지원할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-160">Different documentation engines may also support additional Markdown extensions.</span></span>

<span data-ttu-id="b1314-161">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-161">For example:</span></span>

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

<span data-ttu-id="b1314-162">다음 이름은 문서 주석 헤더로 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-162">The following names are valid as documentation comment headers.</span></span>

- <span data-ttu-id="b1314-163">**요약**: 함수 또는 작업의 동작에 대 한 간단한 요약 또는 형식의 용도입니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-163">**Summary**: A short summary of the behavior of a function or operation, or the purpose of a type.</span></span> <span data-ttu-id="b1314-164">요약의 첫 번째 단락은 가리키기 정보에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-164">The first paragraph of the summary is used for hover information.</span></span> <span data-ttu-id="b1314-165">일반 텍스트 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-165">It should be plain text.</span></span>
- <span data-ttu-id="b1314-166">**설명**: 함수 또는 작업의 동작에 대 한 설명 또는 형식의 용도입니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-166">**Description**: A description of the behavior of a function or operation, or the purpose of a type.</span></span> <span data-ttu-id="b1314-167">요약 및 설명은 함께 함수, 작업 또는 형식에 대해 생성 된 설명서 파일을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-167">Together, the summary and description form the generated documentation file for the function, operation, or type.</span></span>
  <span data-ttu-id="b1314-168">이 설명에서는 인라인 LaTeX 형식의 기호 및 수식을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-168">The description supports in-line LaTeX-formatted symbols and equations.</span></span>
- <span data-ttu-id="b1314-169">**Input**: 작업 또는 함수에 대 한 입력 튜플의 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-169">**Input**: A description of the input tuple for an operation or function.</span></span>
  <span data-ttu-id="b1314-170">입력 튜플의 각 요소를 나타내는 추가 Markdown 하위 섹션을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-170">Can contain additional Markdown subsections indicating each element of the input tuple.</span></span>
- <span data-ttu-id="b1314-171">**Output**: 작업 또는 함수에서 반환 된 튜플에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-171">**Output**: A description of the tuple returned by an operation or function.</span></span>
- <span data-ttu-id="b1314-172">**형식 매개 변수**: 각 제네릭 형식 매개 변수에 대해 하나의 추가 하위 섹션을 포함 하는 빈 섹션입니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-172">**Type Parameters**: An empty section that contains one additional subsection for each generic type parameter.</span></span>
- <span data-ttu-id="b1314-173">**예**: 사용 중인 작업, 함수 또는 형식의 간단한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-173">**Example**: A short example of the operation, function, or type in use.</span></span>
- <span data-ttu-id="b1314-174">**주의**: 작업, 함수 또는 형식에 대 한 몇 가지 측면을 설명 하는 기타 prose.</span><span class="sxs-lookup"><span data-stu-id="b1314-174">**Remarks**: Miscellaneous prose describing some aspect of the operation, function, or type.</span></span>
- <span data-ttu-id="b1314-175">**참고**항목: 관련 된 함수, 작업 또는 사용자 정의 형식을 나타내는 정규화 된 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-175">**See Also**: A list of fully qualified names indicating related functions, operations, or user-defined types.</span></span>
- <span data-ttu-id="b1314-176">**참조**: 문서화 된 항목에 대 한 참조 및 인용의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-176">**References**: A list of references and citations for the documented item.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b1314-177">다음 단계</span><span class="sxs-lookup"><span data-stu-id="b1314-177">Next steps</span></span>

<span data-ttu-id="b1314-178">Q #의 [작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions) 에 대해 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="b1314-178">Learn about [Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions) in Q#.</span></span>