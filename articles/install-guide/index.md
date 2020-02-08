---
title: Microsoft QDK(Quantum Development Kit) 설치 방법 알아보기
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 0e9dd1c74316eeb1fa7bbbf657d2e78231ee4294
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036511"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="57949-102">Microsoft QDK(Quantum Development Kit) 설치</span><span class="sxs-lookup"><span data-stu-id="57949-102">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="57949-103">양자 프로그래밍을 시작할 수 있도록 Microsoft QDK(Quantum Development Kit)를 설치하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="57949-103">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="57949-104">QDK은 다음으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="57949-104">The QDK consists of:</span></span>

- <span data-ttu-id="57949-105">Go 프로그래밍 언어</span><span class="sxs-lookup"><span data-stu-id="57949-105">the Q# programming language</span></span>
- <span data-ttu-id="57949-106">Q#의 복합 기능을 추상화하는 라이브러리 세트</span><span class="sxs-lookup"><span data-stu-id="57949-106">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="57949-107">Q#으로 작성된 양자 프로그램을 실행하기 위한 Python 및 .NET 언어(C#, F# 및 VB.NET)용 API</span><span class="sxs-lookup"><span data-stu-id="57949-107">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="57949-108">개발을 용이하게 하는 도구</span><span class="sxs-lookup"><span data-stu-id="57949-108">tools to facilitate your development</span></span>

<span data-ttu-id="57949-109">Q# 프로그램은 종종 .NET 언어(일반적으로 C#) 또는 Python으로 작성된 호스트 프로그램과 쌍을 이룹니다.</span><span class="sxs-lookup"><span data-stu-id="57949-109">Q# programs are often paired with a host program written in a .NET language (typically C#) or Python.</span></span> <span data-ttu-id="57949-110">이를 통해 클래식 프로그램 내에서 양자 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57949-110">This allows us to call quantum operations from inside a classical program.</span></span>
<span data-ttu-id="57949-111">또한 QDK는 IQ# Jupyter 커널을 통해 Jupyter Notebook에 Q#을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57949-111">In addition, the QDK provides Q# support for Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="57949-112">QDK는 여러 개발 환경에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57949-112">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="57949-113">아래 섹션에서 원하는 설정을 선택하세요.</span><span class="sxs-lookup"><span data-stu-id="57949-113">Select your preferred setup from the sections below:</span></span>

- <span data-ttu-id="57949-114">[C#용 Q# 설치:](xref:microsoft.quantum.install.cs) C#과 Q#을 결합하여 Q# 작업을 호출하는 C# 호스트 프로그램을 만들려면 이 환경을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="57949-114">[Install Q# for C#:](xref:microsoft.quantum.install.cs) choose this environment if you want to combine C# and Q# to create a C# host program that calls Q# operations.</span></span>
- <span data-ttu-id="57949-115">[Python용 Q# 설치:](xref:microsoft.quantum.install.python) Python과 Q#을 결합하여 Q# 작업을 호출하는 Python 호스트 프로그램을 만들려면 이 환경을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="57949-115">[Install Q# for Python:](xref:microsoft.quantum.install.python) choose this environment if you want to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>
- <span data-ttu-id="57949-116">[Jupyter Notebook용 Q# 설치:](xref:microsoft.quantum.install.jupyter) 포함된 텍스트를 사용하여 셀에서 Q# 코드를 실행하거나 양자 컴퓨팅 대화형 자습서를 만들려면 이 환경을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="57949-116">[Install Q# for Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) choose this environment to execute Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> <span data-ttu-id="57949-117">Q#을 외부 클래식 호스트 프로그램과 결합하려는 경우에는 이 환경을 선택하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="57949-117">Do not choose this environment if you want to combine Q# with an external classical host program.</span></span>
