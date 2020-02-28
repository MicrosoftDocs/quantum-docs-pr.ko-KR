---
title: 'Q # 문'
description: '함수 및 작업 선언, 변수 선언 및 할당, 작업 호출을 포함 하 여 Q #에서 문의 올바른 사용에 대해 알아봅니다.'
author: QuantumWriter
uid: microsoft.quantum.language.statements
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: e801a5fdd24b973f47d23d2aca6f11bbebf333d4
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904675"
---
# <a name="statements-and-other-constructs"></a><span data-ttu-id="1372f-103">문 및 기타 구문</span><span class="sxs-lookup"><span data-stu-id="1372f-103">Statements and Other Constructs</span></span>

## <a name="comments"></a><span data-ttu-id="1372f-104">주석</span><span class="sxs-lookup"><span data-stu-id="1372f-104">Comments</span></span>

<span data-ttu-id="1372f-105">주석은 두 개의 슬래시, `//`로 시작 하 고 줄의 끝까지 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-105">Comments begin with two forward slashes, `//`, and continue until the end of line.</span></span>
<span data-ttu-id="1372f-106">설명은 Q # 소스 파일의 어디에 나 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-106">A comment may appear anywhere in a Q# source file.</span></span>

### <a name="documentation-comments"></a><span data-ttu-id="1372f-107">문서 주석</span><span class="sxs-lookup"><span data-stu-id="1372f-107">Documentation Comments</span></span>

<span data-ttu-id="1372f-108">세 개의 슬래시 (`///`)로 시작 하는 주석은 네임 스페이스, 작업, 특수화, 함수 또는 형식 정의 바로 앞에 표시 될 때 컴파일러에서 특수 하 게 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-108">Comments that begin with three forward slashes, `///`, are treated specially by the compiler when they appear immediately before a namespace, operation, specialization, function, or type definition.</span></span>
<span data-ttu-id="1372f-109">이 경우 다른 .NET 언어의 경우와 같이 정의 된 호출 가능 또는 사용자 정의 형식에 대 한 설명서로 해당 내용이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-109">In that case, their contents are taken as documentation for the defined callable or user-defined type, as for other .NET languages.</span></span>

