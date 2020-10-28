---
uid: Microsoft.Quantum.Chemistry.JordanWigner._JordanWignerClusterOperatorImpl
title: _JordanWignerClusterOperatorImpl 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _JordanWignerClusterOperatorImpl
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.

  See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: 9507558ebe73bce87d9089aad22b94c1d9d579d0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714603"
---
# <a name="_jordanwignerclusteroperatorimpl-operation"></a><span data-ttu-id="109af-102">_JordanWignerClusterOperatorImpl 작업</span><span class="sxs-lookup"><span data-stu-id="109af-102">_JordanWignerClusterOperatorImpl operation</span></span>

<span data-ttu-id="109af-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="109af-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="109af-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="109af-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="109af-105">동적 생성기를 simulatable 게이트 집합으로, JordanWigner 기준으로 확장을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="109af-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

<span data-ttu-id="109af-106">자세한 내용은 [동적 생성기 모델링](../libraries/data-structures#dynamical-generator-modeling) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="109af-106">See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.</span></span>

```qsharp
operation _JordanWignerClusterOperatorImpl (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="109af-107">입력</span><span class="sxs-lookup"><span data-stu-id="109af-107">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="109af-108">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="109af-108">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="109af-109">JordanWigner에서 단일 진화로 나타낼 생성기 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="109af-109">A generator index to be represented as unitary evolution in the JordanWigner.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="109af-110">Stsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="109af-110">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="109af-111">시뮬레이션 알고리즘의 시그니처와 일치 하는 더미 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="109af-111">Dummy variable to match signature of simulation algorithms.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="109af-112">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="109af-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="109af-113">시간 진화 연산자에 의해 처리 된 등록입니다.</span><span class="sxs-lookup"><span data-stu-id="109af-113">Register acted upon by time-evolution operator.</span></span>



## <a name="output--unit"></a><span data-ttu-id="109af-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="109af-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

