---
title: Microsoft Q# 표준 라이브러리 소개
description: 퀀텀 프로그램에서 사용되는 작업, 함수 및 데이터 형식을 정의하는 Microsoft Q# 표준 라이브러리에 대해 알아봅니다.
author: QuantumWriter
ms.author: martinro
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.libraries.standard.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 63709015a12a7f972a676018970143ca163e92d0
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90836015"
---
# <a name="introduction-to-the-no-locq-standard-libraries"></a>Q# 표준 라이브러리 소개

Q#은 Q# *표준 라이브러리*를 구성하는 다양한 유용한 연산, 함수 및 사용자 정의 형식에 의해 지원됩니다.
[설치 및 유효성 검사](xref:microsoft.quantum.install) 중에 설치되는 [`Microsoft.Quantum.Development.Kit` NuGet 패키지](https://www.nuget.org/packages/microsoft.quantum.development.kit)는 Q# 컴파일러 및 대상 컴퓨터에서 구현되는 표준 라이브러리의 일부를 제공합니다.
[`Microsoft.Quantum.Standard` 패키지](https://www.nuget.org/packages/microsoft.quantum.standard)는 대상 컴퓨터에서 이식 가능한 Q# 표준 라이브러리의 일부를 제공합니다.

Q# 표준 라이브러리에서 정의되는 기호는 [API 설명서](xref:microsoft.quantum.apiref-intro)에서 훨씬 더 광범위하고 자세하게 정의됩니다.

다음 섹션에서는 각 표준 라이브러리 부분에서 가장 두드러진 몇 가지 기능을 간략하게 설명하고 각 기능을 사용하는 방법에 대한 몇 가지 컨텍스트를 제공합니다.
