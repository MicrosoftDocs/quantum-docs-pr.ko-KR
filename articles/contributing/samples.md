---
title: Microsoft QDK 샘플 참여
description: Microsoft Quantum Development Kit (QDK)에 샘플 코드를 제공 하는 방법에 대해 알아봅니다.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.samples
ms.openlocfilehash: 3bd0de04a448c74eea6c3e8e3a15dcbb19f9d705
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/10/2020
ms.locfileid: "79024154"
---
# <a name="contributing-samples-to-the-quantum-development-kit"></a><span data-ttu-id="4f787-103">퀀텀 개발 키트에 대 한 샘플 기여</span><span class="sxs-lookup"><span data-stu-id="4f787-103">Contributing Samples to the Quantum Development Kit</span></span>

<span data-ttu-id="4f787-104">[샘플 리포지토리에](https://github.com/Microsoft/Quantum)코드를 작성 하는 데 관심이 있는 경우에는 퀀텀 개발 커뮤니티를 더 잘 활용 해 주셔서 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-104">If you're interested in contributing code to the [samples repository](https://github.com/Microsoft/Quantum), thank you for making the quantum development community a better place!</span></span>

## <a name="the-quantum-development-kit-samples-repository"></a><span data-ttu-id="4f787-105">퀀텀 개발 키트 샘플 리포지토리</span><span class="sxs-lookup"><span data-stu-id="4f787-105">The Quantum Development Kit Samples Repository</span></span>

<span data-ttu-id="4f787-106">가능 하면 최대한 활용할 수 있도록 준비 하는 데 도움이 되도록 샘플 리포지토리가 어떻게 배치 되는지 빠르게 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-106">To help you prepare your contribution to help out as much as possible, it's helpful to take a quick look at how the samples repository is laid out:</span></span>

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

<span data-ttu-id="4f787-107">즉, [microsoft/퀀텀 리포지토리의](https://github.com/microsoft/Quantum) 샘플은 주제 영역별로 `algorithms/`, `arithmetic/`또는 `characterization/`와 같은 여러 폴더로 세분화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-107">That is, the samples in the [microsoft/Quantum repository](https://github.com/microsoft/Quantum) are broken down by subject area into different folders such as `algorithms/`, `arithmetic/`, or `characterization/`.</span></span>
<span data-ttu-id="4f787-108">각 주제 영역에 대 한 폴더 내에서 각 샘플은 사용자가 탐색 하 고 해당 샘플을 사용 하는 데 필요한 모든 항목을 수집 하는 단일 폴더로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-108">Within the folder for each subject area, each sample consists of a single folder that collects everything a user will need to explore and make use of that sample.</span></span>

## <a name="how-samples-are-structured"></a><span data-ttu-id="4f787-109">샘플 구성 방법</span><span class="sxs-lookup"><span data-stu-id="4f787-109">How Samples are Structured</span></span>

<span data-ttu-id="4f787-110">각 폴더를 구성 하는 파일을 살펴보면 [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/chsh-game) 샘플을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-110">Looking at the files that make up each folder, let's dive into the [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/chsh-game) sample.</span></span>

| <span data-ttu-id="4f787-111">파일</span><span class="sxs-lookup"><span data-stu-id="4f787-111">File</span></span>              | <span data-ttu-id="4f787-112">Description</span><span class="sxs-lookup"><span data-stu-id="4f787-112">Description</span></span>                                                |
|-------------------|------------------------------------------------------------|
| `CHSHGame.csproj` | <span data-ttu-id="4f787-113">Q # 프로젝트 .NET Core SDK를 사용 하 여 샘플을 빌드하는 데 사용</span><span class="sxs-lookup"><span data-stu-id="4f787-113">Q# project used to build the sample with the .NET Core SDK</span></span> |
| `Game.qs`         | <span data-ttu-id="4f787-114">Q # 샘플의 작업 및 함수</span><span class="sxs-lookup"><span data-stu-id="4f787-114">Q# operations and functions for the sample</span></span>                 |
| `Host.cs`         | <span data-ttu-id="4f787-115">C#샘플을 실행 하는 데 사용 되는 호스트 프로그램</span><span class="sxs-lookup"><span data-stu-id="4f787-115">C# host program used to run the sample</span></span>                     |
| `host.py`         | <span data-ttu-id="4f787-116">샘플을 실행 하는 데 사용 되는 Python 호스트 프로그램</span><span class="sxs-lookup"><span data-stu-id="4f787-116">Python host program used to run the sample</span></span>                 |
| `README.md`       | <span data-ttu-id="4f787-117">샘플에서 수행 하는 작업 및 사용 방법에 대 한 설명서</span><span class="sxs-lookup"><span data-stu-id="4f787-117">Documentation on what the sample does and how to use it</span></span>    |

<span data-ttu-id="4f787-118">모든 샘플이 동일한 파일 집합을 포함 하는 것은 아닙니다. 예를 들어, 일부 샘플 C#은 전용 이거나 Python 호스트가 없거나 일부 샘플에는 보조 데이터 파일이 작동 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-118">Not all samples will have the exact same set of files (e.g.: some samples may be C#-only, others may not have a Python host, or some samples may require auxillary data files to work).</span></span>

## <a name="anatomy-of-a-helpful-readme-file"></a><span data-ttu-id="4f787-119">유용한 추가 정보 파일 분석</span><span class="sxs-lookup"><span data-stu-id="4f787-119">Anatomy of a Helpful README File</span></span>

<span data-ttu-id="4f787-120">그러나 사용자가 샘플을 시작 하는 데 필요한 것과 마찬가지로 특히 중요 한 파일은 `README.md` 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-120">One especially important file, though, is the `README.md` file, as that's what users need to get started with your sample!</span></span>

<span data-ttu-id="4f787-121">각 `README.md`는 docs.microsoft.com/samples을 찾는 데 도움이 되는 메타 데이터를 사용 하 여 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-121">Each `README.md` should start with some metadata that helps docs.microsoft.com/samples find your contribution.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="4f787-122">Chsh-game 샘플이 렌더링 되는 방식 확인</span><span class="sxs-lookup"><span data-stu-id="4f787-122">See how the chsh-game sample is rendered</span></span>](https://docs.microsoft.com/samples/microsoft/quantum/validating-quantum-mechanics/)

<span data-ttu-id="4f787-123">이 메타 데이터는 샘플에서 다루는 언어 (일반적으로 `qsharp`, `csharp`및 `python`)와 샘플에서 다루는 제품 (일반적으로 `qdk`만)을 나타내는 [Yaml 헤더로](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-123">This metadata is provided as a [YAML header](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) that indicates what languages your sample covers (typically, this will be `qsharp`, `csharp`, and `python`), and what products your sample covers (typically, just `qdk`).</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="1-11":::

> [!IMPORTANT]
> <span data-ttu-id="4f787-124">Docs.microsoft.com/samples에 샘플을 표시 하려면 헤더의 `page_type: sample` 키가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-124">The `page_type: sample` key in the header is required for your sample to appear at docs.microsoft.com/samples.</span></span>
> <span data-ttu-id="4f787-125">마찬가지로 `product` 및 `language` 키는 사용자가 샘플을 찾고 실행 하는 데 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-125">Similarly, the `product` and `language` keys are critical for helping users to find and run your sample.</span></span>

<span data-ttu-id="4f787-126">그런 다음 새 샘플에서 수행 하는 작업을 간략하게 소개 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-126">After that, it's helpful to give a short intro that says what your new sample does:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="13-21":::

<span data-ttu-id="4f787-127">샘플 사용자는이를 실행 하는 데 필요한 것을 확인 합니다 (예: 사용자가 양자 개발 키트만 필요 하거나 node.js와 같은 추가 소프트웨어가 필요 함).</span><span class="sxs-lookup"><span data-stu-id="4f787-127">Users of your sample will also appreciate knowing what they need to run it (e.g.: do users just need the Quantum Development Kit itself, or do they need additional software such as node.js?):</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="23-25":::

<span data-ttu-id="4f787-128">모든 것이 준비 되었으므로 사용자에 게 샘플을 실행 하는 방법을 알려줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-128">With all that in place, you can tell users how to run your sample:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="27-50":::

<span data-ttu-id="4f787-129">마지막으로 사용자에 게 샘플의 각 파일이 무엇 인지와 추가 정보를 확인할 수 있는 위치를 알려 주는 것이 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-129">Finally, it's helpful to tell users what each file in your sample does, and where they can go for more information:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="52-61":::

> [!WARNING]
> <span data-ttu-id="4f787-130">Docs.microsoft.com/samples에서 렌더링 될 때 샘플이 다른 URL에 표시 되므로 여기서 절대 Url을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f787-130">Make sure to use absolute URLs here, since your sample will appear at a different URL when rendered at docs.microsoft.com/samples!</span></span>
