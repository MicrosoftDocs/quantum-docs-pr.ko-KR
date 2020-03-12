---
title: Microsoft QDK에 코드 기여
description: Microsoft Quantum Development Kit (QDK)에 샘플 및 라이브러리 코드를 제공 하는 방법에 대해 알아봅니다.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.code
ms.openlocfilehash: edc52dc4434e91258bece28812fd76b66329c6f9
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/10/2020
ms.locfileid: "79022465"
---
# <a name="contributing-code"></a><span data-ttu-id="250a3-103">코드 기여</span><span class="sxs-lookup"><span data-stu-id="250a3-103">Contributing Code</span></span>

<span data-ttu-id="250a3-104">문제를 보고 하 고 설명서를 개선 하는 것 외에도 퀀텀 개발 키트에 대 한 코드는 퀀텀 프로그래밍 커뮤니티의 동료에 게 도움이 되는 매우 직접적인 방법일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-104">In addition to reporting issues and improving documentation, contributing code to the Quantum Development Kit can be a very direct way to help your peers in the quantum programming community.</span></span>
<span data-ttu-id="250a3-105">코드를 사용 하면 문제를 해결 하거나, 새 예제를 제공 하거나, 기존 라이브러리를 더 쉽게 사용할 수 있도록 하거나 완전히 새로운 기능을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-105">By contributing code, you can help to fix issues, provide new examples, make existing libraries easier to use, or even add entirely new features.</span></span>

<span data-ttu-id="250a3-106">이 가이드에서는 기여를 가장 잘 하는 데 도움이 되도록 끌어오기 요청을 검토할 때 표시 되는 내용을 자세히 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-106">In this guide, we'll detail a bit of what we look for when we review pull requests to help your contribution do the most good.</span></span>

## <a name="what-we-look-for"></a><span data-ttu-id="250a3-107">찾는 내용</span><span class="sxs-lookup"><span data-stu-id="250a3-107">What We Look For</span></span>

<span data-ttu-id="250a3-108">이상적인 코드 기여는 퀀텀 Development Kit 리포지토리의 기존 작업을 기반으로 하 여 문제를 해결 하거나 기존 기능을 확장 하거나 리포지토리의 범위 내에 있는 새 기능을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-108">An ideal code contribution builds on the existing work in a Quantum Development Kit repository to fix issues, expand existing features, or to add new features that are within the scope of a repository.</span></span>
<span data-ttu-id="250a3-109">코드 기여를 수락 하는 경우이는 퀀텀 개발 키트 자체의 일부가 되며, 나머지 퀀텀 개발 키트와 동일한 방식으로 새로운 기능이 출시, 유지 관리 및 개발 됩니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-109">When we accept a code contribution, it becomes a part of the Quantum Development Kit itself, such that new features will be released, maintained, and developed in the same way as the rest of the Quantum Development Kit.</span></span>
<span data-ttu-id="250a3-110">따라서 기여에 의해 추가 된 기능이 잘 테스트 되 고 문서화 되는 경우 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-110">Thus, it is helpful when functionality added by a contribution is well-tested and is documented.</span></span>

### <a name="unit-tests"></a><span data-ttu-id="250a3-111">단위 테스트</span><span class="sxs-lookup"><span data-stu-id="250a3-111">Unit Tests</span></span>

