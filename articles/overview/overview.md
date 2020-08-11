---
title: 양자 컴퓨팅 소개
description: 양자 컴퓨팅이란 무엇인지, 양자 컴퓨터로 무엇을 할 수 있는지, 양자 컴퓨팅을 배우려면 어떻게 해야 하는지 알아봅니다.
author: bradben
ms.author: bradben
ms.date: 05/05/2020
ms.topic: overview
uid: microsoft.quantum.overview.introduction
no-loc:
- Q#
- $$v
ms.openlocfilehash: 59cb595ac207d6e84358fc6ba742e0e0019c76f9
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87866981"
---
# <a name="introduction-to-quantum-computing-and-the-quantum-development-kit"></a><span data-ttu-id="6bb34-103">양자 컴퓨팅 및 Quantum Development Kit 소개</span><span class="sxs-lookup"><span data-stu-id="6bb34-103">Introduction to quantum computing and the Quantum Development Kit</span></span>

<span data-ttu-id="6bb34-104">Microsoft QDK(Quantum Development Kit)는 개발자가 양자 알고리즘을 학습하고 양자 프로그램을 작성할 수 있도록 설계된 오픈 소스 도구 세트입니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-104">The Microsoft Quantum Development Kit (QDK) is a set of open-source tools designed to help developers learn quantum algorithms and write quantum programs.</span></span> <span data-ttu-id="6bb34-105">양자 컴퓨팅은 환경, 농업, 의료, 에너지, 기후, 재료 과학 및 아직 접하지 않은 다른 분야에서 지구의 가장 큰 도전 과제 중 일부를 해결할 것이라고 약속하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-105">Quantum computing holds the promise to solve some of our planet's biggest challenges - in the areas of environment, agriculture, health, energy, climate, materials science, and others we haven't encountered yet.</span></span>  

<span data-ttu-id="6bb34-106">이러한 문제 중 일부는 가장 강력한 컴퓨터에도 문제가 발생한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-106">For some of these problems, even our most powerful computers run into problems.</span></span> <span data-ttu-id="6bb34-107">양자 기술은 이제 막 컴퓨팅 세계에 영향을 미치기 시작했지만, 컴퓨팅에 대해 생각하는 방식을 광범위하게 변화시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-107">While quantum technology is just beginning to impact the computing world, it could be far-reaching and change the way we think about computing.</span></span>

## <a name="what-is-quantum-computing"></a><span data-ttu-id="6bb34-108">양자 컴퓨팅이란?</span><span class="sxs-lookup"><span data-stu-id="6bb34-108">What is quantum computing?</span></span>

<span data-ttu-id="6bb34-109">현대의 언어 용법에서 양자라는 단어는 일반적으로 원자 또는 아원자 입자의 속성을 가리키는 모든 물리적 속성에서 가능한 가장 작은 개별 단위를 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-109">In modern usage, the word quantum means the smallest possible discrete unit of any physical property, usually referring to properties of atomic or subatomic particles.</span></span> <span data-ttu-id="6bb34-110">양자 컴퓨터는 실제 양자 입자, 인공 원자 또는 양자 입자의 집합적 속성을 처리 단위로 사용하며, 크고 복잡하며 비용이 많이 드는 디바이스입니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-110">Quantum computers use actual quantum particles, artificial atoms, or collective properties of quantum particles as processing units, and are large, complex, and expensive devices.</span></span>

<span data-ttu-id="6bb34-111">양자 물리학의 고유한 동작을 활용하여 이를 컴퓨팅에 적용하면 양자 컴퓨터에서 새로운 개념을 기존 프로그래밍 방식에 도입하여 중첩, 얽힘, 양자 간섭과 같은 양자 물리학적 동작을 활용합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-111">Harnessing the unique behavior of quantum physics and applying it to computing, quantum computers introduce new concepts to traditional programming methods, making use of quantum physics behaviors such as superposition, entanglement, and quantum interference.</span></span>

## <a name="what-can-a-quantum-computer-do"></a><span data-ttu-id="6bb34-112">양자 컴퓨터에서 수행할 수 있는 작업은 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="6bb34-112">What can a quantum computer do?</span></span>

<span data-ttu-id="6bb34-113">양자 컴퓨터는 모든 작업을 더 빠르게 수행할 수 있는 슈퍼 컴퓨터가 아니지만, 양자 컴퓨터가 매우 효율적으로 작동하는 몇 가지 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-113">A quantum computer isn't a supercomputer that can do everything faster, but there are a few areas where quantum computers do exceptionally well.</span></span>

