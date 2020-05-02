---
title: 끌어오기 요청 열기
description: Microsoft Quantum Development Kit에 코드 또는 설명서를 제공할 준비가 되 면 GitHub 끌어오기 요청을 제출 하는 방법에 대해 알아봅니다.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.pulls
ms.openlocfilehash: 82af3b5123588cc06882f746ffcb0402ad3f0f2e
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82686848"
---
# <a name="opening-pull-requests"></a>끌어오기 요청 열기 #

퀀텀 개발 키트의 모든 설명서는 GitHub에서 호스트 되는 여러 리포지토리를 사용 하 여 Git 버전 제어 시스템을 통해 관리 됩니다.
Git 및 GitHub를 함께 사용 하면 퀀텀 개발 키트를 통해 광범위 하 게 공동 작업을 수행할 수 있습니다.
특히, 모든 Git 리포지토리를 복제 하거나 분기 하 여 해당 리포지토리의 완전히 독립 된 복사본을 만들 수 있습니다.
이를 통해 원하는 속도로 도구를 사용 하 여 작업을 수행할 수 있습니다.

준비가 되 면 GitHub의 _끌어오기 요청_ 기능을 사용 하 여 리포지토리에 대 한 기여를 포함 하는 요청을 보낼 수 있습니다.
각 끌어오기 요청에 대 한 페이지에는 기여를 수행 하는 모든 변경 내용, 기여에 대 한 설명 목록 및 커뮤니티의 다른 구성원이 피드백 및 조언을 제공 하는 데 사용할 수 있는 일련의 검토 도구가 포함 됩니다.

> [!NOTE]
> Git에 대 한 전체 자습서는이 가이드에서 다루지 않지만 Git 학습에 대 한 추가 리소스에 대 한 다음 링크를 제안할 수 있습니다.
>
> - [Git 배우기](https://www.atlassian.com/git): Atlassian에서 git 자습서 집합입니다.
> - [Visual Studio Code의 버전 제어](https://code.visualstudio.com/docs/editor/versioncontrol): GIT의 GUI로 Visual Studio Code를 사용 하는 방법에 대 한 가이드입니다.
> - [Github 학습 랩](https://lab.github.com/): Git, GitHub 및 관련 기술을 사용 하는 온라인 과정 집합입니다.
> - [Git 시각화](https://git-school.github.io/visualizing-git/): git 명령이 리포지토리의 상태를 변경 하는 방법을 시각화 하는 대화형 도구입니다.
> - [Git을 사용한 버전 제어 (EPQIS 2016)](https://nbviewer.jupyter.org/github/QuinnPhys/PythonWorkshop-science/blob/master/lecture-1-scicomp-tools-part1.ipynb#Version-Control-with-Git-(50-Minutes)): 과학적 컴퓨팅 지향 git 자습서입니다.
> - [Git 분기 배우기](https://learngitbranching.js.org/): 새 git 기능을 배우는 데 도움이 되는의 기준 주소 퍼즐 대화형 분기 집합입니다.

## <a name="what-is-a-pull-request"></a>끌어오기 요청 이란? ##

위에서 설명한 것 처럼 **끌어오기 요청이 무엇 인지를**확인 하는 데 몇 분 정도 걸릴 수 있습니다.
Git에서 작업 하는 경우 변경 내용은 해당 변경 내용이 리포지토리의 상태와 어떻게 관련 되어 있는지를 설명 하는 _커밋_ 으로 표시 됩니다.
이전 커밋에서 화살표가 있는 원으로 커밋을 그리는 다이어그램을 그리는 경우가 종종 있습니다.

이라는 `feature` _분기_ 에서 기여를 시작 했다고 가정 합니다.
그러면 **Microsoft/퀀텀** 분기가 다음과 같이 표시 될 수 있습니다.

![GitHub의 작업 분기](~/media/git-workflow-step0.png)

로컬 리포지토리에서 변경을 수행 하는 경우 다른 리포지토리에서 변경 내용을 _끌어_ 업스트림에 발생 한 변경 내용을 파악할 수 있습니다.

![업스트림 리포지토리에서 변경 내용 끌어오기 및 병합](~/media/git-workflow-step1.png)

끌어오기 요청은 동일한 방식으로 작동 하지만, 역방향: 끌어오기 요청을 열 때 업스트림 리포지토리가에서 기여를 가져오도록 요청 합니다.

![변경 내용을 원래 리포지토리로 다시 가져오도록 요청](~/media/git-workflow-step2.png)

리포지토리 중 하나로 끌어오기 요청을 열면 GitHub는 커뮤니티의 다른 사용자가 변경 내용 요약을 보고, 의견을 잡고, 더 나은 기여를 지 원하는 방법에 대 한 제안을 제공할 수 있는 기회를 제공 합니다.

![GitHub의 끌어오기 요청 스크린샷](~/media/pull-request-header.png)

이 프로세스를 사용 하면 GitHub 기능을 사용 하 여 기여를 개선 하 고 퀀텀 프로그래밍 커뮤니티에 대 한 고품질 제품을 유지 관리할 수 있습니다.

## <a name="how-to-make-a-pull-request"></a>끌어오기 요청을 만드는 방법 ##

끌어오기 요청을 만드는 두 가지 주요 방법이 있습니다.  
단일 파일에만 영향을 주는 작은 변경의 경우 GitHub 웹 인터페이스를 사용 하 여 끌어오기 요청을 완전히 온라인 상태로 만들 수 있습니다. 편집 하려는 파일로 이동 하 여 편집 아이콘을 사용 하면 됩니다.  
더 복잡 한 기여를 위해 먼저 리포지토리를 로컬 컴퓨터에 복제 하 여 끌어오기 요청을 준비 하는 것이 가장 쉽습니다.

<!--
### Using the Web Interface ###

**TODO**

### Command-Line and GitHub Flow ###

Most of the time, it's easier to prepare a pull request on your own computer; that makes it easier to work incrementally, and to test your changes.
If you haven't already done so, the first step is to _fork_ the repository that you'd like to contribute to.
Forking makes a complete clone of the original repository, but under your GitHub account instead of under [Microsoft](http://github.com/Microsoft/) or [MicrosoftDocs](http://github.com/MicrosoftDocs/).
This way, you can edit your personal fork to your heart's content before making a pull request for your work.

**TODO: pick up here**

## Code Review and Etiquette ##

**TODO: PR ettiquette, reviews, etc.**

-->

## <a name="next-steps"></a>다음 단계 ##

Git를 사용 하 여 퀀텀 개발 키트 커뮤니티를 도와 주세요!
코드를 작성 하는 방법에 대 한 자세한 내용을 보려면 다음 가이드를 계속 진행 하세요.

> [!div class="nextstepaction"]
> [코드에 참여 하는 방법 알아보기](xref:microsoft.quantum.contributing.code)
