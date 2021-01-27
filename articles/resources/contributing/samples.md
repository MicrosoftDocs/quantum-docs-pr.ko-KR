---
title: Microsoft QDK 샘플 참여
description: Microsoft Quantum Development Kit (QDK)에 샘플 코드를 제공 하는 방법에 대해 알아봅니다.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: contributor-guide
uid: microsoft.quantum.contributing.samples
no-loc:
- Q#
- $$v
ms.openlocfilehash: 0c940a4cf228c694a899988f469158b1bb6e2425
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847591"
---
# <a name="contributing-samples-to-the-quantum-development-kit"></a><span data-ttu-id="b30ec-103">퀀텀 개발 키트에 대 한 샘플 기여</span><span class="sxs-lookup"><span data-stu-id="b30ec-103">Contributing Samples to the Quantum Development Kit</span></span>

<span data-ttu-id="b30ec-104">[샘플 리포지토리에](https://github.com/Microsoft/Quantum)코드를 작성 하는 데 관심이 있는 경우에는 퀀텀 개발 커뮤니티를 더 잘 활용 해 주셔서 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b30ec-104">If you're interested in contributing code to the [samples repository](https://github.com/Microsoft/Quantum), thank you for making the quantum development community a better place!</span></span>

## <a name="the-quantum-development-kit-samples-repository"></a><span data-ttu-id="b30ec-105">퀀텀 개발 키트 샘플 리포지토리</span><span class="sxs-lookup"><span data-stu-id="b30ec-105">The Quantum Development Kit Samples Repository</span></span>

<span data-ttu-id="b30ec-106">가능 하면 최대한 활용할 수 있도록 준비 하는 데 도움이 되도록 샘플 리포지토리가 어떻게 배치 되는지 빠르게 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b30ec-106">To help you prepare your contribution to help out as much as possible, it's helpful to take a quick look at how the samples repository is laid out:</span></span>

```plaintext
microsoft/Quantum
📁 samples/
  📁 algorithms/
    📁 chsh-game/
      📝 CHSHGame.csproj
      📝 Game.qs
      📝 Host.cs
      📝 host.py
      📝 README.md
     ⋮
  📁 arithmetic/
  📁 characterization/
  📁 chemistry/
   ⋮
```

<span data-ttu-id="b30ec-107">즉, [microsoft/퀀텀 리포지토리의](https://github.com/microsoft/Quantum) 샘플은 주제 영역별로, 또는와 같은 여러 폴더로 세분화 됩니다 `algorithms/` `arithmetic/` `characterization/` .</span><span class="sxs-lookup"><span data-stu-id="b30ec-107">That is, the samples in the [microsoft/Quantum repository](https://github.com/microsoft/Quantum) are broken down by subject area into different folders such as `algorithms/`, `arithmetic/`, or `characterization/`.</span></span>
<span data-ttu-id="b30ec-108">각 주제 영역에 대 한 폴더 내에서 각 샘플은 사용자가 탐색 하 고 해당 샘플을 사용 하는 데 필요한 모든 항목을 수집 하는 단일 폴더로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b30ec-108">Within the folder for each subject area, each sample consists of a single folder that collects everything a user will need to explore and make use of that sample.</span></span>

## <a name="how-samples-are-structured"></a><span data-ttu-id="b30ec-109">샘플 구성 방법</span><span class="sxs-lookup"><span data-stu-id="b30ec-109">How Samples are Structured</span></span>

<span data-ttu-id="b30ec-110">각 폴더를 구성 하는 파일을 살펴보면 샘플을 살펴보겠습니다 [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/main/samples/algorithms/chsh-game) .</span><span class="sxs-lookup"><span data-stu-id="b30ec-110">Looking at the files that make up each folder, let's dive into the [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/main/samples/algorithms/chsh-game) sample.</span></span>

| <span data-ttu-id="b30ec-111">파일</span><span class="sxs-lookup"><span data-stu-id="b30ec-111">File</span></span>              | <span data-ttu-id="b30ec-112">설명</span><span class="sxs-lookup"><span data-stu-id="b30ec-112">Description</span></span>                                                |
|-------------------|------------------------------------------------------------|
| `CHSHGame.csproj` | <span data-ttu-id="b30ec-113">Q# .NET Core SDK를 사용 하 여 샘플을 빌드하는 데 사용 되는 프로젝트입니다.</span><span class="sxs-lookup"><span data-stu-id="b30ec-113">Q# project used to build the sample with the .NET Core SDK</span></span> |
| `Game.qs`         | <span data-ttu-id="b30ec-114">Q# 샘플에 대 한 작업 및 함수</span><span class="sxs-lookup"><span data-stu-id="b30ec-114">Q# operations and functions for the sample</span></span>                 |
| `Host.cs`         | <span data-ttu-id="b30ec-115">샘플을 실행 하는 데 사용 되는 c # 호스트 프로그램</span><span class="sxs-lookup"><span data-stu-id="b30ec-115">C# host program used to run the sample</span></span>                     |
| `host.py`         | <span data-ttu-id="b30ec-116">샘플을 실행 하는 데 사용 되는 Python 호스트 프로그램</span><span class="sxs-lookup"><span data-stu-id="b30ec-116">Python host program used to run the sample</span></span>                 |
| `README.md`       | <span data-ttu-id="b30ec-117">샘플에서 수행 하는 작업 및 사용 방법에 대 한 설명서</span><span class="sxs-lookup"><span data-stu-id="b30ec-117">Documentation on what the sample does and how to use it</span></span>    |

<span data-ttu-id="b30ec-118">모든 샘플이 동일한 파일 집합을 포함 하는 것은 아닙니다. 예를 들어 일부 샘플은 c # 전용 이거나, 다른 일부 샘플은 Python 호스트를 포함 하지 않을 수도 있고, 일부 샘플은 보조 데이터 파일을 사용 해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b30ec-118">Not all samples will have the exact same set of files (e.g.: some samples may be C#-only, others may not have a Python host, or some samples may require auxillary data files to work).</span></span>

## <a name="anatomy-of-a-helpful-readme-file"></a><span data-ttu-id="b30ec-119">유용한 추가 정보 파일 분석</span><span class="sxs-lookup"><span data-stu-id="b30ec-119">Anatomy of a Helpful README File</span></span>

<span data-ttu-id="b30ec-120">그러나 특히 중요 한 파일은 `README.md` 사용자가 샘플을 시작 하는 데 필요한 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="b30ec-120">One especially important file, though, is the `README.md` file, as that's what users need to get started with your sample!</span></span>

<span data-ttu-id="b30ec-121">각 `README.md` 은 docs.microsoft.com/samples을 찾는 데 도움이 되는 몇 가지 메타 데이터로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b30ec-121">Each `README.md` should start with some metadata that helps docs.microsoft.com/samples find your contribution.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="b30ec-122">Chsh-game 샘플이 렌더링 되는 방식 확인</span><span class="sxs-lookup"><span data-stu-id="b30ec-122">See how the chsh-game sample is rendered</span></span>](https://docs.microsoft.com/samples/microsoft/quantum/validating-quantum-mechanics/)

<span data-ttu-id="b30ec-123">이 메타 데이터는 샘플에서 [](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) 다루는 언어 (일반적으로, `qsharp` `csharp` 및 `python` )와 샘플에서 다루는 제품 (일반적으로)을 나타내는 yaml 헤더로 제공 됩니다 `qdk` .</span><span class="sxs-lookup"><span data-stu-id="b30ec-123">This metadata is provided as a [YAML header](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) that indicates what languages your sample covers (typically, this will be `qsharp`, `csharp`, and `python`), and what products your sample covers (typically, just `qdk`).</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="1-11":::

> [!IMPORTANT]
> <span data-ttu-id="b30ec-124">`page_type: sample`샘플을 docs.microsoft.com/samples에 표시 하려면 헤더의 키가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b30ec-124">The `page_type: sample` key in the header is required for your sample to appear at docs.microsoft.com/samples.</span></span>
> <span data-ttu-id="b30ec-125">마찬가지로 `product` 및 `language` 키는 사용자가 샘플을 찾고 실행할 수 있도록 하는 데 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b30ec-125">Similarly, the `product` and `language` keys are critical for helping users to find and run your sample.</span></span>

<span data-ttu-id="b30ec-126">그런 다음 새 샘플에서 수행 하는 작업을 간략하게 소개 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b30ec-126">After that, it's helpful to give a short intro that says what your new sample does:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="13-21":::

<span data-ttu-id="b30ec-127">샘플 사용자는이를 실행 하는 데 필요한 항목을 확인 합니다. 예를 들어 사용자는 사용자에 게 퀀텀 개발 키트만 필요 하거나 node.js 같은 추가 소프트웨어가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b30ec-127">Users of your sample will also appreciate knowing what they need to run it (e.g.: do users just need the Quantum Development Kit itself, or do they need additional software such as node.js?):</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="23-25":::

<span data-ttu-id="b30ec-128">모든 것이 준비 되었으므로 사용자에 게 샘플을 실행 하는 방법을 알려줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b30ec-128">With all that in place, you can tell users how to run your sample:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="27-50":::

<span data-ttu-id="b30ec-129">마지막으로 사용자에 게 샘플의 각 파일이 무엇 인지와 추가 정보를 확인할 수 있는 위치를 알려 주는 것이 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b30ec-129">Finally, it's helpful to tell users what each file in your sample does, and where they can go for more information:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="52-61":::

> [!WARNING]
> <span data-ttu-id="b30ec-130">Docs.microsoft.com/samples에서 렌더링 될 때 샘플이 다른 URL에 표시 되므로 여기서 절대 Url을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b30ec-130">Make sure to use absolute URLs here, since your sample will appear at a different URL when rendered at docs.microsoft.com/samples!</span></span>
