---
title: Microsoft QDK 샘플 참여
description: Microsoft Quantum Development Kit (QDK)에 샘플 코드를 제공 하는 방법에 대해 알아봅니다.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.samples
ms.openlocfilehash: 3bd0de04a448c74eea6c3e8e3a15dcbb19f9d705
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275398"
---
# <a name="contributing-samples-to-the-quantum-development-kit"></a>퀀텀 개발 키트에 대 한 샘플 기여

[샘플 리포지토리에](https://github.com/Microsoft/Quantum)코드를 작성 하는 데 관심이 있는 경우에는 퀀텀 개발 커뮤니티를 더 잘 활용 해 주셔서 감사 합니다.

## <a name="the-quantum-development-kit-samples-repository"></a>퀀텀 개발 키트 샘플 리포지토리

가능 하면 최대한 활용할 수 있도록 준비 하는 데 도움이 되도록 샘플 리포지토리가 어떻게 배치 되는지 빠르게 확인 하는 것이 좋습니다.

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

즉, [microsoft/퀀텀 리포지토리의](https://github.com/microsoft/Quantum) 샘플은 주제 영역별로, 또는와 같은 여러 폴더로 세분화 됩니다 `algorithms/` `arithmetic/` `characterization/` .
각 주제 영역에 대 한 폴더 내에서 각 샘플은 사용자가 탐색 하 고 해당 샘플을 사용 하는 데 필요한 모든 항목을 수집 하는 단일 폴더로 구성 됩니다.

## <a name="how-samples-are-structured"></a>샘플 구성 방법

각 폴더를 구성 하는 파일을 살펴보면 샘플을 살펴보겠습니다 [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/chsh-game) .

| 파일              | 설명                                                |
|-------------------|------------------------------------------------------------|
| `CHSHGame.csproj` | Q # 프로젝트 .NET Core SDK를 사용 하 여 샘플을 빌드하는 데 사용 |
| `Game.qs`         | Q # 샘플의 작업 및 함수                 |
| `Host.cs`         | 샘플을 실행 하는 데 사용 되는 c # 호스트 프로그램                     |
| `host.py`         | 샘플을 실행 하는 데 사용 되는 Python 호스트 프로그램                 |
| `README.md`       | 샘플에서 수행 하는 작업 및 사용 방법에 대 한 설명서    |

모든 샘플이 동일한 파일 집합을 포함 하는 것은 아닙니다. 예를 들어 일부 샘플은 c # 전용 이거나, 다른 일부 샘플은 Python 호스트를 포함 하지 않을 수도 있고, 일부 샘플은 보조 데이터 파일을 사용 해야 할 수도 있습니다.

## <a name="anatomy-of-a-helpful-readme-file"></a>유용한 추가 정보 파일 분석

그러나 특히 중요 한 파일은 `README.md` 사용자가 샘플을 시작 하는 데 필요한 파일입니다.

각 `README.md` 은 docs.microsoft.com/samples을 찾는 데 도움이 되는 몇 가지 메타 데이터로 시작 해야 합니다.

> [!div class="nextstepaction"]
> [Chsh-game 샘플이 렌더링 되는 방식 확인](https://docs.microsoft.com/samples/microsoft/quantum/validating-quantum-mechanics/)

이 메타 데이터는 샘플에서 [YAML header](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) 다루는 언어 (일반적으로, `qsharp` `csharp` 및 `python` )와 샘플에서 다루는 제품 (일반적으로)을 나타내는 yaml 헤더로 제공 됩니다 `qdk` .

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="1-11":::

> [!IMPORTANT]
> `page_type: sample`샘플을 docs.microsoft.com/samples에 표시 하려면 헤더의 키가 필요 합니다.
> 마찬가지로 `product` 및 `language` 키는 사용자가 샘플을 찾고 실행할 수 있도록 하는 데 중요 합니다.

그런 다음 새 샘플에서 수행 하는 작업을 간략하게 소개 하는 것이 좋습니다.

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="13-21":::

샘플 사용자는이를 실행 하는 데 필요한 항목을 확인 합니다. 예를 들어 사용자는 사용자에 게 퀀텀 개발 키트만 필요 하거나 node.js 같은 추가 소프트웨어가 필요 합니다.

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="23-25":::

모든 것이 준비 되었으므로 사용자에 게 샘플을 실행 하는 방법을 알려줄 수 있습니다.

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="27-50":::

마지막으로 사용자에 게 샘플의 각 파일이 무엇 인지와 추가 정보를 확인할 수 있는 위치를 알려 주는 것이 유용 합니다.

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="52-61":::

> [!WARNING]
> Docs.microsoft.com/samples에서 렌더링 될 때 샘플이 다른 URL에 표시 되므로 여기서 절대 Url을 사용 해야 합니다.
