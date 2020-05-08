---
title: Q#에서 Grover의 검색 알고리즘 실행 - Quantum Development Kit
description: 정식 양자 알고리즘 중 하나인 Grover의 알고리즘을 보여 주는 Q# 프로젝트를 빌드합니다.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: c67ccd16957ceef694552bdd9c073ba5a35d8aaf
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/01/2020
ms.locfileid: "82686839"
---
# <a name="quickstart-implement-grovers-search-algorithm-in-q"></a>빠른 시작: Q\#에서 Grover의 검색 알고리즘 구현

이 빠른 시작에서는 Grover 검색을 빌드하고 실행하여 비정형 데이터의 검색 속도를 높이는 방법을 배울 수 있습니다.  Grover 검색은 가장 인기 있는 양자 컴퓨팅 알고리즘의 하나이며, 비교적 소규모의 Q# 구현을 통해 양자 알고리즘을 표현하는 고급 Q# 양자 프로그래밍 언어를 사용하여 양자 솔루션 프로그래밍의 장점을 이해할 수 있습니다.  가이드의 끝에서는 시뮬레이션 출력이 정렬되지 않은 항목 목록 중 특정 문자열을 찾는 데 걸리는 시간이 클래식 컴퓨터에서 전체 목록을 검색하는 데 걸리는 시간보다 짧다는 것을 볼 수 있습니다.

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

1. 다음 코드를 새 프로젝트의 `Program.qs` 파일에 추가합니다.

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-41":::

1. 검색하는 목록을 정의하려면 새 `Reflections.qs` 파일을 만들고, 다음 코드를 붙여넣습니다.

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    `ReflectAboutMarked` 연산은 검색 중인 표시된 입력, 즉 0과 1이 교대로 반복되는 문자열을 정의합니다. 이 샘플은 표시된 입력을 하드 코딩하며, 다른 입력을 검색하도록 확장하거나 모든 입력에 대해 일반화할 수 있습니다.

1. 다음으로, 새 Q# 프로그램을 실행하여 `ReflectAboutMarked`로 표시된 항목을 찾습니다.

### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a>Visual Studio 또는 Visual Studio Code를 사용한 Q# 명령줄 애플리케이션

실행 파일은 프로젝트 구성 및 명령줄 옵션에 따라 시뮬레이터 또는 리소스 예측 도구에서 `@EntryPoint()` 특성으로 표시된 작업 또는 함수를 실행합니다.

Visual Studio에서 Ctrl + F5 키를 눌러 스크립트를 실행하기만 하면 됩니다.

VS Code에서 터미널에 아래를 입력하여 `Program.qs`를 처음으로 빌드합니다.

```Command line
dotnet build
```

후속 실행 시, 다시 빌드할 필요가 없습니다. 실행하려면 다음 명령을 입력하고 Enter 키를 누릅니다.

```Command line
dotnet run --no-build
```

터미널에 다음 메시지가 표시되어야 합니다.

```
operations.qs:
This operation applies Grover's algorithm to search all possible inputs to an operation to find a particular marked state.
Usage:
operations.qs [options] [command]

--n-qubits <n-qubits> (REQUIRED)
-s, --simulator <simulator>         The name of the simulator to use.
--version                           Show version information
-?, -h, --help                      Show help and usage information
Commands:
```

이는 사용할 큐비트 수를 지정하지 않았기 때문에 터미널에서 실행 파일에 사용할 수 있는 명령을 알려줍니다. 5개의 큐비트를 사용하려면 다음을 입력해야 합니다.

```Command line
dotnet run --n-qubits 5
```

Enter를 누르면 다음 출력이 표시됩니다.

```
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
[Zero,One,Zero,One,Zero]
```

## <a name="next-steps"></a>다음 단계

이 빠른 시작을 사용한 경우 Q#을 사용하여 사용자 고유의 양자 애플리케이션을 작성하는 방법을 자세히 알아보기 위해 아래 리소스 중 일부를 확인하세요.

- [QDK 시작 가이드로 돌아가기](xref:microsoft.quantum.welcome)
- 더 일반적인 Grover의 검색 알고리즘 [샘플](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)을 사용해 보기
- [Quantum Katas에서 Grover 검색에 대해 자세히 알아보기](xref:microsoft.quantum.overview.katas)
- Grover 검색 알고리즘의 기반이 되는 양자 컴퓨팅 기술인 [진폭 증폭][amplitude-amplification]에 대해 자세히 알아봅니다.
- [양자 컴퓨팅 개념](xref:microsoft.quantum.concepts.intro)
- [Quantum Development Kit 샘플](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
[amplitude-amplification]: xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification
