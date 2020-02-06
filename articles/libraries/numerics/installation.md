---
title: 숫자 라이브러리 설치 및 유효성 검사 | Microsoft Docs
description: 숫자 라이브러리 설치 및 유효성 검사
author: thomashaener
ms.author: thhaner
ms.date: 05/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.installation
ms.openlocfilehash: c41bb73ea484271689eea2ca1b59ce6639dc15a7
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036460"
---
# <a name="numerics-library-installation-and-validation"></a>숫자 라이브러리 설치 및 유효성 검사

퀀텀 개발 키트는 [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) NuGet 패키지를 통해 숫자 기능을 지원 합니다.

**Visual Studio > = 2019:** Visual Studio 2019 이상을 사용 하는 경우 NuGet 패키지 관리자를 사용 하 여 숫자 패키지를 추가할 수 있습니다.
이렇게 하려면 "NuGet 패키지 관리 ..."를 선택 합니다. Visual Studio의 "프로젝트" 메뉴 항목에서

찾아보기 탭에서 "Microsoft. 양자" 패키지 이름을 검색 합니다.

> [!NOTE]
> "시험판 포함"을 사용 해야 합니다.

그러면 다운로드할 수 있는 패키지가 나열 됩니다.
"Microsoft. 양자"를 가리키면 버전 번호 오른쪽에 아래쪽 화살표가 표시 됩니다.
숫자 패키지를 설치 하려면 화살표를 클릭 합니다.

자세한 내용은 [패키지 관리자 UI 가이드](https://docs.microsoft.com/nuget/tools/package-manager-ui)를 참조 하세요.

또는 패키지 관리자 콘솔을 사용 하 여 명령줄 인터페이스를 통해 숫자 라이브러리를 프로젝트에 추가할 수 있습니다.

![](../../media/vs2017-nuget-console-menu.png)

패키지 관리자 콘솔에서 다음을 실행 합니다.

```
Install-Package Microsoft.Quantum.Numerics
```

자세한 내용은 [패키지 관리자 콘솔 가이드](https://docs.microsoft.com/nuget/tools/package-manager-console)를 참조 하세요.

**명령줄 또는 Visual Studio Code:** 명령줄을 사용 하거나 Visual Studio Code 내에서 `dotnet` 명령을 사용 하 여 NuGet 패키지 참조를 프로젝트에 추가할 수 있습니다.

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```


## <a name="verifying-your-installation"></a>설치 확인

퀀텀 개발 키트의 나머지와 마찬가지로 숫자 라이브러리에는 최대한 빨리 시작 하는 데 도움이 되는 샘플이 포함 되어 있습니다.
이러한 예제를 사용 하 여 설치를 테스트 하려면 [주 샘플 리포지토리](https://github.com/Microsoft/Quantum) 를 복제 한 다음 샘플 중 하나를 실행 합니다.

[`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) 샘플을 실행 하려면 다음을 수행 합니다.

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics/CustomModAdd
dotnet run
```