<span data-ttu-id="1372f-110">`///` 주석 내에서 API 설명서의 일부로 표시 되는 텍스트는 특수 하 게 명명 된 헤더로 표시 되는 설명서의 여러 부분을 사용 하 여 [Markdown](https://daringfireball.net/projects/markdown/syntax)로 형식이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-110">Within `///` comments, text to appear as a part of API documentation is formatted as [Markdown](https://daringfireball.net/projects/markdown/syntax), with different parts of the documentation being indicated by specially-named headers.</span></span>
<span data-ttu-id="1372f-111">Markdown에 대 한 확장으로, Q #의 작업, 함수 및 사용자 정의 형식에 대 한 상호 참조는 참조 되는 코드 개체의 정규화 된 이름으로 대체 되는 `@"<ref target>"``<ref target>`을 사용 하 여 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-111">As an extension to Markdown, cross references to operations, functions and user-defined types in Q# can be included using the `@"<ref target>"`, where `<ref target>` is replaced by the fully qualified name of the code object being referenced.</span></span>
<span data-ttu-id="1372f-112">선택적으로 설명서 엔진에서 추가 Markdown 확장을 지원할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-112">Optionally, a documentation engine may also support additional Markdown extensions.</span></span>

<span data-ttu-id="1372f-113">다음은 그 예입니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-113">For example:</span></span>

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

<span data-ttu-id="1372f-114">다음 이름은 문서 주석 헤더로 인식 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-114">The following names are recognized as documentation comment headers.</span></span>

- <span data-ttu-id="1372f-115">**요약**: 함수 또는 작업의 동작에 대 한 간략 한 요약 또는 형식의 용도입니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-115">**Summary**: A short summary of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="1372f-116">요약의 첫 번째 단락은 가리키기 정보에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-116">The first paragraph of the summary is used for hover information.</span></span> <span data-ttu-id="1372f-117">일반 텍스트 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-117">It should be plain text.</span></span>
- <span data-ttu-id="1372f-118">**설명**: 함수 또는 작업의 동작에 대 한 설명 또는 형식의 용도에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-118">**Description**: A description of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="1372f-119">요약 및 설명은 함수, 작업 또는 형식에 대해 생성 된 설명서 파일을 구성 하기 위해 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-119">The summary and description are concatenated to form the generated documentation file for the function, operation, or type.</span></span>
  <span data-ttu-id="1372f-120">설명에는 인라인 LaTeX 형식의 기호 및 수식이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-120">The description may contain in-line LaTeX-formatted symbols and equations.</span></span>
- <span data-ttu-id="1372f-121">**Input**: 작업 또는 함수에 대 한 입력 튜플의 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-121">**Input**: A description of the input tuple for an operation or function.</span></span>
  <span data-ttu-id="1372f-122">입력 튜플의 각 개별 요소를 나타내는 추가 Markdown 하위 섹션이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-122">May contain additional Markdown subsections indicating each individual element of the input tuple.</span></span>
- <span data-ttu-id="1372f-123">**Output**: 작업 또는 함수에서 반환 된 튜플에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-123">**Output**: A description of the tuple returned by an operation or function.</span></span>
- <span data-ttu-id="1372f-124">**형식 매개 변수**: 각 제네릭 형식 매개 변수에 대 한 추가 하위 섹션을 하나씩 포함 하는 빈 섹션입니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-124">**Type Parameters**: An empty section which contains one additional subsection for each generic type parameter.</span></span>
- <span data-ttu-id="1372f-125">**예**: 사용 중인 작업, 함수 또는 형식에 대 한 간단한 예입니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-125">**Example**: A short example of the operation, function or type in use.</span></span>
- <span data-ttu-id="1372f-126">**주의**: 작업, 함수 또는 형식에 대 한 몇 가지 측면을 설명 하는 기타 prose.</span><span class="sxs-lookup"><span data-stu-id="1372f-126">**Remarks**: Miscellaneous prose describing some aspect of the operation, function, or type.</span></span>
- <span data-ttu-id="1372f-127">**참고**항목: 관련 된 함수, 작업 또는 사용자 정의 형식을 나타내는 정규화 된 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-127">**See Also**: A list of fully qualified names indicating related functions, operations, or user-defined types.</span></span>
- <span data-ttu-id="1372f-128">**참조**: 문서화 되는 항목에 대 한 참조 및 인용의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-128">**References**: A list of references and citations for the item being documented.</span></span>

## <a name="namespaces"></a><span data-ttu-id="1372f-129">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="1372f-129">Namespaces</span></span>

<span data-ttu-id="1372f-130">모든 Q # 작업, 함수 및 사용자 정의 형식은 네임 스페이스 내에서 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-130">Every Q# operation, function, and user-defined type is defined within a namespace.</span></span>
<span data-ttu-id="1372f-131">Q #은 다른 .NET 언어로 이름을 지정 하는 것과 동일한 규칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-131">Q# follows the same rules for naming as other .NET languages.</span></span>
<span data-ttu-id="1372f-132">그러나 Q #에서는 네임 스페이스에 대 한 상대 참조를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-132">However, Q# does not support relative references to namespaces.</span></span>
<span data-ttu-id="1372f-133">즉, `a.b` 네임 스페이스를 연 경우 `c.d` 작업 이름에 대 한 참조는 전체 이름이 `a.b.c.d`된 작업으로 확인 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-133">That is, if the namespace `a.b` has been opened, a reference to an operation names `c.d` will not be resolved to an operation with full name `a.b.c.d`.</span></span>

<span data-ttu-id="1372f-134">네임 스페이스 블록 내에서 `open` 지시어를 사용 하 여 특정 네임 스페이스에서 선언 된 모든 형식 및 callables을 가져와서 정규화 되지 않은 이름으로 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-134">Within a namespace block, the `open` directive may be used to import all types and callables declared in a certain namespace and refer to them by their unqualified name.</span></span> <span data-ttu-id="1372f-135">필요에 따라 열린 네임 스페이스의 짧은 이름을 정의 하 여 해당 네임 스페이스의 모든 요소를 정의 된 약식 이름으로 정규화 하 고 필요에 따라 정규화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-135">Optionally, a short name for the opened namespace may be defined such that all elements from that namespace can (and need) to be qualified by the defined short name.</span></span> <span data-ttu-id="1372f-136">`open` 지시문은 파일 내의 전체 네임 스페이스 블록에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-136">The `open` directive applies to the entire namespace block within a file.</span></span>

<span data-ttu-id="1372f-137">현재 네임 스페이스에서 열려 있지 않은 다른 네임 스페이스에 정의 된 형식 또는 호출 가능 이름은 정규화 된 이름으로 참조 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-137">A type or callable defined in another namespace that is not opened in the current namespace must be referenced by its fully-qualified name.</span></span>
<span data-ttu-id="1372f-138">예를 들어 `X.Y` 네임 스페이스가 현재 블록에서 아직 열려 있지 않은 경우 `X.Y` 네임 스페이스에 `Op` 이름이 지정 된 작업은 정규화 된 이름 `X.Y.Op`에서 참조 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-138">For example, an operation named `Op` in the `X.Y` namespace must be referenced by its fully-qualified name `X.Y.Op`, unless the `X.Y` namespace has been opened earlier in the current block.</span></span> <span data-ttu-id="1372f-139">위에서 언급 한 대로 `X` 네임 스페이스를 연 경우에도 `Y.Op`작업을 참조할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-139">As mentioned above, even if the `X` namespace has been opened, it is not possible to reference the operation as `Y.Op`.</span></span>
<span data-ttu-id="1372f-140">`X.Y`의 약식 `Z` 이름이 해당 네임 스페이스 및 파일에 정의 된 경우 `Op`를 `Z.Op`로 참조 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-140">If a short name `Z` for `X.Y` has been defined in that namespace and file, then `Op` needs to be referred to as `Z.Op`.</span></span> 

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace
}
```

<span data-ttu-id="1372f-141">일반적으로 `open` 지시어를 사용 하 여 네임 스페이스를 포함 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-141">It is usually better to include a namespace by using an `open` directive.</span></span>
<span data-ttu-id="1372f-142">두 네임 스페이스가 같은 이름을 사용 하 여 구문을 정의 하 고 현재 소스가 양쪽에서 구문을 사용 하는 경우 정규화 된 이름을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-142">Using a fully-qualified name is required if two namespaces define constructs with the same name, and the current source uses constructs from both.</span></span>

## <a name="formatting"></a><span data-ttu-id="1372f-143">서식 지정</span><span class="sxs-lookup"><span data-stu-id="1372f-143">Formatting</span></span>

<span data-ttu-id="1372f-144">대부분의 Q # 문과 지시문은 종료 세미콜론 (`;`)으로 끝납니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-144">Most Q# statements and directives end with a terminating semicolon, `;`.</span></span>
<span data-ttu-id="1372f-145">문 및 선언 (예: 문 블록으로 끝나는 `for` 및 `operation`)에는 종료 세미콜론이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-145">Statements and declarations such as `for` and `operation` that end with a statement block do not require a terminating semicolon.</span></span>
<span data-ttu-id="1372f-146">각 문 설명에는 종료 세미콜론이 필요한 지 여부에 대 한 설명이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-146">Each statement description notes whether the terminating semicolon is required.</span></span>

<span data-ttu-id="1372f-147">식, 선언 및 지시문과 같은 문은 여러 줄에 걸쳐 분할 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-147">Statements, like expressions, declarations, and directives, may be broken out across multiple lines.</span></span>
<span data-ttu-id="1372f-148">한 줄에 문이 여러 개 있는 것은 피해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-148">Having multiple statements on a single line should be avoided.</span></span>

## <a name="statement-blocks"></a><span data-ttu-id="1372f-149">문 블록</span><span class="sxs-lookup"><span data-stu-id="1372f-149">Statement Blocks</span></span>

<span data-ttu-id="1372f-150">Q # 문은 문 블록으로 그룹화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-150">Q# statements are grouped into statement blocks.</span></span>
<span data-ttu-id="1372f-151">문 블록은 여는 `{` 시작 하 고 닫는 `}`로 끝납니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-151">A statement block starts with an opening `{` and ends with a closing `}`.</span></span>

<span data-ttu-id="1372f-152">다른 블록 내에 어휘를 싸인 문 블록은 포함 하는 블록의 하위 블록으로 간주 됩니다. 포함 및 하위 블록은 외부 및 내부 블록이 라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-152">A statement block that is lexically enclosed within another block is considered to be a sub-block of the containing block; containing and sub-blocks are also called outer and inner blocks.</span></span>

## <a name="symbol-binding-and-assignment"></a><span data-ttu-id="1372f-153">기호 바인딩 및 할당</span><span class="sxs-lookup"><span data-stu-id="1372f-153">Symbol Binding and Assignment</span></span>

<span data-ttu-id="1372f-154">Q #은 변경 가능 하 고 변경할 수 없는 기호를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-154">Q# distinguishes between mutable and immutable symbols.</span></span>
<span data-ttu-id="1372f-155">일반적으로 컴파일러에서 더 많은 최적화를 수행할 수 있기 때문에 변경할 수 없는 기호를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-155">In general, the use of immutable symbols is encouraged because it allows the compiler to perform more optimizations.</span></span>

<span data-ttu-id="1372f-156">바인딩의 왼쪽은 기호 튜플 및 식의 오른쪽으로 구성 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-156">The left-hand-side of the binding consists of a symbol tuple, and the right hand side of an expression.</span></span>

<span data-ttu-id="1372f-157">모든 Q # 형식은 값 형식이 며,이 경우에는 값이 기호에 바인딩되거나 기호가 바인딩 되었을 때 "복사"가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-157">Since all Q# types are value types - with the qubits taking a somewhat special role - formally a "copy" is created when a value is bound to a symbol, or when a symbol is rebound.</span></span> <span data-ttu-id="1372f-158">즉, Q #의 동작은 할당 시 복사본이 생성 된 경우와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-158">That is to say, the behavior of Q# is the same as if a copy were created on assignment.</span></span> <span data-ttu-id="1372f-159">특히 배열도 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-159">This in particular also includes arrays.</span></span> <span data-ttu-id="1372f-160">물론 관련 된 부분만 실제로 필요에 따라 다시 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-160">Of course in practice only the relevant pieces are actually recreated as needed.</span></span> 

### <a name="tuple-deconstruction"></a><span data-ttu-id="1372f-161">튜플 분해</span><span class="sxs-lookup"><span data-stu-id="1372f-161">Tuple Deconstruction</span></span>

<span data-ttu-id="1372f-162">바인딩의 오른쪽이 튜플이 면 할당 시 해당 튜플을 분해 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-162">If the right-hand side of the binding is a tuple, then that tuple may be deconstructed upon assignment.</span></span>
<span data-ttu-id="1372f-163">이러한 분해에는 중첩 된 튜플이 포함 될 수 있으며, 모든 전체 또는 부분 분해은 오른쪽에 있는 튜플의 모양이 기호 튜플의 셰이프와 호환 되는 한 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-163">Such deconstructions may involve nested tuples, and any full or partial deconstruction is valid as long as the shape of the tuple on the right hand side is compatible with the shape of the symbol tuple.</span></span>
<span data-ttu-id="1372f-164">`=`의 오른쪽이 튜플 값 식인 경우에도 특히 튜플 분해 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-164">Tuple deconstruction can in particular also be used when the right-hand side of the `=` is a tuple-valued expression.</span></span>

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

### <a name="immutable-symbols"></a><span data-ttu-id="1372f-165">변경할 수 없는 기호</span><span class="sxs-lookup"><span data-stu-id="1372f-165">Immutable Symbols</span></span>

<span data-ttu-id="1372f-166">변경할 수 없는 기호는 `let` 문을 사용 하 여 바인딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-166">Immutable symbols are bound using the `let` statement.</span></span>
<span data-ttu-id="1372f-167">이는와 C#같은 언어의 변수 선언 및 초기화와 거의 동일 합니다. 단,이 경우는 Q # 기호가 바인딩된 후에는 변경할 수 없습니다. `let` 바인딩은 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-167">This is roughly equivalent to variable declaration and initialization in languages such as C#, except that Q# symbols, once bound, may not be changed; `let` bindings are immutable.</span></span>

<span data-ttu-id="1372f-168">변경할 수 없는 바인딩은 키워드 `let`로 구성 된 다음 기호 또는 기호 튜플, 등호 `=`, 기호를 바인딩할 식, 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-168">An immutable binding consists of the keyword `let`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>
<span data-ttu-id="1372f-169">바인딩된 기호의 형식은 오른쪽에 있는 식을 기반으로 유추 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-169">The type of the bound symbol(s) is inferred based on the expression on the right hand side.</span></span>

### <a name="mutable-symbols"></a><span data-ttu-id="1372f-170">변경 가능한 기호</span><span class="sxs-lookup"><span data-stu-id="1372f-170">Mutable Symbols</span></span>

<span data-ttu-id="1372f-171">변경 가능한 기호는 `mutable` 문을 사용 하 여 정의 및 초기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-171">Mutable symbols are defined and initialized using the `mutable` statement.</span></span>
<span data-ttu-id="1372f-172">`mutable` 문의 일부로 선언 되 고 바인딩된 기호는 코드에서 나중에 다른 값으로 다시 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-172">Symbols declared and bound as part of a `mutable` statement may be rebound to a different value later in the code.</span></span> 

<span data-ttu-id="1372f-173">변경 가능한 바인딩 문은 `mutable`키워드와 기호 또는 기호 튜플, 등호 `=`, 기호를 바인딩할 식, 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-173">A mutable binding statement consists of the keyword `mutable`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>
<span data-ttu-id="1372f-174">바인딩된 기호의 형식은 오른쪽에 있는 식을 기반으로 유추 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-174">The type of the bound symbol(s) is inferred based on the expression on the right hand side.</span></span> <span data-ttu-id="1372f-175">기호를 코드에서 나중에 다시 바인딩하는 경우 해당 형식은 변경 되지 않으며 바인딩된 값은 해당 형식과 호환 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-175">If a symbol is rebound later in the code, its type does not change, and the bound value needs to be compatible with that type.</span></span>

### <a name="rebinding-of-mutable-symbols"></a><span data-ttu-id="1372f-176">변경 가능한 기호 리바인딩</span><span class="sxs-lookup"><span data-stu-id="1372f-176">Rebinding of Mutable Symbols</span></span>

<span data-ttu-id="1372f-177">변경 가능한 변수는 `set` 문을 사용 하 여 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-177">A mutable variable may be rebound using a `set` statement.</span></span>
<span data-ttu-id="1372f-178">이러한 리바인딩은 키워드 `set`로 구성 된 다음 기호 또는 기호 튜플, 등호 `=`, 기호를에 다시 바인딩하는 식 및 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-178">Such a rebinding consists of the keyword `set`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to rebind the symbol(s) to, and a terminating semicolon.</span></span>
<span data-ttu-id="1372f-179">값은 바인딩되는 기호의 형식과 호환 되어야 합니다 (s).</span><span class="sxs-lookup"><span data-stu-id="1372f-179">The value must be compatible with the type(s) of the symbol(s) it is bound to.</span></span>

#### <a name="apply-and-reassign-statement"></a><span data-ttu-id="1372f-180">적용 및 재할당 문</span><span class="sxs-lookup"><span data-stu-id="1372f-180">Apply-and-Reassign Statement</span></span>

<span data-ttu-id="1372f-181">적용 및 재할당 문으로 참조 하는 특정 종류의 set 문은 오른쪽이 이항 연산자의 응용 프로그램으로 구성 되 고 결과가 연산자의 왼쪽 인수에 다시 바인딩 되는 경우 편리 하 게 연결 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-181">A particular kind of set-statement we refer to as an apply-and-reassign statement provides a convenient way of concatenation if the right hand side consists of the application of a binary operator and the result is to be rebound to the left argument to the operator.</span></span> <span data-ttu-id="1372f-182">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-182">For example,</span></span>
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
<span data-ttu-id="1372f-183">`for` 루프의 각 반복에서 카운터 `counter`의 값을 증가 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-183">increments the value of the counter `counter` in each iteration of the `for` loop.</span></span> <span data-ttu-id="1372f-184">위의 코드는와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-184">The code above is equivalent to</span></span> 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```
<span data-ttu-id="1372f-185">왼쪽의 형식이 식 형식과 일치 하는 모든 이항 연산자에 대해 비슷한 문을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-185">Similar statements are available for all binary operators in which the type of the left-hand-side matches the expression type.</span></span> <span data-ttu-id="1372f-186">예를 들어 다음과 같이 값을 누적 하는 편리한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-186">This provides for example a convenient way to accumulate values:</span></span>
```qsharp
mutable results = new Result[0];
for (qubit in qubits) {
    set results += [M(q)];
    // ...
}
```
#### <a name="update-and-reassign-statement"></a><span data-ttu-id="1372f-187">업데이트 및 재할당 문</span><span class="sxs-lookup"><span data-stu-id="1372f-187">Update-and-Reassign Statement</span></span>

