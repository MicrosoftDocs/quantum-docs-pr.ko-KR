---
title: Q#에서 Grover의 검색 알고리즘 실행 - Quantum Development Kit
description: 정식 양자 알고리즘 중 하나인 Grover의 알고리즘을 보여 주는 Q# 프로젝트를 빌드합니다.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: 0e64fcd56929fa33397c45bf1b2e99bf687eca6f
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "77906953"
---
# <a name="quickstart-implement-grovers-search-algorithm-in-q"></a>빠른 시작: Q#에서 Grover의 검색 알고리즘 구현

이 빠른 시작에서는 Grover 검색을 빌드하고 실행하여 비정형 데이터의 검색 속도를 높이는 방법을 배울 수 있습니다.  Grover 검색은 가장 인기 있는 양자 컴퓨팅 알고리즘의 하나이며, 비교적 소규모의 Q# 구현을 통해 양자 알고리즘을 표현하는 고급 Q# 양자 프로그래밍 언어를 사용하여 양자 솔루션 프로그래밍의 장점을 이해할 수 있습니다.  이 가이드를 마치면 클래식 컴퓨터에서 전체 목록을 검색하는 데 소요되는 시간보다 훨씬 짧은 시간에 시뮬레이션 출력이 특정 문자열과 함께 순서대로 정렬된 항목 목록을 찾는 것을 볼 수 있습니다.

Grover의 알고리즘은 특정 항목에 대한 비정형 데이터의 목록을 검색합니다. 예를 들어 다음과 같은 질문에 답할 수 있습니다. 한 벌의 카드에서 뽑은 이 카드는 하트 에이스인가요? 특정 항목의 레이블 지정은 _표시된 입력_이라고 합니다.

Grover의 검색 알고리즘을 사용하면 양자 컴퓨터에서 검색 중인 목록의 항목 수보다 더 적은 단계에서 이 검색을 실행할 수 있습니다. 즉 클래식 알고리즘에서 수행할 수 있는 작업이 없습니다. 카드 한 벌의 경우 증가된 속도는 무시할 수 있지만, 수백만 또는 수십억 개의 항목이 포함된 목록에서는 상당한 시간이 걸립니다.

Grover의 검색 알고리즘은 몇 줄의 코드만으로 빌드할 수 있습니다.

## <a name="prerequisites"></a>사전 요구 사항

- Microsoft [Quantum Development Kit][install]

## <a name="what-does-grovers-search-algorithm-do"></a>Grover의 검색 알고리즘에서 수행하는 작업은 무엇인가요?

Grover의 알고리즘은 목록의 항목이 검색 중인 항목인지 여부를 묻습니다. 이를 위해 각 계수 또는 확률 진폭을 사용하여 목록의 인덱스에 대한 양자 중첩을 생성하여 특정 인덱스가 찾고 있는 인덱스일 확률을 나타냅니다.

알고리즘의 핵심에는 해당 계수의 확률 진폭이 1에 도달할 때까지 찾고 있는 인덱스의 계수를 점진적으로 증가시키는 두 단계가 있습니다.

증분 증폭의 수는 목록의 항목 수보다 작습니다. 이러한 이유로 Grover의 검색 알고리즘에서 클래식 알고리즘보다 적은 단계로 검색을 수행합니다.

![Grover의 검색 알고리즘에 대한 기능 다이어그램](~/media/grover.png)

## <a name="write-the-code"></a>코드 작성

1. Quantum Development Kit를 사용하여 선택한 개발 환경에서 `Grover`라는 [새 Q# 프로젝트를 만듭니다](xref:microsoft.quantum.howto.createproject).

1. 다음 코드를 새 프로젝트의 `Operations.qs` 파일에 추가합니다.

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-40":::

1. 검색하는 목록을 정의하려면 새 `Reflections.qs` 파일을 만들고, 다음 코드를 붙여넣습니다.

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    `ReflectAboutMarked` 연산은 검색 중인 표시된 입력, 즉 0과 1이 교대로 반복되는 문자열을 정의합니다. 이 샘플은 표시된 입력을 하드 코딩하며, 다른 입력을 검색하도록 확장하거나 모든 입력에 대해 일반화할 수 있습니다.

1. 다음으로, 새 Q# 프로그램을 실행하여 `ReflectAboutMarked`로 표시된 항목을 찾습니다.

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Visual Studio 코드 또는 명령줄을 사용하는 Python](#tab/tabid-python)

    Python에서 새 Q# 프로그램을 실행하려면 다음 코드를 `host.py`로 저장합니다.

    :::code language="python" source="~/quantum/samples/algorithms/simple-grover/host.py" range="9-14":::

    그러면 명령줄에서 Python 호스트 프로그램을 실행할 수 있습니다.

    ```bash
    $ python host.py
    Preparing Q# environment...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    [0, 1, 0, 1, 0]
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[Visual Studio 코드 또는 명령줄을 사용하는 C#](#tab/tabid-csharp)

    C#에서 새 Q# 프로그램을 실행하려면 다음 C# 코드를 포함하도록 `Driver.cs`를 수정합니다.

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    그러면 명령줄에서 C# 호스트 프로그램을 실행할 수 있습니다.

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```

    ### <a name="c-with-visual-studio-2019"></a>[Visual Studio 2019를 사용하는 C#](#tab/tabid-vs2019)

    Visual Studio를 사용하여 C#에서 새 Q# 프로그램을 실행하려면 다음 C# 코드를 포함하도록 `Driver.cs`를 수정합니다.

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    그런 다음, F5 키를 누르면 프로그램이 실행되고 새 창에 다음 결과가 표시됩니다. 

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```
    ***

    `ReflectAboutMarked` 연산은 4번만 호출되지만, Q# 프로그램이 2^{5} = 32$ 가능한 입력 중에서 "01010" 입력을 찾을 수 있었습니다!

## <a name="next-steps"></a>다음 단계

이 빠른 시작을 사용한 경우 Q#을 사용하여 사용자 고유의 양자 애플리케이션을 작성하는 방법을 자세히 알아보기 위해 아래 리소스 중 일부를 확인하세요.

- [QDK 시작 가이드로 돌아가기](xref:microsoft.quantum.welcome)
- 더 일반적인 Grover의 검색 알고리즘 [샘플](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)을 사용해 보기
- [Quantum Katas에서 Grover 검색에 대해 자세히 알아보기](xref:microsoft.quantum.overview.katas)
- Grover 검색 알고리즘의 기반이 되는 양자 컴퓨팅 기술인 [진폭 증폭](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification)에 대해 자세히 알아봅니다.
- [양자 컴퓨팅 개념](xref:microsoft.quantum.concepts.intro)
- [Quantum Development Kit 샘플](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
