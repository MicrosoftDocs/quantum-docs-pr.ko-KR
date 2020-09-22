---
title: 양자 기계 학습 패키지 소개 | Microsoft Docs
description: 양자 기계 학습 패키지 소개
author: QuantumWriter
ms.author: alexeib
ms.date: 12/5/2019
ms.topic: article
uid: microsoft.quantum.machine-learning.concepts.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 321901a7976e4633a672495827c27c5f1645ad30
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835692"
---
# <a name="introduction-to-the-quantum-machine-learning-library"></a><span data-ttu-id="9baaf-103">양자 기계 학습 라이브러리 소개</span><span class="sxs-lookup"><span data-stu-id="9baaf-103">Introduction to the Quantum Machine Learning Library</span></span>

<span data-ttu-id="9baaf-104">Quantum Machine Learning 라이브러리는 Q#으로 작성된 API로, 하이브리드 퀀텀/클래식 기계 학습 실험을 실행하는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9baaf-104">The Quantum Machine Learning Library is an API, written in Q#, that gives you the ability to run hybrid quantum/classical machine learning experiments.</span></span> <span data-ttu-id="9baaf-105">이 라이브러리는 다음을 수행할 수 있는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9baaf-105">The library gives you the ability to:</span></span>

- <span data-ttu-id="9baaf-106">사용자 고유의 데이터를 로드하여 양자 시뮬레이터 분류</span><span class="sxs-lookup"><span data-stu-id="9baaf-106">Load your own data to classify with quantum simulators</span></span>

- <span data-ttu-id="9baaf-107">샘플 및 자습서를 사용하여 양자 기계 학습 분야 학습</span><span class="sxs-lookup"><span data-stu-id="9baaf-107">Use samples and tutorials to get introduced to the field of quantum machine learning</span></span>

<span data-ttu-id="9baaf-108">현존하는 클래식 기계 학습 프레임워크에 비해 성능이 낮을 것으로 예상할 수 있습니다(이미 컴퓨팅 비용이 많이 드는 양자 디바이스 시뮬레이션을 기반으로 모든 것이 실행되므로).</span><span class="sxs-lookup"><span data-stu-id="9baaf-108">You can expect low performance compared to current classical machine learning frameworks (remember that everything is running on top of the simulation of a quantum device that is already computationally expensive).</span></span>

<span data-ttu-id="9baaf-109">이 설명서의 목적은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9baaf-109">The purpose of this documentation is:</span></span>

- <span data-ttu-id="9baaf-110">하이브리드 양자/클래식 학습을 위한 기계 학습 도구(Q\#으로 작성)를 간단하게 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="9baaf-110">A concise introduction to machine learning tools (written in Q\#) for hybrid quantum/classical learning.</span></span>
- <span data-ttu-id="9baaf-111">기계 학습 개념, 특히 양자 회로 중심 분류자(양자 순차 분류자라고도 함)의 실현을 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="9baaf-111">Introduce machine learning concepts and specifically their realization in quantum circuit centric classifiers (also known as quantum sequential classifiers).</span></span>
- <span data-ttu-id="9baaf-112">라이브러리에서 제공하는 도구를 사용하기 위한 기본 사항을 알려주는 일련의 자습서를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9baaf-112">Provide a set of tutorials on the basics to start using the tools provided by the library.</span></span>
- <span data-ttu-id="9baaf-113">이러한 분류자의 학습 및 유효성 검사 메서드 및 메서드를 라이브러리에서 제공하는 특정 Q\# 작업으로 변환하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="9baaf-113">Discuss the training and validation methods for such classifiers and how they translate into specific Q\# operations provided by the library.</span></span>

<span data-ttu-id="9baaf-114">이 라이브러리에 구현된 모델은 [회로 중심 양자 분류자](https://arxiv.org/abs/1804.00633)에 제공되는 양자-클래식 학습 체계를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="9baaf-114">The model implemented in this library is based on the quantum-classical training scheme presented in [Circuit-centric quantum classifiers](https://arxiv.org/abs/1804.00633)</span></span>