<span data-ttu-id="1372f-188">오른쪽에 복사 및 업데이트 식에 대 한 유사한 연결이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-188">A similar concatenation exists for copy-and-update expressions on the right hand side.</span></span> <span data-ttu-id="1372f-189">마찬가지로, 사용자 정의 형식의 명명 된 항목 뿐만 아니라 배열 항목에 대해 업데이트 및 재할당 문이 존재 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-189">Correspondingly, update-and-reassign statements exist for named items in user-defined types as well as for array items.</span></span>  

```qsharp
newtype Complex = (Re : Double, Im : Double);

function ComplexSum(reals : Double[], ims : Double[]) : Complex[] {
    mutable res = Complex(0.,0.);

    for (r in reals) {
        set res w/= Re <- res::Re + r; // update-and-reassign statement
    }
    for (i in ims) {
        set res w/= Im <- res::Im + i; // update-and-reassign statement
    }
    return res;
}
```

<span data-ttu-id="1372f-190">배열의 경우 표준 라이브러리에는 여러 일반적인 배열 초기화 및 조작 요구에 필요한 도구가 포함 되어 있으므로 첫 번째 위치의 배열 항목을 업데이트 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-190">In the case of arrays, our standard libraries contain the necessary tools for many common array initialization and manipulation needs, and thus help avoid having to update array items in the first place.</span></span> <span data-ttu-id="1372f-191">필요에 따라 업데이트 및 재할당 문이 대안을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-191">Update-and-reassign statements provide an alternative if needed:</span></span>