<span data-ttu-id="250a3-112">라고과 같은 라이브러리를 구성 하는 Q # 함수, 작업 및 사용자 정의 형식은 [**Microsoft/QuantumLibraries**](https://github.com/Microsoft/QuantumLibraries/) 리포지토리에서 개발의 일부로 자동으로 테스트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-112">The Q# functions, operations, and user-defined types that make up libraries such as the canon are automatically tested as a part of development on the [**Microsoft/QuantumLibraries**](https://github.com/Microsoft/QuantumLibraries/) repository.</span></span>
<span data-ttu-id="250a3-113">예를 들어 새 끌어오기 요청을 열면 [Azure Pipelines](https://azure.microsoft.com/services/devops/pipelines/) 구성에서 끌어오기 요청의 변경 내용이 퀀텀 프로그래밍 커뮤니티에 의존 하는 기존 기능을 중단 하지 않았는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-113">When a new pull request is opened, for instance, our [Azure Pipelines](https://azure.microsoft.com/services/devops/pipelines/) configuration will check that the changes in the pull request do not break any existing functionality that the quantum programming community depends on.</span></span>

<span data-ttu-id="250a3-114">최신 Q # 버전을 사용 하 여 단위 테스트는 `@Test("QuantumSimulator")` 특성을 사용 하 여 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-114">With the latest Q# version, unit test are defined using the `@Test("QuantumSimulator")` attribute.</span></span> <span data-ttu-id="250a3-115">인수는 "QuantumSimulator", "ToffoliSimulator", "TraceSimulator" 또는 실행 대상을 지정 하는 정규화 된 이름일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-115">The argument may be either "QuantumSimulator", "ToffoliSimulator", "TraceSimulator", or any fully qualified name specifying the execution target.</span></span> <span data-ttu-id="250a3-116">다른 실행 대상을 정의 하는 여러 특성이 동일한 호출 가능에 연결 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-116">Several attributes defining different execution targets may be attached to the same callable.</span></span> <span data-ttu-id="250a3-117">일부 테스트는 `Test`에서 끝나는 모든 Q # 함수 및 작업을 [xunit](https://xunit.github.io/) 프레임 워크로 노출 하는 사용 되지 않는 [Microsoft.](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) n e t. n e t 장치 패키지를 계속 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-117">Some of our tests still use the deprecated [Microsoft.Quantum.Xunit](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) package that exposes all Q# functions and operations ending in `Test` to the [xUnit](https://xunit.github.io/) framework.</span></span> <span data-ttu-id="250a3-118">이 패키지는 더 이상 단위 테스트를 정의 하는 데 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-118">This package is no longer needed for defining unit tests.</span></span> 

<span data-ttu-id="250a3-119">다음 함수를 사용 하 여 <xref:microsoft.quantum.canon.fst> 및 <xref:microsoft.quantum.canon.snd> 함수에서 대표적인 예의 올바른 출력을 반환 하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-119">The following function is used to ensure that the <xref:microsoft.quantum.canon.fst> and <xref:microsoft.quantum.canon.snd> functions both return the right outputs in a representative example.</span></span>
<span data-ttu-id="250a3-120">`Fst` 또는 `Snd`의 출력이 잘못 된 경우 `fail` 문을 사용 하 여 테스트 실패를 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-120">If the output of `Fst` or `Snd` is incorrect, the `fail` statement is used to cause the test to fail.</span></span>

```qsharp
@Test("QuantumSimulator")
function PairTest () : Unit {
    let pair = (12, PauliZ);

    if (Fst(pair) != 12) {
        let actual = Fst(pair);
        fail $"Expected 12, actual {actual}.";
    }

    if (Snd(pair) != PauliZ) {
        let actual = Snd(pair);
        fail $"Expected PauliZ, actual {actual}.";
    }
}
```

<span data-ttu-id="250a3-121">표준 라이브러리 가이드의 [테스트 섹션](xref:microsoft.quantum.libraries.diagnostics) 에 있는 기술을 사용 하 여 더 복잡 한 조건을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-121">More complicated conditions can be checked using the techniques in the [testing section](xref:microsoft.quantum.libraries.diagnostics) of the standard libraries guide.</span></span>
<span data-ttu-id="250a3-122">예를 들어 다음 테스트는 <xref:microsoft.quantum.canon.applywith>에 의해 호출 되는 `H(q); X(q); H(q);` `Z(q)`와 동일한 지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-122">For instance, the following test checks that `H(q); X(q); H(q);` as called by <xref:microsoft.quantum.canon.applywith> does the same thing as `Z(q)`.</span></span>

```Q#
@Test("QuantumSimulator")
operation TestApplyWith() : Unit {
    let actual = ApplyWith(H, X, _);
    let expected = Z;
    AssertOperationsEqualReferenced(ApplyToEach(actual, _), ApplyToEachA(expected, _), 4);
}
```

<span data-ttu-id="250a3-123">새 기능을 추가 하는 경우 새 테스트를 추가 하 여 기여도가 예상 하는 작업을 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-123">When adding new features, it's a good idea to also add new tests to make sure that your contribution does what it's supposed to.</span></span>
<span data-ttu-id="250a3-124">이렇게 하면 나머지 커뮤니티에서 기능을 유지 관리 하 고 개발할 수 있으며, 특히 다른 개발자가 기능을 사용할 수 있다는 것을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-124">This helps the rest of the community to maintain and develop your feature, and in particular helps other developers know that they can rely on your feature.</span></span>

> [!NOTE]
> <span data-ttu-id="250a3-125">이는 다른 방법으로도 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-125">This works the other way around, too!</span></span>
> <span data-ttu-id="250a3-126">일부 테스트가 누락 된 기존 기능이 있는 경우 테스트 검사를 추가 하면 커뮤니티에 훌륭한 기여를 내릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-126">If there's an existing feature that's missing some tests, helping us add test coverage would make a great contribution to the community.</span></span>

<span data-ttu-id="250a3-127">로컬에서 단위 테스트는 Visual Studio 테스트 탐색기 또는 `dotnet test` 명령을 사용 하 여 실행할 수 있으므로 끌어오기 요청을 열기 전에 기여를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-127">Locally, unit tests can be run using the Visual Studio Test Explorer or the `dotnet test` command, so that you can check your contribution before opening up a pull request.</span></span>

<!-- TODO:
### Comments and Documentation ###

### Citations and References ### -->


## <a name="when-well-reject-a-pull-request"></a><span data-ttu-id="250a3-128">끌어오기 요청을 거부 하는 경우</span><span class="sxs-lookup"><span data-stu-id="250a3-128">When We'll Reject a Pull Request</span></span>

<span data-ttu-id="250a3-129">경우에 따라 끌어오기 요청이 기여를 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-129">Sometimes, we'll reject the pull request for a contribution.</span></span>
<span data-ttu-id="250a3-130">이러한 상황이 발생 하는 경우에는 특정 기여를 수락 하지 못할 수 있는 여러 가지 이유가 있으므로 잘못 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-130">If this happens to you, it doesn't mean that it's bad, as there's a number of reasons why we might not be able to accept a particular contribution.</span></span>
<span data-ttu-id="250a3-131">가장 일반적으로 퀀텀 프로그래밍 커뮤니티에 기여 하는 것은 매우 좋지만 퀀텀 개발 키트 리포지토리를 개발 하기에 적합 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-131">Perhaps most commonly, a contribution to the quantum programming community is a really good one, but the Quantum Development Kit repositories aren't the right place to develop it.</span></span>
<span data-ttu-id="250a3-132">이러한 경우에는 사용자 고유의---리포지토리를 사용 하는 것이 좋습니다 .이는 NuGet.org을 배포 하는 것과 동일한 방식으로 GitHub 및를 사용 하 여 고유한 라이브러리를 쉽게 만들고 배포할 수 있다는 것입니다. 지금 바로 라이브러리를 만드세요.</span><span class="sxs-lookup"><span data-stu-id="250a3-132">In such cases, we strongly encourage you to make your own repository --- part of the strength of the Quantum Development Kit is that it's easy to make and distribute your own libraries using GitHub and NuGet.org, the same way that we distribute the canon and chemistry libraries today.</span></span>

<span data-ttu-id="250a3-133">그 외에는 아직 유지 관리 및 개발할 준비가 되지 않았기 때문에 좋은 기여를 거부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-133">At other times, we may reject a good contribution simply because we aren't yet ready to maintain and develop it.</span></span>
<span data-ttu-id="250a3-134">모든 작업을 수행 하기 어려울 수 있으므로 로드맵으로 작업 하는 데 가장 적합 한 기능을 계획 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-134">It can be difficult to do everything, so we plan out what features we're best able to work on as a roadmap.</span></span>
<span data-ttu-id="250a3-135">이는 기능을 타사 라이브러리로 해제 하는 것이 좋은 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-135">This can be another case where releasing a feature as a third-party library can make a lot of sense.</span></span>
<span data-ttu-id="250a3-136">또는 microsoft에서 제공 하는 최상의 작업을 수행할 수 있도록 로드맵에 보다 적합 한 기능을 수정 하는 데 도움을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-136">Alternatively, we may ask for your help in modifying a feature to better fit into our roadmap so that we can do the best work we can with it.</span></span>

<span data-ttu-id="250a3-137">또한 더 많은 설명서 또는 단위 테스트가 필요한 경우에도 끌어오기 요청에 대 한 변경 사항을 요청 하 여 사용자가 기능을 찾는 것이 더 어려워질 수 있도록 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-137">We'll also ask for changes to a pull request if it requires more documentation or unit tests to help us make use of it, or if it differs enough in style from the rest of the Q# libraries that it will make it harder for users to find your feature.</span></span>
<span data-ttu-id="250a3-138">이러한 경우 추가 하거나 변경할 수 있는 항목에 대 한 코드 검토에 몇 가지 조언을 제공 하 여 참여를 더 쉽게 포함할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-138">In these cases, we'll try to offer some advice in code reviews about what can be added or changed to make your contribution easier for us to include.</span></span>

<span data-ttu-id="250a3-139">마지막으로 [Microsoft 오픈 소스 준수](https://opensource.microsoft.com/codeofconduct/)에 설명 된 대로 퀀텀 컴퓨팅 커뮤니티를 손상 시키는 기여를 수락할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-139">Finally, we cannot accept contributions that cause harm the quantum computing community, as outlined in the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).</span></span>
<span data-ttu-id="250a3-140">Microsoft는 현재 훌륭한 다양성에서 전체 퀀텀 컴퓨팅 커뮤니티를 제공 하 고 향후 더 포괄적으로 성장 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-140">We want to ensure that contributions serve the entire quantum computing community, both in its current wonderful diversity, and in the future as it grows to become still more inclusive.</span></span>
<span data-ttu-id="250a3-141">이러한 목표를 실현 하는 데 도움을 주셔서 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-141">We appreciate your help in realizing this goal.</span></span>

## <a name="next-steps"></a><span data-ttu-id="250a3-142">다음 단계</span><span class="sxs-lookup"><span data-stu-id="250a3-142">Next steps</span></span>

<span data-ttu-id="250a3-143">퀀텀 개발 키트를 전체 퀀텀 프로그래밍 커뮤니티에서 사용할 수 있도록 하는 데 도움을 주셔서 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-143">Thanks for helping to make the Quantum Development Kit a great resource for the entire quantum programming community!</span></span>
<span data-ttu-id="250a3-144">자세히 알아보려면 Q # 스타일에 대 한 다음 가이드를 계속 진행 하세요.</span><span class="sxs-lookup"><span data-stu-id="250a3-144">To learn more, please continue with the following guide on Q# style.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="250a3-145">Q # 스타일 지침에 대해 알아보기</span><span class="sxs-lookup"><span data-stu-id="250a3-145">Learn about Q# style guidelines</span></span>](xref:microsoft.quantum.contributing.style)

<span data-ttu-id="250a3-146">기여 하는 코드의 종류에 따라 기여를 가능한 한 커뮤니티에 최대한 활용 하는 데 도움이 되는 추가 사항이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="250a3-146">Depending on what kind of code you're contributing, there may be additional things to keep in mind that can help you make your contribution do as much good for the community as possible.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="250a3-147">참여 샘플에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="250a3-147">Learn about contributing samples</span></span>](xref:microsoft.quantum.contributing.samples)
