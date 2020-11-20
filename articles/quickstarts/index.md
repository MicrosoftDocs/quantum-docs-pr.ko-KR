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
ms.openlocfilehash: f0c3df1998f9b64ff6544867b83a7afe52b6f46d
ms.sourcegitcommit: fd57a845d013ae4578715d04b1ed1edc1c8ff6b4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/18/2020
ms.locfileid: "94870824"
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

<table>
    <tr>
        <th width=10%>&nbsp;</th>
        <th>&nbsp;</th>
        <th align="center" width=18%><img src="~/media/vs_code.png" alt="VS Code" width="50"/><br><b>VS 코드<br>(2019 이상)</b></th>
        <th align="center" width=18%><img src="~/media/vs_studio.png" alt="VS Studio" width="50"/><br><b>VS Studio<br>(2019 이상)</b></th>
        <th align="center" width=18%><img src="~/media/jupyter-wht.png" alt="jupyter install" width="65"/><br><b>Jupyter Notebook</b></th>
        <th align="center" width=18%><img src="~/media/blank.png" alt="blank spacer" width="65"/><br><b>명령줄</b></th>
    </tr>
    <tr>
        <th>&nbsp;</th>
        <td align="left"><b>OS 지원:</b></td>
        <td align="center">Windows, macOS, Linux</td>
        <td align="center">Windows만</td>
        <td align="center">Windows, macOS, Linux</td>
        <td align="center">Windows, macOS, Linux</td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/quantum-wht.png" alt="QDK" width="60"/></td>
        <td align="left"><b>Q# 독립 실행형</b></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">설치</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">설치</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.jupyter">설치</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">설치</a></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/python.png" alt="python install" width="50"/></td>
        <td align="left"><b>Q# 및 Python</b></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">설치</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">설치</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.jupyter">설치</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">설치</a></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/dot_net.png" alt="dotnet install" width="50"/></td>
        <td align="left"><b>Q# 및 .NET(C#, F#)</b></td> 
        <td align="center"><a href="xref:microsoft.quantum.install.cs">설치</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.cs">설치</a></td>
        <td align="center">&#10006;</td>
        <td align="center"><a href="xref:microsoft.quantum.install.cs">설치</a></td>
   </tr>
</table>

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
