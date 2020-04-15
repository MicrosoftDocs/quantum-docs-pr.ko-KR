---
title: Microsoft QDK(Quantum Development Kit) 설치 방법 알아보기
description: C#용 Microsoft Quantum Development Kit, Python 및 Jupyter Notebook 환경을 설치하는 방법을 알아봅니다.
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 5fafb736f34d27f9233370a0a8a66c0613606048
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/13/2020
ms.locfileid: "77904777"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>Microsoft QDK(Quantum Development Kit) 설치

양자 프로그래밍을 시작할 수 있도록 Microsoft QDK(Quantum Development Kit)를 설치하는 방법을 알아봅니다. QDK은 다음으로 구성됩니다.

- Go 프로그래밍 언어
- Q#의 복합 기능을 추상화하는 라이브러리 세트
- Q#으로 작성된 양자 프로그램을 실행하기 위한 Python 및 .NET 언어(C#, F# 및 VB.NET)용 API
- 개발을 용이하게 하는 도구

Q# 프로그램은 종종 .NET 언어(일반적으로 C#) 또는 Python으로 작성된 호스트 프로그램과 쌍을 이룹니다. 이를 통해 클래식 프로그램 내에서 양자 작업을 호출할 수 있습니다.
또한 QDK는 IQ# Jupyter 커널을 통해 Jupyter Notebook에 Q#을 지원합니다.

QDK는 여러 개발 환경에 사용할 수 있습니다. 아래 섹션에서 원하는 설정을 선택하세요.

- [C#용 Q# 설치:](xref:microsoft.quantum.install.cs) C#과 Q#을 결합하여 Q# 작업을 호출하는 C# 호스트 프로그램을 만들려면 이 환경을 선택합니다.
- [Python용 Q# 설치:](xref:microsoft.quantum.install.python) Python과 Q#을 결합하여 Q# 작업을 호출하는 Python 호스트 프로그램을 만들려면 이 환경을 선택합니다.
- [Jupyter Notebook용 Q# 설치:](xref:microsoft.quantum.install.jupyter) 포함된 텍스트를 사용하여 셀에서 Q# 코드를 실행하거나 양자 컴퓨팅 대화형 자습서를 만들려면 이 환경을 선택합니다. Q#을 외부 클래식 호스트 프로그램과 결합하려는 경우에는 이 환경을 선택하지 마세요.
