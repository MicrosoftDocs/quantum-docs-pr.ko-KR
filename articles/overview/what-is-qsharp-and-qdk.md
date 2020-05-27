---
title: Q# 프로그래밍 언어 및 QDK란?
description: Microsoft Quantum Development Kit, Q# 프로그래밍 언어 및 양자 프로그램을 만드는 방법에 대해 알아봅니다.
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.q-sharp
ms.openlocfilehash: 55ac946aa935d3748b36ac99096a89d0db686835
ms.sourcegitcommit: a03d79ca3f0774161a9f86a15528d36e1291acce
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83433030"
---
# <a name="what-are-the-q-programming-language-and-qdk"></a>Q# 프로그래밍 언어 및 QDK란?

Q#는 양자 알고리즘을 개발하고 실행하기 위한 Microsoft의 오픈 소스 프로그래밍 언어입니다. 이는 [Q# 라이브러리](xref:microsoft.quantum.libraries), [양자 시뮬레이터](xref:microsoft.quantum.machines), [다른 프로그래밍 환경용 확장](xref:microsoft.quantum.install) 및 [API 설명서](xref:microsoft.quantum.standardlibsintro)가 포함된 QDK(Qualument Development Kit)의 일부입니다. QDK에는 표준 Q# 라이브러리 외에도 화학, Machine Learning 및 숫자 라이브러리가 포함되어 있습니다.

프로그래밍 언어인 Q#은 Python, C# 및 F#에서 친숙한 요소를 가져오고 반복, if/then 문 및 공통 데이터 형식을 사용하여 프로그램을 작성하는 기본 절차 모델을 지원합니다. 또한 새로운 양자 관련 데이터 구조 및 연산도 소개합니다.

## <a name="what-can-i-do-with-the-qdk"></a>QDK에서 수행할 수 있는 작업은 무엇인가요?

완전한 기능을 갖춘 Q#용 개발 키트인 QDK는 일반적인 도구 및 언어와 함께 사용하여 다양한 환경에서 실행할 수 있는 양자 애플리케이션을 개발할 수 있습니다. Q# 프로그램은 Japyter Notebook을 통해 명령줄 앱으로 실행하거나 Python 또는 .NET 호스트 프로그램을 사용할 수 있습니다.

### <a name="develop-in-common-tools-and-environments"></a>일반적인 도구 및 환경에서 개발

양자 개발을 [Visual Studio, Visual Studio Code](xref:microsoft.quantum.install.standalone) 및 [Jupyter Notebook](xref:microsoft.quantum.install.jupyter)과 통합합니다. 기본 제공 API를 사용하여 프로그램을 [Python](xref:microsoft.quantum.install.python) 및 [.NET](xref:microsoft.quantum.install.cs) 호스트 언어와 페어링합니다.

### <a name="try-quantum-operations-and-domain-specific-libraries"></a>양자 연산 및 도메인별 라이브러리 사용해 보기

중첩, 얽힘 및 기타 양자 연산을 검색하는 양자 알고리즘을 작성하고 테스트합니다. Q# 라이브러리를 사용하면 하위 수준의 연산 순서를 설계하지 않고도 복잡한 양자 연산을 실행할 수 있습니다.

### <a name="run-programs-in-simulators"></a>시뮬레이터에서 프로그램 실행

전체 상태 양자 시뮬레이터, 제한된 범위의 Toffoli 시뮬레이터에서 양자 프로그램을 실행하거나 다른 리소스 예측 도구에서 Q# 코드를 테스트합니다. 

## <a name="where-can-i-learn-more"></a>자세한 내용을 알아보려면 어떤 정보를 참조해야 하나요?

|||
| ---- | ---- |
| **양자 컴퓨팅을 처음 접하는 경우** | [주요 개념](xref:microsoft.quantum.overview.understanding)에서 양자 물리학 및 양자 컴퓨팅에 대한 몇 가지 기본 사항을 검토합니다.|
| **Q# 언어에 대해 자세히 알아보려는 경우** | [Q# 사용자 가이드](xref:microsoft.quantum.guide)에서 형식, 식, 변수 및 양자 프로그램 구조를 살펴봅니다.|
| **양자 프로그램 작성을 시작하려는 경우** | Q# 환경을 설치하고, [빠른 시작](xref:microsoft.quantum.install)에서 양자 프로그램 작성을 시작합니다.|

## <a name="how-does-q-work"></a>Q#은 어떻게 작동하나요?

Q# 프로그램은 독립 실행형 명령줄 애플리케이션으로 컴파일하거나 Python 또는 .NET 언어로 작성된 호스트 프로그램에서 호출할 수 있습니다.

프로그램을 컴파일하고 실행하면 양자 시뮬레이터의 인스턴스가 만들어지고 Q# 코드가 전달됩니다. 시뮬레이터는 Q# 코드를 사용하여 큐비트를 만들고(양자 입자 시뮬레이션), 변환을 적용하여 해당 상태를 수정합니다. 그런 다음, 시뮬레이터의 양자 연산 결과가 프로그램에 반환됩니다.  

시뮬레이터에서 Q# 코드를 격리하면 알고리즘이 양자 물리학 법칙을 따르고 양자 컴퓨터에서 올바르게 실행될 수 있습니다.

![qsharp-code-flow](~/media/qsharp-code-flow.png)

## <a name="how-do-i-use-the-qdk"></a>QDK를 사용하려면 어떻게 할까요?

Q# 컴파일러, Q# 라이브러리 및 양자 시뮬레이터를 포함하여 Q# 프로그램을 작성하고 실행하는 데 필요한 모든 항목을 로컬 컴퓨터에서 설치하고 실행할 수 있습니다. 결국에는 실제 양자 컴퓨터에서 Q# 프로그램을 원격으로 실행할 수 있지만, 그 후에는 QDK에서 제공되는 양자 시뮬레이터에서 정확하고 신뢰할 수 있는 결과를 제공합니다.

- [명령줄에서 Q#을 실행](xref:microsoft.quantum.install.standalone)하는 것이 가장 빠른 시작 방법입니다.

- Q# 프로그램을 컴파일, 시뮬레이션 및 시각화하는 Jupyter 확장인 [IQ#을 사용하여 독립 실행형 Jupyter Notebook을 실행](xref:microsoft.quantum.install.jupyter)합니다.

- [Python](xref:microsoft.quantum.install.python)에 익숙한 경우 이를 호스트 프로그래밍 플랫폼으로 사용하여 시작할 수 있습니다. Python은 개발자뿐만 아니라 과학자, 연구원 및 교사 사이에서도 널리 사용되고 있습니다.

- 이미 [C#, F# 또는 VB.NET](xref:microsoft.quantum.install.cs)을 사용한 경험이 있고 Visual Studio 개발 환경에 익숙한 경우 Q#을 준비하려면 몇 가지 확장만 Visual Studio에 추가하면 됩니다.  

## <a name="summary"></a>요약

Q#은 양자 프로그램을 개발하기 위한 오픈 소스 프로그래밍 언어입니다. 여기에는 복합 양자 연산을 만들 수 있는 라이브러리 및 프로그램을 정확하게 실행하고 테스트할 수 있는 양자 시뮬레이터가 있습니다. Q# 프로그램은 독립 실행형 앱으로 실행되거나 Python 또는 .NET 호스트 프로그램에서 호출될 수 있으며 로컬 컴퓨터에서 작성, 실행 및 테스트할 수 있습니다.

## <a name="next-steps"></a>다음 단계

> [!div class="nextstepaction"]
> [양자 컴퓨팅을 위한 선형 대수](xref:microsoft.quantum.overview.algebra)
