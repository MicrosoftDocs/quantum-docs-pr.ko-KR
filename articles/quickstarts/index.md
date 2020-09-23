---
title: Microsoft QDK(Quantum Development Kit) 설정
description: 다양한 환경에 Microsoft Quantum Development Kit를 설치하는 방법을 알아봅니다.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 74b9b3d8f694072f5b5f4d0eb520263387de8919
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834485"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a>Microsoft QDK(Quantum Development Kit) 설정

퀀텀 프로그래밍을 시작할 수 있도록 사용자 환경에 맞게 Microsoft QDK(Quantum Development Kit)를 설정하는 방법을 알아봅니다. QDK은 다음으로 구성됩니다.

- Q# 프로그래밍 언어
- Q#의 복합 기능을 추상화하는 라이브러리 세트
- Q#으로 작성된 퀀텀 프로그램을 실행하기 위한 Python 및 .NET 언어(C#, F# 및 VB.NET)용 API
- 개발을 용이하게 하는 도구

Q# 프로그램은 Visual Studio Code 또는 Visual Studio를 사용하거나 IQ# Jupyter 커널의 Jupyter Notebook을 통해 독립 실행형 애플리케이션으로 실행하거나 Python 또는 .NET 언어(C#, F#)로 작성된 호스트 프로그램과 쌍을 이뤄 실행할 수 있습니다. [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/) 또는 [Docker](#use-the-qdk-with-docker)를 사용하여 Q# 프로그램을 온라인으로 실행할 수도 있습니다. 

## <a name="options-for-setting-up-the-qdk"></a>QDK를 설정하는 옵션

QDK는 세 가지 방법으로 사용할 수 있습니다.

- [QDK 로컬 설치](#install-the-qdk-locally)
- [QDK 온라인 사용](#use-the-qdk-online)
- [QDK Docker 이미지 사용](#use-the-qdk-with-docker)

## <a name="install-the-qdk-locally"></a>QDK 로컬 설치

대부분의 즐겨찾기 IDE에서 Q# 코드를 개발할 수 있을 뿐만 아니라 Q#를 Python 및 .NET(C#, F#)과 같은 다른 언어와 통합할 수 있습니다.

|&nbsp; | **VS Code<br>(2019 이상)**| **Visual Studio<br>(2019 이상)** | **Jupyter Notebook** | **명령줄**|
|:-----|:-----:|:-----:|:-----:|:-----:|
|**OS** |Windows, macOS, Linux |Windows만 |Windows, macOS, Linux |Windows, macOS, Linux |
|<br>**Q# 독립 실행형** |<br>[설치](xref:microsoft.quantum.install.standalone) |<br> [설치](xref:microsoft.quantum.install.standalone)  |<br> [설치](xref:microsoft.quantum.install.jupyter) |<br>[설치](xref:microsoft.quantum.install.standalone)|
|**Q# 및 Python** |[설치](xref:microsoft.quantum.install.python) |[설치](xref:microsoft.quantum.install.python) |[설치](xref:microsoft.quantum.install.jupyter) |[설치](xref:microsoft.quantum.install.python) |
|**Q# 및 .NET(C#, F#)**|[설치](xref:microsoft.quantum.install.cs) |[설치](xref:microsoft.quantum.install.cs)|&#10006; |[설치](xref:microsoft.quantum.install.cs) |

## <a name="use-the-qdk-online"></a>QDK 온라인 사용

다음과 같은 옵션으로 로컬에 아무 것도 설치하지 않고 Q# 코드를 개발할 수도 있습니다.

|리소스|장점|제한 사항|
|---|---|---|
|[**Visual Studio Codespaces**](xref:microsoft.quantum.install.standalone)|풍부한 온라인 개발 환경  |Azure 구독과 플랜 필요 |
|[**바인더**](xref:microsoft.quantum.install.binder) | 무료 온라인 Notebook 환경 |지속성 없음 |

## <a name="use-the-qdk-with-docker"></a>Docker와 함께 QDK 사용

ACI와 같이 Docker 이미지를 지원하는 서비스를 통해 로컬 Docker 설치 또는 클라우드에서 QDK Docker 이미지를 사용할 수 있습니다.

https://github.com/microsoft/iqsharp/#using-iq-as-a-container 에서 IQ# Docker 이미지를 다운로드할 수 있습니다. 

또한 Visual Studio Code 원격 개발 컨테이너와 함께 Docker를 사용하여 개발 환경을 빠르게 정의할 수 있습니다. VS Code 개발 컨테이너에 대한 자세한 내용은 https://github.com/microsoft/Quantum/tree/master/.devcontainer 를 참조하세요.

## <a name="next-steps"></a>다음 단계

이러한 각 설치 방법에 대한 워크플로는 [Q# 프로그램을 실행하는 방법](xref:microsoft.quantum.guide.host-programs)에서 설명하고 비교합니다.
