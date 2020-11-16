---
title: Microsoft QDK 문서에 기여
description: Microsoft 퀀텀 설명서 집합에 개념 또는 API 콘텐츠를 참여 하는 방법에 대해 알아봅니다.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.docs
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: 2debef858c38b9a8f11264858130ed7cb41543ae
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691788"
---
# <a name="improving-documentation"></a><span data-ttu-id="eea2a-103">설명서 개선</span><span class="sxs-lookup"><span data-stu-id="eea2a-103">Improving Documentation</span></span>

<span data-ttu-id="eea2a-104">퀀텀 개발 키트에 대 한 설명서는 퀀텀 개발자가 정보를 쉽게 사용할 수 있도록 여러 가지 형태를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-104">The documentation for the Quantum Development Kit takes on several different forms, such that information is readily available to quantum developers.</span></span>

<span data-ttu-id="eea2a-105">[코드와 같은 문서](https://www.writethedocs.org/guide/docs-as-code/)원칙에 따라 모든 퀀텀 개발 키트 설명서는 코드로 형식이 지정 되 고, Git를 사용 하 여 Git를 사용 하 여 관리 됩니다 .이는 퀀텀 개발 키트를 빌드하는 데 사용 되는 소스 코드와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-105">Following the principles of [Docs as Code](https://www.writethedocs.org/guide/docs-as-code/), all Quantum Development Kit documentation is formatted as code and is managed using Git in the same way as the source code that is used to build the Quantum Development Kit.</span></span>
<span data-ttu-id="eea2a-106">대부분의 경우 코드 지원 설명서는 다양 한 형식의 [Markdown](https://daringfireball.net/projects/markdown/)로 구성 되며, 명령줄, ide 및 소스 제어에서 사용 하기 쉬운 일반 텍스트 형식으로 다양 한 형식의 텍스트를 작성 하는 데 사용 되는 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-106">For the most part, the code backing documentation consists of various forms of [Markdown](https://daringfireball.net/projects/markdown/), a language for writing out richly formatted text in a plain text format that's easy to use at the command line, in IDEs, and with source control.</span></span>
<span data-ttu-id="eea2a-107">이와 비슷한 방식으로 [MathJax](https://www.mathjax.org/) 라이브러리를 채택 하 여 아래에서 설명 하는 것 처럼 LaTeX 언어를 사용 하는 설명서에서 수학 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-107">We similarly adopt the [MathJax](https://www.mathjax.org/) library to allow for formatting mathematics in documentation using the LaTeX language, as detailed further below.</span></span>


<span data-ttu-id="eea2a-108">즉, 각 설명서 형태는 세부 정보에서 약간 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-108">That said, each form of documentation does vary somewhat in the details:</span></span>

- <span data-ttu-id="eea2a-109">**개념 설명서** 는에 게시 되는 일련의 문서를 구성 https://docs.microsoft.com/quantum 하며,이를 통해 퀀텀 컴퓨팅의 기본 사항에서 교환 형식에 대 한 기술 사양을 설명 하는 모든 것을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-109">The **conceptual documentation** consists of a set of articles that are published to https://docs.microsoft.com/quantum, and that describe everything from the basics of quantum computing to the technical specifications for interchange formats.</span></span> <span data-ttu-id="eea2a-110">이러한 문서는 풍부한 설명서 집합을 만드는 데 사용 되는 Markdown variant 인 [Flavored Markdown (DFM)](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html)로 작성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-110">These articles are written in [DocFX-Flavored Markdown (DFM)](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html), a Markdown variant used for creating rich documentation sets.</span></span>
- <span data-ttu-id="eea2a-111">**API 참조** 는 Q# 에 게시 된 각 함수, 작업 및 사용자 정의 형식에 대 한 페이지 집합입니다 https://docs.microsoft.com/qsharp/api/ .</span><span class="sxs-lookup"><span data-stu-id="eea2a-111">The **API reference** is a set of pages for each Q# function, operation, and user-defined type, published to https://docs.microsoft.com/qsharp/api/.</span></span> <span data-ttu-id="eea2a-112">이러한 페이지에는 호출 가능한 각에 대 한 입력 및 작업과 추가 정보에 대 한 링크와 예제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-112">These pages document the inputs and operations to each callable, along with examples and links to more information.</span></span> <span data-ttu-id="eea2a-113">API 참조는 Q# 각 릴리스의 일부로 소스 코드의 small DFM 문서에서 자동으로 추출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-113">The API reference is automatically extracted from small DFM documents in Q# source code as a part of each release.</span></span>
- <span data-ttu-id="eea2a-114">각 샘플 및 kata에 포함 된 **추가 정보 <!---->** 파일은 해당 샘플 또는 kata를 사용 하는 방법, 포함 된 내용, 나머지 퀀텀 개발 키트와의 관계를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-114">The **README<!---->.md** files included with each sample and kata describe how to use that sample or kata is used, what it covers, and how it relates to the rest of the Quantum Development Kit.</span></span> <span data-ttu-id="eea2a-115">이러한 파일은 코드 리포지토리에 직접 문서를 연결 하는 데 널리 사용 되는 [DFM (GitHub Flavored Markdown)](https://github.github.com/gfm/)을 사용 하 여 작성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-115">These files are written using [GitHub Flavored Markdown (GFM)](https://github.github.com/gfm/), a more lightweight alternative to DFM that's popular for attaching documentation directly to code repositories.</span></span>

## <a name="contributing-to-the-conceptual-documentation"></a><span data-ttu-id="eea2a-116">개념 설명서에 기여</span><span class="sxs-lookup"><span data-stu-id="eea2a-116">Contributing to the Conceptual Documentation</span></span>

<span data-ttu-id="eea2a-117">개념 또는 추가 정보 설명서에 대 한 향상 된 기능을 제공 하기 위해은 적절 하 게 [**MicrosoftDocs/양자**](https://github.com/MicrosoftDocs/quantum-docs-pr/
), [**microsoft/퀀텀**](https://github.com/Microsoft/Quantum)또는 [**microsoft/QuantumKatas**](https://github.com/Microsoft/QuantumKatas)로 끌어오기 요청을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-117">To contribute an improvement to the conceptual or README documentation, then, starts with a pull request onto either [**MicrosoftDocs/quantum-docs-pr**](https://github.com/MicrosoftDocs/quantum-docs-pr/
), [**Microsoft/Quantum**](https://github.com/Microsoft/Quantum), or [**Microsoft/QuantumKatas**](https://github.com/Microsoft/QuantumKatas), as is appropriate.</span></span>
<span data-ttu-id="eea2a-118">아래의 끌어오기 요청에 대해 자세히 설명 하겠습니다. 지금은 설명서를 개선 하는 데 도움이 되는 몇 가지 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-118">We'll describe more about pull requests below, but for now there's a few things that are good to keep in mind as you improve documentation:</span></span>

- <span data-ttu-id="eea2a-119">독자는 매우 광범위 한 배경에서 퀀텀 개발 키트 설명서를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-119">Readers come to the Quantum Development Kit documentation from a very wide range of backgrounds.</span></span> <span data-ttu-id="eea2a-120">퀀텀 컴퓨팅 연구를 수행 하는 있었던 교직원에 게 새롭고 흥미로운 작업을 배우는 학교 학생의 모든 사람들은 설명서를 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-120">Everyone from high school students looking to learn something new and exciting through to tenured faculty performing quantum computing research should be able to get something out of reading the documentation.</span></span> <span data-ttu-id="eea2a-121">가능 하면 판독기의 일부에 대 한 광범위 한 정보를 생각해 서는 안 됩니다. 이는 명확 하 고 액세스 가능한 설명을 제공 하거나 자세한 정보를 위해 다른 리소스에 대 한 링크를 제공할 수 있는 경우에 가장 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-121">To the extent that's possible, please don't assume extensive knowledge on the part of your readers, as they may just be starting out. It's most helpful if you can provide clear and accessible descriptions, or can provide links to other resources for more information.</span></span>
- <span data-ttu-id="eea2a-122">설명서 집합은 설명서 나 문서와 같이 배치 되지 않으며, 독자가 "중간" 처럼 보일 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-122">Documentation sets aren't laid out like books or papers, in that readers will arrive in what might seem like the "middle."</span></span> <span data-ttu-id="eea2a-123">예를 들어 검색 엔진은 인덱스를 제안 하지 않을 수도 있고, 친구가 링크를 전송 하 여 도움을 받을 수도 있습니다. 적절 한 링크와 함께 명확한 컨텍스트를 항상 제공 하 여 판독기를 도와 보세요.</span><span class="sxs-lookup"><span data-stu-id="eea2a-123">For example, search engines might not suggest the index, or they might have been sent a link by a friend trying to help them out. Try to help your reader by always providing a clear context, along with links where appropriate.</span></span>
- <span data-ttu-id="eea2a-124">일부 판독기는 가장 유용 하 게 사용할 수 있는 추상 문과 정의를 찾을 수 있는 반면, 다른 독자는 구체적 예제에서 추정 가장 잘 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-124">Some readers will find abstract statements and definitions most helpful, while other readers work best by extrapolating from concrete examples.</span></span> <span data-ttu-id="eea2a-125">일반적인 사례와 특정 예제를 모두 제공 하면 두 판독기 모두 퀀텀 프로그래밍을 최대한 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-125">Providing both the general case and specific examples can help both readers get the most out of quantum programming.</span></span>
- <span data-ttu-id="eea2a-126">특히 문서화 되는 코드를 작성 한 경우 독자에 게 명확 하지 않은 것을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-126">Especially if you also wrote the code being documented, things may be obvious to you that are not at all obvious to your reader.</span></span> <span data-ttu-id="eea2a-127">한 가지 고유한 프로그램을 프로그래밍 방식으로 사용할 수 있는 것은 아닙니다. 즉, 독자가 무엇 인지에 관계 없이 코드에서 아이디어를 표현 하는 데 가장 유용한 디자인 패턴을 추측할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-127">There's no one unique best way to program, so no matter how clever or experienced a reader might be, they can't guess at what design patterns you found the most helpful to express your ideas in code.</span></span> <span data-ttu-id="eea2a-128">판독기가 코드를 사용할 수 있도록 하는 방법에 대 한 자세한 내용은 해당 컨텍스트를 제공 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-128">Being clear about how a reader can expect to make use of your code can help provide that context.</span></span>
- <span data-ttu-id="eea2a-129">퀀텀 프로그래밍 커뮤니티의 많은 멤버는 교육 연구원 이며 주로 커뮤니티에 대 한 기여에 대 한 인용문을 통해 인식 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-129">Many members of the quantum programming community are academic researchers, and are recognized mainly through citations for their contributions to the community.</span></span> <span data-ttu-id="eea2a-130">독자 들이 추가 자료를 쉽게 찾을 수 있도록 하는 것 외에도, 용지, 통신, 블로그 게시물 및 소프트웨어 도구와 같은 교육용 자료를 적절히 명시 하 여 교육 참가자가 커뮤니티를 개선 하는 데 가장 적합 한 작업을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-130">In addition to helping readers find additional materials, making sure to properly cite academic outputs such as papers, talks, blog posts, and software tools can help academic contributors to keep doing their best work to improve the community.</span></span>
- <span data-ttu-id="eea2a-131">퀀텀 프로그래밍 커뮤니티는 광범위 하 고 wonderfully 다양 한 커뮤니티입니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-131">The quantum programming community is a broad and wonderfully diverse community.</span></span> <span data-ttu-id="eea2a-132">세 번째 사용자 예의 gendered 대명사 (예: "사용자 ..., he ...")를 사용 하는 것은 포함이 아닌 제외 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-132">The use of gendered pronouns in third-person examples (e.g.: "if a user ..., he will ...") can work to exclude rather than include.</span></span> <span data-ttu-id="eea2a-133">인용 및 링크에서 사람들의 이름을 cognizant, 비 ASCII 문자를 올바르게 포함 하는 경우 해당 멤버에 대 한 내용을 표시 하 여 커뮤니티의 다양성을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-133">Being cognizant of people's names in citations and links, and of the correct inclusion of non-ASCII characters can serve the diversity of the community by showing respect to its members.</span></span> <span data-ttu-id="eea2a-134">마찬가지로, 영어 언어의 많은 단어는 기술 설명서에서 사용 하는 경우 개별 판독기와 커뮤니티 모두에 게 피해를 일으킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-134">Similarly, many words in the English language are often used in a hateful manner, such that their use in technical documentation can cause harm both to individual readers and to the community at large.</span></span>

### <a name="referencing-sample-code-from-conceptual-articles"></a><span data-ttu-id="eea2a-135">개념 문서에서 샘플 코드 참조</span><span class="sxs-lookup"><span data-stu-id="eea2a-135">Referencing Sample Code from Conceptual Articles</span></span>

<span data-ttu-id="eea2a-136">[Samples 리포지토리의](https://github.com/Microsoft/Quantum)코드를 포함 하려면 특수 DocFX-Flavored Markdown 명령을 사용 하 여이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-136">If you want to include code from the [samples repository](https://github.com/Microsoft/Quantum), you can do so using a special DocFX-Flavored Markdown command:</span></span>

```markdown
:::code language="qsharp" source="~/quantum/samples/algorithms/chsh-game/Game.qs" range="4-8":::
```

<span data-ttu-id="eea2a-137">이 명령은 [ `Game.qs` `chsh-game` 샘플에서 파일](https://github.com/microsoft/Quantum/blob/main/samples/algorithms/chsh-game/Game.qs)의 4 ~ 8 줄을 가져와 Q# 구문 강조 표시의 용도에 대 한 코드로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-137">This command will import lines 4 to 8 of the [`Game.qs` file from the `chsh-game` sample](https://github.com/microsoft/Quantum/blob/main/samples/algorithms/chsh-game/Game.qs), marking them as Q# code for the purpose of syntax highlighting.</span></span>
<span data-ttu-id="eea2a-138">이 명령을 사용 하면 설명서의 샘플 코드를 항상 최대한 최신 상태로 유지 하기 위해 개념 아티클과 샘플 리포지토리 간에 코드를 복제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-138">Using this command, you can avoid duplicating code between conceptual articles and the samples repository, so that sample code in documentation is always as up to date as possible.</span></span>

## <a name="contributing-to-the-api-references"></a><span data-ttu-id="eea2a-139">API 참조에 기여</span><span class="sxs-lookup"><span data-stu-id="eea2a-139">Contributing to the API References</span></span>

<span data-ttu-id="eea2a-140">API 참조에 대 한 향상 된 기능을 제공 하기 위해 문서화 되는 코드에서 직접 끌어오기 요청을 여는 것이 가장 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-140">To contribute an improvement to the API references, it's most helpful to open a pull request directly on the code being documented.</span></span>
<span data-ttu-id="eea2a-141">각 함수, 작업 또는 사용자 정의 형식은 문서 주석을 지원 합니다 (대신로 표시 됨 `///` `//` ).</span><span class="sxs-lookup"><span data-stu-id="eea2a-141">Each function, operation, or user-defined type supports a documentation comment (denoted with `///` instead of `//`).</span></span>
<span data-ttu-id="eea2a-142">퀀텀 개발 키트의 각 릴리스를 컴파일할 때 이러한 주석은 https://docs.microsoft.com/qsharp/api/ 각 호출의 입력 및 출력에 대 한 세부 정보, 호출할 수 있는 각각의 가정 및 사용 방법에 대 한 예제를 포함 하 여에 대 한 API 참조를 생성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-142">When we compile each release of the Quantum Development Kit, these comments are used to generate the API reference at https://docs.microsoft.com/qsharp/api/, including details about the inputs to and outputs from each callable, the assumptions each callable makes, and examples of how to use them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eea2a-143">이러한 파일은 각각의 새 릴리스로 덮어쓰므로 생성 된 API 설명서를 수동으로 편집 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="eea2a-143">Please make sure to not manually edit the generated API documentation, as these files are overwritten with each new release.</span></span>
> <span data-ttu-id="eea2a-144">우리는 커뮤니티에 대 한 기여를 제공 하 고 변경 내용이 릴리스 후 사용자의 릴리스를 계속 하는 데 도움이 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-144">We value your contribution to the community, and want to make sure that your changes continue to help users release after release.</span></span>

<span data-ttu-id="eea2a-145">예를 들어 함수를 살펴보겠습니다 `ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="eea2a-145">For example, consider the function `ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="eea2a-146">설명서 주석은 사용자가 및 함수를 해석 하는 방법을 이해 하는 데 도움이 됩니다 `bits` `oracle` .</span><span class="sxs-lookup"><span data-stu-id="eea2a-146">A documentation comment should help a user learn how to interpret `bits` and `oracle` and what the function is for.</span></span>
<span data-ttu-id="eea2a-147">이러한 각 정보는 Q# 설명서 주석에서 특수 하 게 명명 된 Markdown 섹션을 통해 컴파일러에 제공 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-147">Each of these different pieces of information can be provided to the Q# compiler by a specially named Markdown section in the documentation comment.</span></span>
<span data-ttu-id="eea2a-148">예를 들어 `ControlledOnBitString` 다음과 같은 항목을 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-148">For the example of `ControlledOnBitString`, we might write something like the following:</span></span>

```qsharp
 /// # Summary
 /// Returns a unitary operation that applies an oracle on the target register if the 
 /// control register state corresponds to a specified bit mask.
 ///
 /// # Description
 /// The output of this function is an operation that can be represented by a
 /// unitary transformation $U$ such that
 /// \begin{align}
 ///     U \ket{b_0 b_1 \cdots b_{n - 1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_{n-1}} \otimes
 ///     \begin{cases}
 ///         V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_{n - 1}) = \texttt{bits} \\\\
 ///         \ket{\psi} & \textrm{otherwise}
 ///     \end{cases},
 /// \end{align}
 /// where $V$ is a unitary transformation that represents the action of the
 /// `oracle` operation.
 ///
 /// # Input
 /// ## bits
 /// The bit string to control the given unitary operation on.
 /// ## oracle
 /// The unitary operation to be applied on the target register.
 ///
 /// # Output
 /// A unitary operation that applies `oracle` on the target register if the control 
 /// register state corresponds to the bit mask `bits`.
 ///
 /// # Remarks
 /// The length of `bits` and `controlRegister` must be equal.
 ///
 /// Given a Boolean array `bits` and a unitary operation `oracle`, the output of this function
 /// is an operation that performs the following steps:
 /// * apply an `X` operation to each qubit of the control register that corresponds to `false` 
 /// element of the `bits`;
 /// * apply `Controlled oracle` to the control and target registers;
 /// * apply an `X` operation to each qubit of the control register that corresponds to `false` 
 /// element of the `bits` again to return the control register to the original state.
 ///
 /// The output of the `Controlled` functor is a special case of `ControlledOnBitString` where `bits` is equal to `[true, ..., true]`.
 ///
 /// # Example
 /// The following code snippets are equivalent:
 /// ```qsharp
 /// (ControlledOnBitString(bits, oracle))(controlRegister, targetRegister);
 /// ```
 /// and
 /// ```qsharp
 /// within {
 ///     ApplyPauliFromBitString(PauliX, false, bits, controlRegister);
 /// } apply {
 ///     Controlled oracle(controlRegister, targetRegister);
 /// }
 /// ```
 ///
 /// The following code prepares a state $\frac{1}{2}(\ket{00} - \ket{01} + \ket{10} + \ket{11})$:
 /// ```qsharp
 /// using (register = Qubit[2]) {
 ///     ApplyToEach(H, register);
 ///     (ControlledOnBitString([false], Z))(register[0..0], register[1]);
 /// }
 /// ```
 function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
 {
     return ControlledOnBitStringImpl(bits, oracle, _, _);
 }
```

<span data-ttu-id="eea2a-149">[ `ControlledOnBitString` 함수에 대 한 API 설명서](xref:Microsoft.Quantum.Canon.ControlledOnBitString)에서 위의 코드에 대해 렌더링 된 버전을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-149">You can see the rendered version of the code above in the [API documentation for the `ControlledOnBitString` function](xref:Microsoft.Quantum.Canon.ControlledOnBitString).</span></span>

<span data-ttu-id="eea2a-150">문서 작성에 대 한 일반적인 관행 외에도 API 문서 주석을 작성 하면 몇 가지 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-150">In addition to the general practice of documentation writing, in writing API documentation comments it helps to keep a few things in mind:</span></span>

- <span data-ttu-id="eea2a-151">각 문서 주석의 형식은 Q# 컴파일러가 제대로 표시 될 수 있도록 컴파일러가 기대 하는 내용과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-151">The format of each documentation comment has to match what the Q# compiler expects for your documentation to appear correctly.</span></span> <span data-ttu-id="eea2a-152">예를 들어, 일부 섹션 `/// # Remarks` 은 자유형 콘텐츠를 허용 하지만 섹션과 같은 섹션 `/// # See Also` 은 더 제한적입니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-152">Some sections, such as `/// # Remarks` allow for freeform content, while sections such as `/// # See Also` section are more restrictive.</span></span>
- <span data-ttu-id="eea2a-153">판독기는 주 API 참조 사이트, 각 네임 스페이스에 대 한 요약 또는 가리키기 정보를 사용 하 여 IDE 내 에서도 API 설명서를 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-153">A reader may read your API documentation on the main API reference site, on the summary for each namespace, or even from within their IDE through the use of hover information.</span></span> <span data-ttu-id="eea2a-154">`/// # Summary`문장에 대 한 보다 길지 않으면 판독기가 더 많은 부분을 읽고 있는지 확인 하 고 네임 스페이스 요약을 통해 신속 하 게 검색 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-154">Making sure that `/// # Summary` isn't longer than about a sentence helps your reader quickly sort out whether they need to read further or look elsewhere, and can help in quickly scanning through namespace summaries.</span></span>
- <span data-ttu-id="eea2a-155">설명서가 코드 자체 보다 훨씬 더 오래 걸릴 수 있지만이는 정상입니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-155">Your documentation may well wind up being much longer than the code itself, but that's OK!</span></span> <span data-ttu-id="eea2a-156">코드가 존재 하는 컨텍스트를 모르는 사용자에 게 예기치 않은 결과가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-156">Even a small piece of code can have unexpected effects to users that don't know the context in which that code exists.</span></span> <span data-ttu-id="eea2a-157">구체적인 예제와 명확한 설명을 제공 하 여 사용자가 사용할 수 있는 코드를 최대한 활용할 수 있도록 도와 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eea2a-157">By providing concrete examples and clear explanations, you can help users make the best use of the code that's available to them.</span></span>

<!-- ## LaTeX Formatting ##

**TODO** -->