```qsharp
operation GenerateRandomInts(max : Int, nSamples : Int) : Int[] {
    mutable samples = new Double[0];
    for (i in 1 .. nSamples) {
        set samples += [RandomInt(max)];
    }
    return samples;
}

operation SampleUniformDistrbution(nSamples : Int, nSteps : Int) : Double[] {
    let normalization = 1. / IntAsDouble(nSteps);
    mutable samples = GenerateRandomInts(nSteps, nSamples);
    
    for (i in IndexRange(samples) {
        let value = IntAsDouble(samples[i]);
        set samples w/= i <- normalization * value; // update-and-reassign statement
    }
}

```

> [!TIP]   
> <span data-ttu-id="1372f-192"><xref:microsoft.quantum.arrays>에서 제공 하는 도구를 활용 하 여 업데이트 및 재할당 문의 불필요 한 사용을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-192">Avoid unnecessary use of update-and-reassign statements by leveraging the tools provided in <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="1372f-193">함수</span><span class="sxs-lookup"><span data-stu-id="1372f-193">The function</span></span>
```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    mutable pauliArray = new Pauli[length];
    for (index in 0 .. length - 1) {
        set pauliArray w/= index <- 
            index == location ? pauli | PauliI;
    }    
    return pauliArray;
}
```
<span data-ttu-id="1372f-194">예를 들어 `Microsoft.Quantum.Arrays`에서 `ConstantArray` 함수를 사용 하 고 복사 및 업데이트 식을 반환 하는 것은 간단 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-194">for example can simply be simplified using the function `ConstantArray` in `Microsoft.Quantum.Arrays`, and returning a copy-and-update expression:</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

### <a name="binding-scopes"></a><span data-ttu-id="1372f-195">바인딩 범위</span><span class="sxs-lookup"><span data-stu-id="1372f-195">Binding Scopes</span></span>

<span data-ttu-id="1372f-196">일반적으로 기호 바인딩은 범위를 벗어난 것으로,에서 발생 하는 문 블록의 끝에서 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-196">In general, symbol bindings go out of scope and become inoperative at the end of the statement block they occur in.</span></span>
<span data-ttu-id="1372f-197">이 규칙에는 두 가지 예외가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-197">There are two exceptions to this rule:</span></span>

