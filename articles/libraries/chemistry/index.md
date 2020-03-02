---
title: 양자 화학 라이브러리 소개
description: Microsoft 양자 화학 라이브러리에 대한 내용 및 이 라이브러리를 사용하여 양자 컴퓨터에서 전자 구조 문제를 시뮬레이션하는 방법을 알아봅니다.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.intro
ms.openlocfilehash: 4268eafa5e53c0a026d179503ac6db88652a8f90
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907327"
---
# <a name="introduction-to-the-quantum-chemistry-library"></a><span data-ttu-id="7295d-103">양자 화학 라이브러리 소개</span><span class="sxs-lookup"><span data-stu-id="7295d-103">Introduction to the Quantum Chemistry Library</span></span>

<span data-ttu-id="7295d-104">물리적 시스템의 시뮬레이션은 양자 컴퓨팅에서 오랫 동안 중요한 역할을 수행해 왔습니다.</span><span class="sxs-lookup"><span data-stu-id="7295d-104">Simulation of physical systems has long played a central role in quantum computing.</span></span>  <span data-ttu-id="7295d-105">양자 동역학이 양자 컴퓨터에서 시뮬레이트하기 어려운 분야라고 널리 인식되어 왔기 때문입니다. 즉, 이 시스템의 시뮬레이트 복잡성은 양자 시스템 규모에 따라 기학급수적으로 높아집니다.</span><span class="sxs-lookup"><span data-stu-id="7295d-105">This is because quantum dynamics are widely believed to be intractable to simulate on quantum computers, meaning that the complexity of simulating the system scales exponentially with the size of the quantum system in question.</span></span>  <span data-ttu-id="7295d-106">화학 및 재료 과학의 시뮬레이트 문제점은 양자 컴퓨팅의 가장 유용한 응용 분야에서도 나타나며, 이로 인해 우리의 측정 또는 시뮬레이트 능력을 벗어나는 화학 반응 메커니즘을 분석해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7295d-106">Simulating problems in chemistry and material science remains perhaps the most evocative application of quantum computing and would allow us to probe chemical reaction mechanisms that hitherto were beyond our ability to measure or simulate.</span></span>  <span data-ttu-id="7295d-107">또한 고온의 초전도체와 같은 상호 연관된 전자 재료를 시뮬레이트해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7295d-107">It would also allow us to simulate correlated electronic materials such as high-temperature superconductors.</span></span> <span data-ttu-id="7295d-108">이 우주 내에서의 응용 범주는 광범위합니다.</span><span class="sxs-lookup"><span data-stu-id="7295d-108">The list of applications in this space is vast.</span></span>

<span data-ttu-id="7295d-109">이 설명서는 사용자들이 우주 내에서 해밀토니안 시뮬레이션 라이브러리의 여러 측면에 수행하는 역할을 이해하도록 지원하기 위해 양자 컴퓨터의 전자 구조 문제를 시뮬레이트하는 방법을 간단히 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="7295d-109">The purpose of this documentation is to provide a concise introduction to simulating electronic structure problems on quantum computers in order to help the reader understand the role that many aspects of the Hamiltonian simulation library play within the space.</span></span>  <span data-ttu-id="7295d-110">먼저 양자 메커니즘을 간략히 소개한 후, 전자 시스템이 모델링되는 방식을 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="7295d-110">We begin with a brief introduction to quantum mechanics and then proceed to discuss how electronic systems are modeled in it.</span></span>  <span data-ttu-id="7295d-111">그런 다음, 양자 컴퓨터를 사용하여 이러한 양자 동역할을 에뮬레이트하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="7295d-111">We will then discuss how such quantum dynamics can be emulated using a quantum computer.</span></span>  <span data-ttu-id="7295d-112">이 작업이 완료되면 양자 동역할을 기본 게이트 시퀀스로 컴파일하는 데 사용되는 다음 두 가지 방법을 설명할 것입니다. Trotter-Suzuki 분해 및 양자화</span><span class="sxs-lookup"><span data-stu-id="7295d-112">Once this is complete we will discuss two methods used to compile the quantum dynamics to sequences of elementary gates: Trotter-Suzuki decompositions and qubitization.</span></span>
