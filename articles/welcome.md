---
uid: microsoft.quantum.welcome
title: QDK(Quantum Development Kit) 시작
description: Microsoft QDK(Quantum Development Kit)에서 Q#으로 양자 프로젝트 프로그래밍을 시작하는 방법을 알아봅니다.
author: natke
ms.author: nakersha
ms.date: 10/23/2019
ms.topic: overview
ms.openlocfilehash: cea39e47ec5e7e2ad97adbbb39ba586274564967
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "77907633"
---
# <a name="get-started-with-the-quantum-development-kit-qdk"></a>QDK(Quantum Development Kit) 시작

Microsoft Quantum Development Kit에 오신 것을 환영합니다!  
QDK에는 자체 양자 프로그램을 구축하고 양자 애플리케이션 개발을 위해 특별히 설계된 프로그래밍 언어인 Q#을 실험하는 데 필요한 모든 도구가 포함되어 있습니다. 

바로 들어가려면 [QDK 설치 가이드](xref:microsoft.quantum.install)로 이동합니다.
그런 다음, Windows, Linux 또는 MacOS 머신에 Quantum Development Kit를 설치하여 사용자가 직접 양자 프로그램을 작성할 수 있도록 안내합니다.

코딩을 시작할 준비가 되지 않았지만 양자 컴퓨팅 및 Q#에 대해 자세히 알아보려면 이 문서를 계속 읽어 잘 사용할 수 있도록 리소스에 대한 감각을 익히는 것이 좋습니다. [양자 컴퓨팅에 대한 5가지 질문](#five-questions-about-quantum-computing) 섹션에서 원하는 내용으로 정확히 연결되는 링크를 찾을 수 있습니다!

## <a name="get-started-programming"></a>프로그래밍 시작

Quantum Development Kit는 Q#을 사용하여 양자 프로그램을 개발하는 방법을 배울 수 있는 여러 가지 방법을 제공합니다.
양자의 기능을 시작 및 실행하기 위해 *빠른 시작*을 사용해 볼 수 있습니다.

