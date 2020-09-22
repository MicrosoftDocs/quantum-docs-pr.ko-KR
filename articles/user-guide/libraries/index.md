---
title: Quantum Development Kit 라이브러리
description: Microsoft Quantum Development Kit에 포함된 표준, 화학 및 숫자 라이브러리의 개요입니다.
author: cgranade
ms.author: chgranad
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries
no-loc:
- Q#
- $$v
ms.openlocfilehash: 90672b6ec78bf8305bdb3ab8326002cf8ce34bfe
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835726"
---
# <a name="overview-of-no-locq-libraries"></a><span data-ttu-id="41925-103">Q# 라이브러리 개요</span><span class="sxs-lookup"><span data-stu-id="41925-103">Overview of Q# Libraries</span></span>
<span data-ttu-id="41925-104">Quantum Development Kit에는 Q#에서 퀀텀 애플리케이션을 더 쉽게 개발할 수 있도록 여러 라이브러리가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="41925-104">The Quantum Development Kit is provided with several libraries to make it easier to develop quantum applications in Q#.</span></span>
<span data-ttu-id="41925-105">설명서의 다음 섹션에서는 이러한 라이브러리와 프로그램에서 해당 라이브러리를 사용하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="41925-105">In this section of the documentation, we describe these libraries and how to use them in your programs.</span></span>

- <span data-ttu-id="41925-106">[**표준 라이브러리**](xref:microsoft.quantum.libraries.standard.intro): 이 섹션에서는 Q# 프로그램과 대상 머신 간의 인터페이스를 정의하는 도입부(prelude) 및 Q# 프로그램 작성에 사용할 범용 연산과 함수를 제공하는 Q# 라이브러리인 Canon에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="41925-106">[**Standard libraries**](xref:microsoft.quantum.libraries.standard.intro): This section describes the prelude, which defines the interface between Q# programs and target machines, and the canon, a Q# library that provides general-purpose operations and functions for use in writing Q# programs.</span></span>
- <span data-ttu-id="41925-107">[**양자 화학 라이브러리**](xref:microsoft.quantum.chemistry.concepts.intro): 이 섹션에서는 페르미온 해밀턴의 표현 및 이러한 표현에 대해 작동하는 양자 시뮬레이션 연산과 함수를 로드하기 위한 데이터 모델을 제공하는 양자 화학 라이브러리에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="41925-107">[**Quantum chemistry library**](xref:microsoft.quantum.chemistry.concepts.intro): This section describes the quantum chemistry library, which provides a data model for loading representations of fermionic Hamiltonians and quantum simulation operations and functions which act on these representations.</span></span>
- <span data-ttu-id="41925-108">[**양자 숫자 라이브러리**](xref:microsoft.quantum.numerics.intro): 이 섹션에서는 많은 수학 함수를 구현하는 양자 숫자 라이브러리에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="41925-108">[**Quantum numerics library**](xref:microsoft.quantum.numerics.intro): This section describes the quantum numerics library, which provides implementations for a host of mathematical functions.</span></span> <span data-ttu-id="41925-109">정수(부호 있음 및 부호 없음) 및 고정 소수점 표현을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="41925-109">It supports integer (signed & unsigned) and fixed-point representations.</span></span>
- <span data-ttu-id="41925-110">[**양자 기계 학습 라이브러리**](xref:microsoft.quantum.machine-learning.concepts.intro): 이 섹션에서는 퀀텀 컴퓨팅을 활용하여 데이터를 활용하는 순차 분류자를 구현하는 양자 기계 학습 라이브러리에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="41925-110">[**Quantum machine learning library**](xref:microsoft.quantum.machine-learning.concepts.intro): This section describes the quantum machine learning library, which provides an implementation of the sequential classifiers that take advantage of quantum computing to understand data.</span></span>

<span data-ttu-id="41925-111">라이브러리 원본과 코드 샘플은 GitHub에서 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41925-111">Sources of the libraries as well as code samples can be obtained from GitHub.</span></span>
<span data-ttu-id="41925-112">자세한 내용은 [라이선스](xref:microsoft.quantum.libraries.licensing)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="41925-112">See [Licensing](xref:microsoft.quantum.libraries.licensing) for further information.</span></span> <span data-ttu-id="41925-113">패키지 참조("이진 파일")는 라이브러리에 대해서도 사용할 수 있으며 라이브러리를 프로젝트에 포함하는 다른 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="41925-113">Note that package references ("binaries") are available also for the libraries and offer another way of including the libraries in projects.</span></span>
<span data-ttu-id="41925-114">[NuGet](https://nuget.org)을 통해 편리하게 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41925-114">A convenient way of obtaining them is via [NuGet](https://nuget.org).</span></span>