- <span data-ttu-id="1372f-198">`for` 루프의 루프 변수 바인딩은 for 루프 본문의 범위 내에 있지만 루프가 끝난 후에는 범위 내에 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-198">The binding of the loop variable of a `for` loop is in scope for the body of the for loop, but not after the end of the loop.</span></span>
- <span data-ttu-id="1372f-199">`repeat`/`until` 루프 (본문, 테스트 및 픽스업)의 세 부분은 모두 단일 범위로 처리 되므로 본문에 바인딩된 기호는 테스트 및 픽스업에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-199">All three portions of a `repeat`/`until` loop (the body, the test, and the fixup) are treated as a single scope, so symbols that are bound in the body are available in the test and in the fixup.</span></span>

<span data-ttu-id="1372f-200">두 가지 유형의 루프 모두 루프를 통과 하는 각은 자체 범위에서 실행 되므로 이전 패스의 바인딩은 이후 단계에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-200">For both types of loops, each pass through the loop executes in its own scope, so bindings from an earlier pass are not available in a later pass.</span></span>

<span data-ttu-id="1372f-201">외부 블록의 기호 바인딩은 내부 블록에 의해 상속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-201">Symbol bindings from outer blocks are inherited by inner blocks.</span></span>
<span data-ttu-id="1372f-202">기호는 블록 당 한 번만 바인딩할 수 있습니다. 범위 내에 있는 다른 기호와 동일한 이름을 사용 하 여 기호를 정의할 수 없습니다 ("숨김" 없음).</span><span class="sxs-lookup"><span data-stu-id="1372f-202">A symbol may only be bound once per block; it is illegal to define a symbol with the same name as another symbol that is within scope (no "shadowing").</span></span>
<span data-ttu-id="1372f-203">다음 시퀀스는 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-203">The following sequences would be legal:</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

<span data-ttu-id="1372f-204">and</span><span class="sxs-lookup"><span data-stu-id="1372f-204">and</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
} else {
    ...
    let n = 8;
    ...             // n is 8
}
```

<span data-ttu-id="1372f-205">그러나이는 올바르지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-205">But this would be illegal:</span></span>

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

<span data-ttu-id="1372f-206">다음과 같이 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-206">as would:</span></span>

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="control-flow"></a><span data-ttu-id="1372f-207">제어 흐름</span><span class="sxs-lookup"><span data-stu-id="1372f-207">Control Flow</span></span>

### <a name="for-loop"></a><span data-ttu-id="1372f-208">For 루프</span><span class="sxs-lookup"><span data-stu-id="1372f-208">For Loop</span></span>

<span data-ttu-id="1372f-209">`for` 문은 정수 범위 또는 배열에 대 한 반복을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-209">The `for` statement supports iteration over an integer range or over an array.</span></span>
<span data-ttu-id="1372f-210">문은 키워드 `for`, 여는 괄호 `(`, 기호 또는 기호 튜플, 키워드 `in`, `Range` 또는 배열 형식의 식, 닫는 괄호 `)`및 문 블록으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-210">The statement consists of the keyword `for`, an open parenthesis `(`, followed by a symbol or symbol tuple, the keyword `in`, an expression of type `Range` or array, a close parenthesis `)`, and a statement block.</span></span>

<span data-ttu-id="1372f-211">문 블록 (루프의 본문)은 범위 또는 배열의 각 값에 바인딩된 정의 된 기호 (루프 변수)를 사용 하 여 반복적으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-211">The statement block (the body of the loop) is executed repeatedly, with the defined symbol(s) (the loop variable(s)) bound to each value in the range or array.</span></span>
<span data-ttu-id="1372f-212">범위 식이 빈 범위 또는 배열로 계산 되는 경우 본문은 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-212">Note that if the range expression evaluates to an empty range or array, the body will not be executed at all.</span></span>
<span data-ttu-id="1372f-213">식은 루프를 시작 하기 전에 완전히 계산 되며 루프가 실행 되는 동안에는 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-213">The expression is fully evaluated before entering the loop, and will not change while the loop is executing.</span></span>

<span data-ttu-id="1372f-214">선언 된 기호의 바인딩은 변경할 수 없으며 다른 변수 바인딩과 동일한 규칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-214">The binding of the declared symbol(s) is immutable and follows the same rules as other variable bindings.</span></span> <span data-ttu-id="1372f-215">특히 루프 변수에 할당 될 때 배열에 대 한 반복의 배열 항목을 소멸 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-215">In particular, it is possible to destruct e.g. array items for an iteration over an array upon assignment to the loop variable(s).</span></span>

<span data-ttu-id="1372f-216">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-216">For example,</span></span>

```qsharp
// ...
for (qubit in qubits) { // qubits contains a Qubit[]
    H(qubit);
}

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {
    set results w/= index <- (index, M(qubits[index]));
}

