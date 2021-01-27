---
title: 버그 보고
description: Microsoft Quantum Development Kit (QDK)를 사용 하 여 버그 또는 문제를 보고 하는 방법에 대해 알아봅니다.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: contributor-guide
uid: microsoft.quantum.contributing.reporting
no-loc:
- Q#
- $$v
ms.openlocfilehash: e15bfd0933aa10ae8f3c52295f50126d1d887dc7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857610"
---
# <a name="reporting-bugs"></a><span data-ttu-id="8e62e-103">버그 보고</span><span class="sxs-lookup"><span data-stu-id="8e62e-103">Reporting Bugs</span></span> #

<span data-ttu-id="8e62e-104">퀀텀 개발 키트의 구성 요소에서 버그를 발견 했다고 생각 되 면 보고서에 매우 많은 도움이 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8e62e-104">If you think you've found a bug in a component of the Quantum Development Kit, we would very much appreciate a report.</span></span>
<span data-ttu-id="8e62e-105">그 후에도 다른 사람이 동일한 문제로 인 한 것일 수 있습니다. 알려주세요. 모든 사용자를 위해 수정 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e62e-105">After all, someone else may be struggling with the same issue as well; letting us know helps us to get to fixing it for everyone.</span></span>
<span data-ttu-id="8e62e-106">버그를 보고 하는 첫 번째 단계는 다른 사람이 동일한 문제를 보고 했을 수 있으므로 각 리포지토리에 있는 기존 문제를 살펴보는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8e62e-106">The first step in reporting a bug is to start by looking through the existing issues found on each repository, as it's very possible that someone else has reported the same problem.</span></span>

<span data-ttu-id="8e62e-107">이전에 문제가 이미 발견 된 경우 문제를 진단 하 고 해결 하는 데 도움이 될 수 있는 추가 정보나 컨텍스트를 제공 하는 것이 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e62e-107">If the issue has already been found before, it may be helpful to provide additional information or context that can help us to diagnose and solve the problem.</span></span>
<span data-ttu-id="8e62e-108">이 경우 문제에 대 한 토론에 참여 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e62e-108">In that case, please feel free to participate in discussions on the issue.</span></span>

<span data-ttu-id="8e62e-109">이전에 버그가 보고 되지 않은 경우 해당 구성 요소에 대 한 리포지토리에서 새 문제를 열 때 감사를 드립니다.</span><span class="sxs-lookup"><span data-stu-id="8e62e-109">If your bug hasn't been reported before, then we'd appreciate if you open a new issue on the repository for the component in question.</span></span>
<span data-ttu-id="8e62e-110">새 문제를 만들 때 정보를 제공 하는 버그 보고서를 작성 하는 데 도움이 되는 정보를 제공 하는 템플릿이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e62e-110">When creating a new issue, you'll be prompted with a template that suggests some information that is often helpful in making informative bug reports:</span></span>

- <span data-ttu-id="8e62e-111">문제를 재현하기 위한 단계</span><span class="sxs-lookup"><span data-stu-id="8e62e-111">Steps to reproduce the problem</span></span>
- <span data-ttu-id="8e62e-112">발생할 것으로 예상 되는 작업</span><span class="sxs-lookup"><span data-stu-id="8e62e-112">What you expected to happen</span></span>
- <span data-ttu-id="8e62e-113">실제로 발생 한 상황</span><span class="sxs-lookup"><span data-stu-id="8e62e-113">What actually happened</span></span>
- <span data-ttu-id="8e62e-114">소프트웨어 환경에 대 한 정보 (예: OS, .NET Core 및 퀀텀 Development Kit 버전)</span><span class="sxs-lookup"><span data-stu-id="8e62e-114">Information about your software environment (e.g.: OS, .NET Core, and Quantum Development Kit versions)</span></span>

<span data-ttu-id="8e62e-115">또한 매우 간단 하 고 토론을 수행할 가치가 없는 경우 (예: 오타가 있는 경우), 버그를 직접 수정 하는 [끌어오기 요청을 만들](https://help.github.com/articles/about-pull-requests/) 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e62e-115">You can also [create a pull request](https://help.github.com/articles/about-pull-requests/) to fix the bug directly, if it's very straightforward and is not worth the discussion (for example, a typo).</span></span>

