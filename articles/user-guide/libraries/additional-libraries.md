---
title: 추가 Q# 라이브러리 사용
description: Q#퀀텀 응용 프로그램에 라이브러리를 추가 하는 방법에 대해 알아봅니다.
author: cgranade
ms.author: chgranad
ms.date: 06/30/2020
ms.topic: article
uid: microsoft.quantum.libraries.using
no-loc:
- Q#
- $$v
ms.openlocfilehash: ef88ca765a394a7092eb0a60bf6f3615c082ef6a
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869582"
---
# <a name="using-additional-no-locq-libraries"></a>추가 Q# 라이브러리 사용

퀀텀 개발 키트는 프로젝트에 추가할 수 있는 _NuGet 패키지_ 를 통해 추가 도메인별 기능을 제공 합니다 Q# .

| Q#라이브러리  | NuGet 패키지 | 참고 |
|---------|---------|--------|
| [Q#표준 라이브러리](xref:microsoft.quantum.libraries.standard.intro) | [**Microsoft 양자 표준**](https://www.nuget.org/packages/Microsoft.Quantum.Standard) | 기본적으로 포함됨 |
| [양자 화학 라이브러리](xref:microsoft.quantum.chemistry.concepts.intro) | [**Microsoft.Quantum.Chemistry**](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) | |
| [양자 숫자 라이브러리](xref:microsoft.quantum.numerics.intro) | [**Microsoft 양자**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) | |
| [양자 기계 학습 라이브러리](xref:microsoft.quantum.libraries.machine-learning.intro) | [**Microsoft.Quantum.MachineLearning**](https://www.nuget.org/packages/Microsoft.Quantum.MachineLearning) | |

선호 하는 환경 및 호스트 언어와 함께 사용 하기 위해 퀀텀 개발 키트를 설치한 후에는 추가 설치 없이 개별 프로젝트에 라이브러리를 쉽게 추가할 수 있습니다 Q# .

> [!NOTE]
> 일부 Q# 라이브러리는 프로그램과 함께 작동 Q# 하거나 호스트 응용 프로그램과 통합 되는 추가 도구에서 제대로 작동할 수 있습니다.
> 예를 들어, [화학 라이브러리 설치 지침](xref:microsoft.quantum.chemistry.concepts.installation) 에서는 NWChem 계산 화학 플랫폼과 함께 [ **Microsoft 양자** 패키지](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) 를 사용 하는 방법과 `qdk-chem` 퀀텀 화학 데이터를 사용 하기 위한 명령줄 도구를 설치 하는 방법에 대해 설명 합니다.

## <a name="no-locq-command-line-applications-or-net-interopability"></a>[Q#명령줄 응용 프로그램 또는 .NET interopability](#tab/tabid-csproj)

**명령줄 또는 Visual Studio Code:** 명령줄을 사용 하거나 Visual Studio Code 내에서 명령을 사용 하 여 `dotnet` NuGet 패키지 참조를 프로젝트에 추가할 수 있습니다.
예를 들어, [**Microsoft 양자**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) 패키지를 추가 하려면 다음 명령을 실행 합니다.

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```

**Visual Studio:** Visual Studio 2019 이상을 사용 하는 경우 Q# NuGet 패키지 관리자를 사용 하 여 패키지를 더 추가할 수 있습니다.
패키지를 로드 하려면: 
1. Visual Studio에서 프로젝트를 열고 **프로젝트** 메뉴에서 **NuGet 패키지 관리 ...** 를 선택 합니다.

2. **찾아보기**를 클릭 하 고, **시험판 포함** 을 선택 하 고, 패키지 이름 "Microsoft. 양자"를 검색 합니다. 그러면 다운로드할 수 있는 패키지가 나열 됩니다.

3. **Microsoft. 양자** 를 마우스로 가리키고 버전 번호 오른쪽에 있는 아래쪽 화살표를 클릭 하 여 숫자 패키지를 설치 합니다.

자세한 내용은 [패키지 관리자 UI 가이드](https://docs.microsoft.com/nuget/tools/package-manager-ui)를 참조 하세요.

또는 패키지 관리자 콘솔을 사용 하 여 명령줄 인터페이스를 통해 숫자 라이브러리를 프로젝트에 추가할 수 있습니다.

![명령줄에서 패키지 관리자 콘솔 사용](~/media/vs2017-nuget-console-menu.png)

패키지 관리자 콘솔에서 다음을 실행 합니다.

```
Install-Package Microsoft.Quantum.Numerics
```

자세한 내용은 [패키지 관리자 콘솔 가이드](https://docs.microsoft.com/nuget/tools/package-manager-console)를 참조 하세요.

## <a name="ino-locq-notebooks"></a>[Q#전자 필기장](#tab/tabid-notebook)

Q# [ `%package` 매직 명령을](xref:microsoft.quantum.iqsharp.magic-ref.package)사용 하 여 I 노트북에서 추가 패키지를 사용할 수 있도록 만들 수 있습니다.
예를 들어 I 노트북에서 사용할 [**Microsoft 양자**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) 패키지를 추가 하려면 Q# 노트북 셀에서 다음 명령을 실행 합니다.

```
%package Microsoft.Quantum.Numerics
```

이 명령을 수행 하면 노트북 내의 모든 셀에서 패키지를 사용할 수 있습니다.
현재 작업 영역의 코드에서 패키지를 사용할 수 있도록 하려면 Q# 패키지를 추가한 후 작업 영역을 다시 로드 합니다.

```
%workspace reload
```

## <a name="python-interoperability"></a>[Python 상호 운용성](#tab/tabid-python)


메서드를 사용 하 여 Python 호스트 프로그램에서 추가 패키지를 사용할 수 있도록 만들 수 있습니다 [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp/qsharp.packages.packages) .
예를 들어 I 노트북에서 사용할 [**Microsoft 양자**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) 패키지를 추가 하려면 Q# 다음 Python 코드를 실행 합니다.

```python
import qsharp
qsharp.packages.add("Microsoft.Quantum.Numerics")
```

이 명령을 수행 하면를 Q# 사용 하 여 컴파일된 모든 코드에서 패키지를 사용할 수 있습니다 `qsharp.compile` .
현재 작업 영역의 코드에서 패키지를 사용할 수 있도록 하려면 Q# 패키지를 추가한 후 작업 영역을 다시 로드 합니다.

```python
qsharp.reload()
```

***
