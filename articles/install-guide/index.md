---
title: Microsoft QDK(Quantum Development Kit) 설치
description: 다양한 환경에 Microsoft Quantum Development Kit를 설치하는 방법입니다.
author: natke
ms.author: nakersha
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 2041b90ba021b7640615d73c35841cc21f025ac0
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426465"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>Microsoft QDK(Quantum Development Kit) 설치

양자 프로그래밍을 시작할 수 있도록 Microsoft QDK(Quantum Development Kit)를 설치하는 방법을 알아봅니다. QDK은 다음으로 구성됩니다.

- Q# 프로그래밍 언어
- Q#의 복합 기능을 추상화하는 라이브러리 세트
- Q#으로 작성된 양자 프로그램을 실행하기 위한 Python 및 .NET 언어(C#, F# 및 VB.NET)용 API
- 개발을 용이하게 하는 도구

Q# 프로그램은 Visual Studio Code 또는 Visual Studio를 사용하거나 IQ# Jupyter 커널의 Jupyter Notebook을 통해 독립 실행형 애플리케이션으로 실행할 수 있습니다.

또한 .NET 언어(대개 C#) 또는 Python으로 작성된 호스트 프로그램과 쌍을 이룰 수 있으므로 기존 프로그램 내부에서 양자 연산을 호출할 수 있습니다.

QDK는 여러 개발 환경에 사용할 수 있습니다. 다음 중에서 원하는 설정을 선택하세요.

[**Q# 명령줄 애플리케이션으로 개발**](xref:microsoft.quantum.install.standalone) - 명령줄에서 Q#으로 작업하려면 이 방법을 선택합니다. 아래 옵션과 같이 드라이버나 호스트 프로그램이 필요하지 않습니다.

[**Q# Jupyter Notebook으로 개발**](xref:microsoft.quantum.install.jupyter) - 포함된 텍스트를 사용하여 셀에서 Q# 코드를 실행하거나 양자 컴퓨팅 대화형 자습서를 만들려면 이 환경을 선택합니다. 

[**Q# 및 Python으로 개발**](xref:microsoft.quantum.install.python) - Python과 Q#을 결합하여 Q# 연산을 호출하는 Python 호스트 프로그램을 만들 수 있습니다.

[**Q# 및 .NET으로 개발**](xref:microsoft.quantum.install.cs) - C#, F# 또는 VB.NET을 Q#과 결합하여 Q# 연산을 호출하는 .NET 호스트 프로그램을 만듭니다.