mutable accumulated = 0;
for ((index, measured) in results) {
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```

<span data-ttu-id="1372f-217">루프 변수는 루프 본문에 대 한 각 입구에 바인딩되고 본문의 끝에서 바인딩되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-217">The loop variable is bound at each entrance to the loop body, and unbound at the end of the body.</span></span>
<span data-ttu-id="1372f-218">특히 for 루프가 완료 된 후 루프 변수가 바인딩되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-218">In particular, the loop variable is not bound after the for loop is completed.</span></span>

### <a name="repeat-until-success-loop"></a><span data-ttu-id="1372f-219">반복-성공 루프</span><span class="sxs-lookup"><span data-stu-id="1372f-219">Repeat-Until-Success Loop</span></span>

<span data-ttu-id="1372f-220">`repeat` 문은 "성공 될 때까지 반복" 패턴을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-220">The `repeat` statement supports the quantum “repeat until success” pattern.</span></span>
<span data-ttu-id="1372f-221">`repeat`키워드, 문 블록 ( _루프_ 본문), 키워드 `until`, 부울 식, 종료 세미콜론 또는 키워드 `fixup` 뒤에 다른 문 블록 ( _픽스업_)이 오는 키워드로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-221">It consists of the keyword `repeat`, followed by a statement block (the _loop_ body), the keyword `until`, a Boolean expression, and either a terminating semicolon or the keyword `fixup` followed by another statement block (the _fixup_).</span></span>
<span data-ttu-id="1372f-222">루프 본문, 조건 및 픽스업은 모두 단일 범위로 간주 되므로 본문에 바인딩된 기호는 조건 및 픽스업에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-222">The loop body, condition, and fixup are all considered to be a single scope, so symbols bound in the body are available in the condition and fixup.</span></span>

```qsharp
mutable iter = 1;
repeat {
    ProbabilisticCircuit(qubits);
    let success = ComputeSuccessIndicator(qubits);
}
until (success || iter > maxIter)
fixup {
    iter += 1;
    ComputeCorrection(qubits);
}
```

<span data-ttu-id="1372f-223">루프 본문이 실행 된 후 조건이 평가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-223">The loop body is executed, and then the condition is evaluated.</span></span>
<span data-ttu-id="1372f-224">조건이 true 이면 문이 완료 된 것입니다. 그렇지 않으면 픽스업이 실행 되 고 문이 루프 본문부터 다시 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-224">If the condition is true, then the statement is completed; otherwise, the fixup is executed, and the statement is re-executed starting with the loop body.</span></span>
<span data-ttu-id="1372f-225">픽스업 실행을 완료 하면 해당 문의 범위가 끝나기 때문에 본문 또는 픽스업 중에 만든 기호 바인딩을 후속 반복에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-225">Note that completing the execution of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="1372f-226">예를 들어 다음 코드는 Hadamard 및 T 게이트를 사용 하 여 $V _3 = (\boldone + 2 i Z)/\sqrt{5}$ 중요 한 회전 게이트를 구현 하는 확률 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-226">For example, the following code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the Hadamard and T gates.</span></span>
<span data-ttu-id="1372f-227">루프는 평균에서 $ \frac{8}{5}$ 반복에서 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-227">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="1372f-228">자세한 내용은 [*반복-성공--성공: 단일 기능 비트 unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick 및 svore, 2014)의 비결 정적 분해를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1372f-228">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for details.</span></span>

```qsharp
using (qubit = Qubit()) {
    repeat {
        H(qubit);
        T(qubit);
        CNOT(target, qubit);
        H(qubit);
        Adjoint T(qubit);
        H(qubit);
        T(qubit);
        H(qubit);
        CNOT(target, qubit);
        T(qubit);
        Z(target);
        H(qubit);
        let result = M(qubit);
    } until (result == Zero);
}
```

> [!TIP]   
> <span data-ttu-id="1372f-229">함수 내에서-success 루프를 사용 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="1372f-229">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="1372f-230">함수에서 루프를 통해 해당 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-230">The corresponding functionality is provided by while loops in functions.</span></span> 

### <a name="while-loop"></a><span data-ttu-id="1372f-231">While 루프</span><span class="sxs-lookup"><span data-stu-id="1372f-231">While Loop</span></span>

<span data-ttu-id="1372f-232">반복-성공 패턴에는 퀀텀 별 connotation가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-232">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="1372f-233">이러한 클래스는 특정 퀀텀 알고리즘 클래스에서 널리 사용 되므로 Q #에서 전용 언어 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-233">They are widely used in particular classes of quantum algorithms -- hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="1372f-234">그러나 조건에 따라 중단 되 고 해당 실행 길이는 컴파일 시간에 알 수 없는 루프는 퀀텀 런타임에서 특히 주의 해 서 처리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-234">However, loops that break based on a condition and whose execution length is thus unknown at compile time need to be handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="1372f-235">반면에 함수 내에서의 사용은 기존 (비 퀀텀) 하드웨어에서 실행 되는 코드만 포함 하기 때문에 문제가 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-235">Their use within functions on the other hand is unproblematic, since these only contain code that will be executed on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="1372f-236">따라서 Q #은 함수 내 에서만 while 루프를 사용할 수 있도록 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-236">Q# therefore supports to use of while loops within functions only.</span></span> <span data-ttu-id="1372f-237">`while` 문은 키워드 `while`, 여는 괄호 `(`, 조건 (예: 부울 식), 닫는 괄호 `)`및 문 블록으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-237">A `while` statement consists of the keyword `while`, an open parenthesis `(`, a condition (i.e. a Boolean expression), a close parenthesis `)`, and a statement block.</span></span>
<span data-ttu-id="1372f-238">문 블록 (루프의 본문)은 조건이 `true`로 평가 되는 동안 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-238">The statement block (the body of the loop) is executed as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

### <a name="conditional-statement"></a><span data-ttu-id="1372f-239">조건문</span><span class="sxs-lookup"><span data-stu-id="1372f-239">Conditional Statement</span></span>

<span data-ttu-id="1372f-240">`if` 문은 조건부 실행을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-240">The `if` statement supports conditional execution.</span></span>
<span data-ttu-id="1372f-241">키워드 `if`, 여는 괄호 `(`, 부울 식, 닫는 괄호 `)`및 문 블록 ( _then_ 블록)으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-241">It consists of the keyword `if`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="1372f-242">다음에는 여러 개의 else if 절이 올 수 있습니다. 각 절은 `elif`, 여는 괄호 `(`, 부울 식, 닫는 괄호 `)`및 문 블록 ( _else if_ 블록)으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-242">This may be followed by any number of else-if clauses, each of which consists of the keyword `elif`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="1372f-243">마지막으로, 다른 문 블록 ( _else_ 블록) 뒤에 오는 키워드 `else` 구성 된 else 절을 사용 하 여 문을 선택적으로 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-243">Finally, the statement may optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>
<span data-ttu-id="1372f-244">조건이 평가 되 고 true 이면 then 블록이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-244">The condition is evaluated, and if it is true, the then block is executed.</span></span>
<span data-ttu-id="1372f-245">조건이 false 이면 첫 번째 else 조건이 평가 됩니다. true 이면 else 블록을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-245">If the condition is false, then the first else-if condition is evaluated; if it is true, that else-if block is executed.</span></span>
<span data-ttu-id="1372f-246">그렇지 않으면 두 번째 else if 블록이 테스트 되 고, 세 번째는 조건이 true 인 절이 발생 하거나 else if 절이 더 이상 없을 때까지 테스트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-246">Otherwise, the second else-if block is tested, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="1372f-247">원래 if 조건과 모든 else if 절이 false 이면 else 블록이 제공 된 경우 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-247">If the original if condition and all else-if clauses evaluate to false, the else block is executed if one was provided.</span></span>

<span data-ttu-id="1372f-248">실행 되는 블록은 자체 범위에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-248">Note that whichever block is executed is executed in its own scope.</span></span>
<span data-ttu-id="1372f-249">Then, else-if 또는 else 블록 내부에서 만든 바인딩은 if 문의 끝 뒤에 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-249">Bindings made inside of a then, else-if, or else block are not visible after the end of the if statement.</span></span>

<span data-ttu-id="1372f-250">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-250">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
} 
```

<span data-ttu-id="1372f-251">또는</span><span class="sxs-lookup"><span data-stu-id="1372f-251">or</span></span>

```qsharp
if (i == 1) {
    X(target);
} elif (i == 2) {
    Y(target);
} else {
    Z(target);
}
```

### <a name="return"></a><span data-ttu-id="1372f-252">반환 값</span><span class="sxs-lookup"><span data-stu-id="1372f-252">Return</span></span>

<span data-ttu-id="1372f-253">Return 문은 작업 또는 함수의 실행을 종료 하 고 호출자에 게 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-253">The return statement ends execution of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="1372f-254">`return`키워드와 해당 형식의 식, 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-254">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="1372f-255">빈 튜플 `()`반환 하는 호출 가능에는 return 문이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-255">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
<span data-ttu-id="1372f-256">초기 종료를 사용 하는 경우이 경우 `return ()` 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-256">If an early exit is desired, `return ()` may be used in this case.</span></span>
<span data-ttu-id="1372f-257">다른 형식을 반환 하는 callables에는 최종 return 문이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-257">Callables that return any other type require a final return statement.</span></span>

<span data-ttu-id="1372f-258">작업 내에는 최대 개수의 return 문이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-258">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="1372f-259">문이 블록 내의 return 문 뒤에 오는 경우 컴파일러는 경고를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-259">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

<span data-ttu-id="1372f-260">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-260">For example,</span></span>

```qsharp
return 1;
```

<span data-ttu-id="1372f-261">또는</span><span class="sxs-lookup"><span data-stu-id="1372f-261">or</span></span>

```qsharp
return ();
```

<span data-ttu-id="1372f-262">또는</span><span class="sxs-lookup"><span data-stu-id="1372f-262">or</span></span>

```qsharp
return (results, qubits);
```

### <a name="fail"></a><span data-ttu-id="1372f-263">실패</span><span class="sxs-lookup"><span data-stu-id="1372f-263">Fail</span></span>

<span data-ttu-id="1372f-264">Fail 문은 작업 실행을 종료 하 고 호출자에 게 오류 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-264">The fail statement ends execution of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="1372f-265">`fail`키워드와 문자열 및 종료 세미콜론으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-265">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="1372f-266">문자열은 오류 메시지로 기존 드라이버에 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-266">The string is returned to the classical driver as the error message.</span></span>

<span data-ttu-id="1372f-267">작업 내의 실패 문 수에 대 한 제한은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-267">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="1372f-268">문이 블록 내의 fail 문 뒤에 오는 경우 컴파일러는 경고를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-268">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="1372f-269">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-269">For example,</span></span>

```qsharp
fail $"Impossible state reached";
```

<span data-ttu-id="1372f-270">또는</span><span class="sxs-lookup"><span data-stu-id="1372f-270">or</span></span>

```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="qubit-management"></a><span data-ttu-id="1372f-271">이상 비트 관리</span><span class="sxs-lookup"><span data-stu-id="1372f-271">Qubit Management</span></span>

<span data-ttu-id="1372f-272">이러한 문은 함수 본문 내에서 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-272">Note that none of these statements are allowed within the body of a function.</span></span>
<span data-ttu-id="1372f-273">작업 내 에서만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-273">They are only valid within operations.</span></span>

### <a name="clean-qubits"></a><span data-ttu-id="1372f-274">정리 비트</span><span class="sxs-lookup"><span data-stu-id="1372f-274">Clean Qubits</span></span>

<span data-ttu-id="1372f-275">`using` 문은 문 블록 중에 사용할 새 요소를 가져오는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-275">The `using` statement is used to acquire new qubits for use during a statement block.</span></span>
<span data-ttu-id="1372f-276">이는 계산 `Zero` 상태로 초기화 되도록 보장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-276">The qubits are guaranteed to be initialized to the computational `Zero` state.</span></span>
<span data-ttu-id="1372f-277">이 요소는 문 블록의 끝에서 계산 `Zero` 상태 여야 합니다. 시뮬레이터는이를 적용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-277">The qubits should be in the computational `Zero` state at the end of the statement block; simulators are encouraged to enforce this.</span></span>

<span data-ttu-id="1372f-278">문은 키워드 `using`으로 구성 되 고, 여는 괄호 `(`, 바인딩, 닫는 괄호 `)`및 해당 요소를 사용할 수 있는 문 블록으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-278">The statement consists of the keyword `using`, followed by an open parenthesis `(`, a binding, a close parenthesis `)`, and the statement block within which the qubits will be available.</span></span>
<span data-ttu-id="1372f-279">바인딩은 `let` 문과 동일한 패턴을 따릅니다. 단일 기호 또는 기호의 튜플, 등호 `=`, 단일 값 또는 이니셜라이저의 일치 하는 튜플 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-279">The binding follows the same pattern as `let` statements: either a single symbol or a tuple of symbols, followed by an equals sign `=`, and either a single value or a matching tuple of initializers.</span></span>
<span data-ttu-id="1372f-280">이니셜라이저는 `Qubit()`로 표시 되는 단일의 비트 또는 `Qubit[`, `Int` 식 및 `]`로 표시 되는 비트 배열로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-280">Initializers are available either for a single qubit, indicated as `Qubit()`, or an array of qubits, indicated by `Qubit[`, an `Int` expression, and `]`.</span></span>

<span data-ttu-id="1372f-281">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-281">For example,</span></span>

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, qubits) = (Qubit(), Qubit[bits * 2 + 3])) {
    // ...
}
```

### <a name="borrowed-qubits"></a><span data-ttu-id="1372f-282">빌려의 비트</span><span class="sxs-lookup"><span data-stu-id="1372f-282">Borrowed Qubits</span></span>

<span data-ttu-id="1372f-283">`borrowing` 문은 임시 사용을 위해 필요한 비트를 가져오는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-283">The `borrowing` statement is used to obtain qubits for temporary use.</span></span> <span data-ttu-id="1372f-284">문은 키워드 `borrowing`으로 구성 되 고, 여는 괄호 `(`, 바인딩, 닫는 괄호 `)`및 해당 요소를 사용할 수 있는 문 블록으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-284">The statement consists of the keyword `borrowing`, followed by an open parenthesis `(`, a binding, a close parenthesis `)`, and the statement block within which the qubits will be available.</span></span>
<span data-ttu-id="1372f-285">바인딩은 `using` 문에 있는 것과 동일한 패턴 및 규칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-285">The binding follows the same pattern and rules as the one in a `using` statement.</span></span>

<span data-ttu-id="1372f-286">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-286">For example,</span></span>

```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, qubits) = (Qubit(), Qubit[bits * 2 + 3])) {
    // ...
}
```

<span data-ttu-id="1372f-287">인 중 한 비트는 알 수 없는 상태 이며 문 블록의 끝에 있는 범위를 벗어났습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-287">The borrowed qubits are in an unknown state and go out of scope at the end of the statement block.</span></span>
<span data-ttu-id="1372f-288">대출자는가 중에 있던 상태와 동일한 상태를 유지 하도록 커밋 합니다. 즉, 문 블록의 시작과 끝에 있는 상태는 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-288">The borrower commits to leaving the qubits in the same state they were in when they were borrowed, i.e. their state at the beginning and at the end of the statement block is expected to be the same.</span></span>
<span data-ttu-id="1372f-289">특히 borrowing 범위에는 측정값이 포함 되지 않아야 하는 일반적인 상태가 아닐 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-289">This state in particular is not necessarily a classical state, such that in most cases, borrowing scopes should not contain measurements.</span></span> 

<span data-ttu-id="1372f-290">[*Toffoli 기반 모듈식 곱하기*](https://arxiv.org/abs/1611.07995) (Haner, Roet2n Er 및 svs2017)를 사용 하 여 + 2의 팩터링 사용을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1372f-290">See [*Factoring using 2n+2 qubits with Toffoli based modular multiplication*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler, and Svore 2017) for an example of borrowed qubit use.</span></span>

<span data-ttu-id="1372f-291">Borrowing를 사용 하는 경우 시스템은 먼저 사용 중인에서 요청을 채우려고 시도 하지만,이는 `borrowing` 문의 본문 중에는 액세스 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-291">When borrowing qubits, the system will first try to fill the request from qubits that are in use but that are not accessed during the body of the `borrowing` statement.</span></span>
<span data-ttu-id="1372f-292">이러한 것이 충분 하지 않은 경우 요청을 완료 하기 위해 새 비트를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-292">If there aren't enough such qubits, then it will allocate new qubits to complete the request.</span></span>

## <a name="conjugations"></a><span data-ttu-id="1372f-293">변화</span><span class="sxs-lookup"><span data-stu-id="1372f-293">Conjugations</span></span>

<span data-ttu-id="1372f-294">기존 비트와는 달리, 더 이상 필요 하지 않은 계산에 대 한 의도 하지 않은 영향이 있을 경우이를 무조건 다시 설정 하면 나머지 계산에 원치 않는 영향이 있을 수 있으므로 퀀텀 메모리 해제는 약간 더 복잡 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-294">In contrast to classical bits, releasing quantum memory is slightly more involved since blindly resetting qubits can have undesired effects on the remaining computation if the qubits are still entangled.</span></span> <span data-ttu-id="1372f-295">메모리를 해제 하기 전에 수행 된 계산을 적절히 "실행 취소" 하 여이를 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-295">This can be avoided by properly "undoing" performed computations prior to releasing the memory.</span></span> <span data-ttu-id="1372f-296">따라서 퀀텀 컴퓨팅의 일반적인 패턴은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-296">A common pattern in quantum computing is hence the following:</span></span> 

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    outerOperation(target);
    innerOperation(target);
    Adjoint outerOperation(target);
}
```

<span data-ttu-id="1372f-297">: new: 0.9 릴리스부터는 위의 변환을 구현 하는 활용 문을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-297">:new: Starting with our 0.9 release, we support a conjugation statement that implements the transformation above.</span></span> <span data-ttu-id="1372f-298">이 문을 사용 하 여 다음과 같은 방법으로 `ApplyWith` 작업을 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-298">Using that statement, the operation `ApplyWith` can be implemented in the following way:</span></span>

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    within{ 
        outerOperation(target);
    }
    apply {
        innerOperation(target);
    }
}
```
<span data-ttu-id="1372f-299">이러한 활용은 외부 및 내부 변환을 작업으로 쉽게 사용할 수 없지만 대신 여러 문으로 구성 된 블록에서 더 편리 하 게 사용할 수 있는 경우 훨씬 더 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-299">Such a conjugation statement obviously becomes far more useful if the outer and inner transformation are not readily available as operations but are instead more convenient to describe by a block consisting of several statements.</span></span> 

<span data-ttu-id="1372f-300">블록 내에서 정의 된 문에 대 한 역 변환은 컴파일러에서 자동으로 생성 되 고 적용 블록이 완료 된 후에 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-300">The inverse transformation for the statements defined in the within-block is automatically generated by the compiler and executed after the apply-block completes.</span></span> <span data-ttu-id="1372f-301">블록 내에 사용 되는 변경할 수 있는 변수는 적용 블록에서 바인딩 가능 하지 않으므로 생성 된 변환은 블록 내에서 계산의 adjoint로 보장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-301">Since any mutable variables used as part of the within-block cannot be rebound in the apply-block, the generated transformation is guaranteed to be the adjoint of the computation in the within-block.</span></span> 

## <a name="expression-evaluation-statements"></a><span data-ttu-id="1372f-302">식 계산 문</span><span class="sxs-lookup"><span data-stu-id="1372f-302">Expression Evaluation Statements</span></span>

<span data-ttu-id="1372f-303">`Unit` 형식의 호출 식은 문으로 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-303">Any call expression of type `Unit` may be used as a statement.</span></span>
<span data-ttu-id="1372f-304">이는 `Unit`을 반환 하는 stbits에서 작업을 호출할 때 주로 사용 됩니다 .이는 문의 목적이 암시적 퀀텀 상태를 수정 하는 것 이기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-304">This is primarily of use when calling operations on qubits that return `Unit` because the purpose of the statement is to modify the implicit quantum state.</span></span>
<span data-ttu-id="1372f-305">식 계산 문에는 종료 세미콜론이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-305">Expression evaluation statements require a terminating semicolon.</span></span>

<span data-ttu-id="1372f-306">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1372f-306">For example,</span></span>

```qsharp
X(q);
CNOT(control, target);
Adjoint T(q);
```