* [양자 난수 생성기](xref:microsoft.quantum.quickstarts.qrng)는 몇 분 만에 양자 애플리케이션을 빌드하여 실행하면서 양자 개념을 간단히 소개하는 "Q# Hello World" 스타일 애플리케이션입니다.
* [Q#을 사용하는 양자 기본 사항](xref:microsoft.quantum.write-program)은 양자 프로그래밍의 기본적인 개념을 보여주는 Q# 프로그램 작성 방법을 안내합니다. 
    코딩을 시작할 준비가 되지 않은 경우에도 QDK를 설치하지 않고 자습서를 계속 따라 하면서 Q# 프로그래밍 언어와 양자 컴퓨팅의 첫 번째 개념에 대한 개요를 확인할 수 있습니다.
* [Grover 검색 알고리즘](xref:microsoft.quantum.quickstarts.search)은 낮은 수준의 양자 작업을 추상화하는 방식으로 양자 알고리즘을 표현하는 Q#의 기능을 파악할 수 있는 Q# 프로그램 예제를 제공합니다. 
    이 빠른 시작 가이드는 다양한 프로그래밍 환경(Python 호스트 또는 .NET 언어 호스트 및 Visual Studio 또는 Visual Studio Code 포함)을 사용하여 프로그램을 개발하는 방법을 안내합니다.

### <a name="learning-further"></a>자세히 알아보기
* Q# 프로그래밍에 대해 자세히 알아 보려면 Q#의 프로그래밍 연습을 통해 양자 컴퓨팅을 소개하는 자기 주도적 프로그래밍 연습 모음인 [Quantum Katas](https://github.com/Microsoft/QuantumKatas)를 확인하세요.
    이들 katas 대부분은 Q# Notebook으로도 사용할 수 있습니다. 
* [샘플 리포지토리](https://github.com/Microsoft/Quantum)는 Q#을 사용하여 양자 프로그램을 작성하는 방법에 대한 여러 예제를 소개합니다. 이러한 샘플의 대부분은 [표준](https://github.com/Microsoft/QuantumLibraries) 및 [화학](xref:microsoft.quantum.libraries.standard.intro) 라이브러리를 포함하여 오픈 소스 [양자 라이브러리](xref:microsoft.quantum.chemistry.concepts.intro)를 사용하여 작성되었습니다(자세한 내용은 아래 참조).

## <a name="five-questions-about-quantum-computing"></a>양자 컴퓨팅에 대한 5가지 질문

양자 개발이 처음인 경우 이 모든 것이 다소 어려워 보일 수 있습니다. 이에 양자 컴퓨팅 학습을 시작하는 데 도움이 되는 리소스를 제공합니다. 이러한 짧은 문서를 활용하면 프로그래밍을 바로 시작할 수 있을 것이라 확신합니다.
* [양자 컴퓨팅이란?](xref:microsoft.quantum.overview.what)
* [양자 컴퓨터에서 수행할 수 있는 작업은 무엇인가요?](xref:microsoft.quantum.overview.computers)
* [양자 컴퓨팅을 배워야 하는 이유는 무엇인가요?](xref:microsoft.quantum.overview.why)
* [Q#이란?](xref:microsoft.quantum.overview.qsharp)
* [Q#에서 양자 컴퓨팅을 배우려면 어떻게 해야 하나요?](xref:microsoft.quantum.overview.learn)

## <a name="quantum-development-kit-documentation"></a>Quantum Development Kit 설명서

현재 설명서에는 다음과 같은 추가 항목이 포함되어 있습니다.

### <a name="using-q"></a>Q# 사용
* [양자 개발 기술](xref:microsoft.quantum.techniques.intro)은 Q#에서 양자 프로그램을 만드는 데 사용되는 핵심 개념이 명시되어 있습니다. 항목에는 파일 구조, 작업 및 함수, 큐비트 사용 및 몇 가지 고급 항목이 포함되어 있습니다.
* [Q# 언어 참조](xref:microsoft.quantum.language.intro)는 형식 모델, 식, 문장 및 컴파일러 사용을 비롯한 Q# 언어에 대해 자세히 설명합니다.
* [양자 시뮬레이터 및 호스트 애플리케이션](xref:microsoft.quantum.machines) 양자 알고리즘을 실행하는 방법, 사용할 수 있는 양자 머신 및 양자 프로그램을 위한 비 Q# 드라이버를 작성하는 방법에 대해 설명합니다.

### <a name="q-libraries"></a>Q# 라이브러리
* [Q# 표준 라이브러리](xref:microsoft.quantum.libraries.standard.intro)는 기존 언어 제어 요구 사항과 Q# 양자 알고리즘을 모두 지원하는 작업 및 함수에 대해 설명합니다. 
    항목에는 제어 흐름, 데이터 구조, 오류 수정, 테스트 및 디버깅이 있습니다. 
* [Q# 화학 라이브러리](xref:microsoft.quantum.chemistry.concepts.intro)는 양자 컴퓨팅의 중요한 애플리케이션인 양자 화학 시뮬레이션을 지원하는 작업 및 함수에 대해 설명합니다. 항목에는 해밀턴 동역학 시뮬레이션 및 양자 단계 예측 등이 있습니다.
* [Q# 숫자 라이브러리](xref:microsoft.quantum.numerics.intro)는 대상 머신의 원시 작업에 관하여 복잡한 산술 함수를 표현하도록 지원하는 작업 및 함수에 대해 설명합니다.
* [Q# 라이브러리 참조](xref:microsoft.quantum.standardlibsintro)는 네임스페이스별 라이브러리 엔터티에 대한 참조 정보가 포함되어 있습니다.

### <a name="general-quantum-computing"></a>일반 양자 컴퓨팅
* [양자 컴퓨팅 개념](xref:microsoft.quantum.concepts.intro)에는 양자 컴퓨팅에 대한 선형 대수의 관련성, 큐비트의 특성 및 사용, 양자 회로 읽는 방법 등의 항목이 포함되어 있습니다.
* [양자 컴퓨팅 용어집](xref:microsoft.quantum.glossary)은 양자 컴퓨팅 및 프로그램 개발과 관련된 몇 가지 중요한 용어집입니다. 
    필드를 처음 접하는 경우 설명서를 읽을 때 이 용어집을 편리하게 참조할 수 있습니다.
* [추가 정보](xref:microsoft.quantum.more-information)에는 양자 컴퓨팅 항목을 심층적으로 다루기 위해 특별히 선정된 참조가 있습니다.

### <a name="additional-info"></a>추가 정보
* [Microsoft Quantum Development Kit 릴리스 정보](xref:microsoft.quantum.relnotes).


## <a name="be-a-part-of-the-q-open-source-community"></a>Q# 오픈 소스 커뮤니티의 일원되기
Quantum Development Kit는 세계에서 가장 어려운 문제 중 일부를 해결하기 위해 양자 컴퓨팅에 보다 쉽게 액세스할 수 있도록 개발자를 지원하는 오픈 소스 개발 키트입니다.  오픈 소스 소프트웨어가 필요한 교육 기관은 양자 학습 및 개발용으로 Q#을 배포할 수 있습니다. 또한 개발 키트를 오픈 소싱하면 개발자와 도메인 전문가가 코드를 통해 개선 사항과 아이디어를 제공할 수 있습니다.

Quantum Development Kit에 대한 피드백, 참여 및 기여가 중요합니다.  Quantum Development Kit 소스에 대해 자세히 알아보고, 피드백을 제공하고, 의사 결정에 참여하고 점점 커지는 이 양자 개발 플랫폼에 기여하는 방법을 알아 보려면 [Quantum Development Kit에 기여](xref:microsoft.quantum.contributing)를 참조하세요.

Microsoft의 양자 컴퓨팅 이니셔티브에 대해 보다 일반적인 정보가 필요한 경우 [Microsoft Quantum](https://www.microsoft.com/en-us/quantum/)을 참조하세요.