- [<span data-ttu-id="6bb34-114">양자 시뮬레이션</span><span class="sxs-lookup"><span data-stu-id="6bb34-114">Quantum simulation</span></span>](xref:microsoft.quantum.overview.introduction#quantum-simulation)
- [<span data-ttu-id="6bb34-115">암호화</span><span class="sxs-lookup"><span data-stu-id="6bb34-115">Cryptography</span></span>](xref:microsoft.quantum.overview.introduction#cryptography-and-shors-algorithm)
- [<span data-ttu-id="6bb34-116">검색</span><span class="sxs-lookup"><span data-stu-id="6bb34-116">Search</span></span>](xref:microsoft.quantum.overview.introduction#search-and-grovers-algorithm)
- [<span data-ttu-id="6bb34-117">최적화</span><span class="sxs-lookup"><span data-stu-id="6bb34-117">Optimization</span></span>](xref:microsoft.quantum.overview.introduction#quantum-inspired-computing-and-optimization)
- [<span data-ttu-id="6bb34-118">기계 학습</span><span class="sxs-lookup"><span data-stu-id="6bb34-118">Machine learning</span></span>](xref:microsoft.quantum.overview.introduction#quantum-machine-learning)

## <a name="quantum-simulation"></a><span data-ttu-id="6bb34-119">양자 시뮬레이션</span><span class="sxs-lookup"><span data-stu-id="6bb34-119">Quantum simulation</span></span>

<span data-ttu-id="6bb34-120">양자 컴퓨터는 계산에서 양자 현상을 사용하므로 다른 양자 시스템을 모델링하는 데 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-120">Since quantum computers use quantum phenomena in computation, they are well suited for modeling other quantum systems.</span></span> <span data-ttu-id="6bb34-121">광합성, 초전도체 그리고 복합 분자 형성은 양자 프로그램에서 시뮬레이션할 수 있는 양자 메커니즘의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-121">Photosynthesis, superconductivity, and complex molecular formations are examples of quantum mechanisms that quantum programs can simulate.</span></span>

## <a name="cryptography-and-shors-algorithm"></a><span data-ttu-id="6bb34-122">암호화 및 Shor 알고리즘</span><span class="sxs-lookup"><span data-stu-id="6bb34-122">Cryptography and Shor’s algorithm</span></span>

<span data-ttu-id="6bb34-123">1994년 Peter Shor는 확장 가능한 양자 컴퓨터에서 RSA 알고리즘과 같이 널리 사용되는 암호화 기술을 해제할 수 있음을 보여 주었습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-123">In 1994, Peter Shor showed that a scalable quantum computer could break widely used encryption techniques such as the RSA algorithm.</span></span> <span data-ttu-id="6bb34-124">클래식 암호화는 정수 인수 분해 또는 이산 로그와 같이 다루기 힘든 문제의 영향을 받으며, 이 중 상당 부분은 양자 컴퓨터를 사용하여 더 효율적으로 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-124">Classical cryptography relies on the intractability of problems such as integer factorization or discrete logarithms, many of which can be solved more efficiently using quantum computers.</span></span>

## <a name="search-and-grovers-algorithm"></a><span data-ttu-id="6bb34-125">검색 및 Grover 알고리즘</span><span class="sxs-lookup"><span data-stu-id="6bb34-125">Search and Grover’s algorithm</span></span>

<span data-ttu-id="6bb34-126">1996년 Lov Grover는 비정형 데이터를 검색하는 솔루션의 속도를 획기적으로 높여 클래식 알고리즘보다 더 적은 수의 단계로 검색을 실행하는 양자 알고리즘을 개발했습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-126">In 1996, Lov Grover developed a quantum algorithm that dramatically sped up the solution to unstructured data searches, running the search in fewer steps than any classical algorithm could.</span></span>

## <a name="quantum-inspired-computing-and-optimization"></a><span data-ttu-id="6bb34-127">양자 유도 컴퓨팅 및 최적화</span><span class="sxs-lookup"><span data-stu-id="6bb34-127">Quantum-inspired computing and optimization</span></span>

<span data-ttu-id="6bb34-128">양자 유도 알고리즘은 속도와 정확도를 높이기 위해 양자 원리를 사용하지만 클래식 컴퓨터 시스템에서 구현됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-128">Quantum-inspired algorithms use quantum principles for increased speed and accuracy but implement on classical computer systems.</span></span> <span data-ttu-id="6bb34-129">이 접근 방식을 통해 개발자는 아직 새로운 산업인 양자 하드웨어를 기다리지 않고도 오늘날 새로운 양자 기술의 강력한 기능을 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-129">This approach allows developers to leverage the power of new quantum techniques today without waiting for quantum hardware, which is still an emerging industry.</span></span>

<span data-ttu-id="6bb34-130">최적화는 원하는 결과와 제약 조건을 고려하여 문제에 대한 최상의 솔루션을 찾는 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-130">Optimization is the process of finding the best solution to a problem, given its desired outcome and constraints.</span></span> <span data-ttu-id="6bb34-131">비용, 품질 또는 생산 시간과 같은 요소는 모두 산업과 과학의 중요한 결정에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-131">Factors such as cost, quality, or production time all play into critical decisions made by industry and science.</span></span> <span data-ttu-id="6bb34-132">오늘날의 클래식 컴퓨터에서 실행되는 양자 유도 최적화 알고리즘은 지금까지 불가능했던 솔루션을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-132">Quantum-inspired optimization algorithms running on today's classical computers can find solutions that up to now have not been possible.</span></span> <span data-ttu-id="6bb34-133">혼잡을 줄이기 위해 교통 흐름을 최적화하는 것 외에도 비행기 탑승구 할당, 패키지 배송, 작업 예약 등이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-133">In addition to optimizing traffic flow to reduce congestion, there is airplane gate assignment, package delivery, job scheduling and more.</span></span> <span data-ttu-id="6bb34-134">재료 과학의 획기적인 발전을 통해 새로운 형태의 에너지, 더 큰 용량의 배터리, 더 가볍고 내구성이 뛰어난 재료가 나타날 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-134">With breakthroughs in materials science, there will be new forms of energy, batteries with larger capacity, and lighter and more durable materials.</span></span>

> [!NOTE]
> <span data-ttu-id="6bb34-135">Microsoft 양자 유도 컴퓨팅을 [재료 과학](https://cloudblogs.microsoft.com/quantum/2020/01/21/oti-lumionics-accelerating-materials-design-microsoft-azure-quantum/), [위험 관리](https://cloudblogs.microsoft.com/quantum/2019/05/22/microsoft-quantum-collaborates-with-willis-towers-watson-to-transform-risk-management-solutions/) 및 [의학](https://blogs.microsoft.com/blog/2018/05/18/microsoft-quantum-helps-case-western-reserve-university-advance-mri-research/) 분야에서 사용하는 방법에 대해 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="6bb34-135">Read more about how Microsoft quantum-inspired computing is being used in [materials science](https://cloudblogs.microsoft.com/quantum/2020/01/21/oti-lumionics-accelerating-materials-design-microsoft-azure-quantum/), [risk management](https://cloudblogs.microsoft.com/quantum/2019/05/22/microsoft-quantum-collaborates-with-willis-towers-watson-to-transform-risk-management-solutions/), and [medicine](https://blogs.microsoft.com/blog/2018/05/18/microsoft-quantum-helps-case-western-reserve-university-advance-mri-research/).</span></span>

## <a name="quantum-machine-learning"></a><span data-ttu-id="6bb34-136">양자 기계 학습</span><span class="sxs-lookup"><span data-stu-id="6bb34-136">Quantum machine learning</span></span>

<span data-ttu-id="6bb34-137">클래식 컴퓨터의 기계 학습은 과학과 비즈니스의 세계를 혁신적으로 변화시키고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-137">Machine learning on classical computers is revolutionizing the world of science and business.</span></span> <span data-ttu-id="6bb34-138">그러나 모델 학습에 들어가는 높은 계산 비용은 이 분야의 개발 및 범위를 넓히는 데 방해가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-138">However, the high computational cost of training the models hinders the development and scope of the field.</span></span> <span data-ttu-id="6bb34-139">양자 기계 학습 영역은 클래식 컴퓨터보다 더 빠르게 실행되는 기계 학습을 가능하게 하는 양자 소프트웨어를 고안하고 구현하는 방법을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-139">The area of quantum machine learning explores how to devise and implement quantum software that enables machine learning that runs faster than classical computers.</span></span>

<span data-ttu-id="6bb34-140">Quantum Development Kit는 하이브리드 양자/클래식 기계 학습 실험을 실행할 수 있는 [양자 기계 학습 라이브러리](xref:microsoft.quantum.machine-learning.concepts.intro)와 함께 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-140">The Quantum Development Kit comes with the [quantum machine learning library](xref:microsoft.quantum.machine-learning.concepts.intro) that gives you the ability to run hybrid quantum/classical machine learning experiments.</span></span> <span data-ttu-id="6bb34-141">이 라이브러리는 샘플과 자습서를 포함하고 있으며, 감독된 분류 문제를 해결하기 위해 새 하이브리드 양자 클래식 알고리즘인 회로 중심 양자 분류자를 구현하는 데 필요한 도구를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-141">The library includes samples and tutorials, and provides the necessary tools to implement a new hybrid quantum–classical algorithm, the circuit-centric quantum classifier, to solve supervised classification problems.</span></span>

## <a name="no-locq-and-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="6bb34-142">Q# 및 Microsoft QDK(Quantum Development Kit)</span><span class="sxs-lookup"><span data-stu-id="6bb34-142">Q# and the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="6bb34-143">Q#은 퀀텀 알고리즘을 개발하고 실행하기 위한 Microsoft의 오픈 소스 프로그래밍 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-143">Q# is Microsoft's open-source programming language for developing and running quantum algorithms.</span></span> <span data-ttu-id="6bb34-144">완전한 기능을 갖춘 Q#용 개발 키트인 [QDK](https://docs.microsoft.com/quantum/)의 일부로서, 표준 도구 및 언어와 함께 사용하여 다양한 환경에서 실행할 수 있는 퀀텀 애플리케이션(기본 제공되는 전체 상태 퀀텀 시뮬레이터 포함)을 개발할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-144">It is part of the [QDK](https://docs.microsoft.com/quantum/), a full-featured development kit for Q# that you can use with standard tools and languages to develop quantum applications that you can run in various environments, including the built-in full-state quantum simulator.</span></span>

<span data-ttu-id="6bb34-145">Visual Studio 및 VS Code용 확장과 Python 및 Jupyter Notebook에서 사용할 수 있는 패키지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-145">There are extensions for Visual Studio and VS Code, and packages for use with Python and Jupyter Notebook.</span></span>

<span data-ttu-id="6bb34-146">QDK에는 전문적인 화학, 기계 학습 및 숫자 라이브러리와 함께 표준 라이브러리가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-146">The QDK includes a standard library along with specialized chemistry, machine learning, and numerics libraries.</span></span>

<span data-ttu-id="6bb34-147">설명서에는 Q# 언어 가이드, 자습서 및 샘플 코드가 포함되어 있어 빠르게 시작할 수 있으며, 다양한 문서를 통해 양자 컴퓨팅 개념을 더 깊이 이해할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-147">The documentation includes a Q# language guide, tutorials, and sample code to get you started quickly, and rich articles to help you dive deeper into quantum computing concepts.</span></span>  

## <a name="microsoft-quantum-hardware-partners"></a><span data-ttu-id="6bb34-148">Microsoft 양자 하드웨어 파트너</span><span class="sxs-lookup"><span data-stu-id="6bb34-148">Microsoft quantum hardware partners</span></span>

<span data-ttu-id="6bb34-149">Microsoft는 개발자에게 양자 하드웨어에 대한 클라우드 액세스를 제공하기 위해 양자 하드웨어 회사와 파트너 관계를 맺고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-149">Microsoft is partnering with quantum hardware companies to provide developers with cloud access to quantum hardware.</span></span> <span data-ttu-id="6bb34-150">개발자는 [Azure Quantum](https://azure.microsoft.com/services/quantum/) 플랫폼과 Q# 언어를 활용하여 퀀텀 알고리즘을 검색하고 다양한 유형의 퀀텀 하드웨어에서 퀀텀 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-150">Leveraging the [Azure Quantum](https://azure.microsoft.com/services/quantum/) platform and the Q# language, developers will be able to explore quantum algorithms and run their quantum programs on different types of quantum hardware.</span></span>

<span data-ttu-id="6bb34-151">[IonQ](https://ionq.com/news/november-4-2019-microsoft-partnership) 및 [Honeywell](https://www.honeywell.com/en-us/newsroom/news/2019/11/the-future-of-quantum-computing)은 모두 **포획 이온(trapped ion) 기반** 프로세서를 사용하여 전자장에서 포획된 개별 이온을 활용하는 반면, [QCI](https://quantumcircuits.com/news-and-publications/quantum-circuits-partners-with-microsoft-on-azure-quantum)는 초전도 회로를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6bb34-151">[IonQ](https://ionq.com/news/november-4-2019-microsoft-partnership) and [Honeywell](https://www.honeywell.com/en-us/newsroom/news/2019/11/the-future-of-quantum-computing) both use **trapped ion-based** processors, utilizing individual ions trapped in an electronic field, whereas [QCI](https://quantumcircuits.com/news-and-publications/quantum-circuits-partners-with-microsoft-on-azure-quantum) uses superconducting circuits.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6bb34-152">다음 단계</span><span class="sxs-lookup"><span data-stu-id="6bb34-152">Next steps</span></span>

<span data-ttu-id="6bb34-153">[양자 컴퓨팅의 주요 개념](xref:microsoft.quantum.overview.understanding)
[빠른 시작](xref:microsoft.quantum.welcome)</span><span class="sxs-lookup"><span data-stu-id="6bb34-153">[Key concepts for quantum computing](xref:microsoft.quantum.overview.understanding)
[Quickstarts](xref:microsoft.quantum.welcome)</span></span>