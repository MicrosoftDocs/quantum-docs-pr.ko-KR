---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerFermionImpl
title: JordanWignerFermionImpl 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerFermionImpl
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.

  See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: 616174d4d7f5ac8f4cea9454098d819468076648
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714008"
---
# <a name="jordanwignerfermionimpl-operation"></a><span data-ttu-id="3cd9e-102">JordanWignerFermionImpl 작업</span><span class="sxs-lookup"><span data-stu-id="3cd9e-102">JordanWignerFermionImpl operation</span></span>

<span data-ttu-id="3cd9e-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="3cd9e-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="3cd9e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3cd9e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3cd9e-105">동적 생성기를 simulatable 게이트 집합으로, JordanWigner 기준으로 확장을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3cd9e-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

<span data-ttu-id="3cd9e-106">자세한 내용은 [동적 생성기 모델링](../libraries/data-structures#dynamical-generator-modeling) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3cd9e-106">See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.</span></span>

```qsharp
operation JordanWignerFermionImpl (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="3cd9e-107">입력</span><span class="sxs-lookup"><span data-stu-id="3cd9e-107">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="3cd9e-108">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="3cd9e-108">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="3cd9e-109">JordanWigner에서 단일 진화로 나타낼 생성기 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="3cd9e-109">A generator index to be represented as unitary evolution in the JordanWigner.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="3cd9e-110">Stsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="3cd9e-110">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="3cd9e-111">에서 참조 된 조건에 따라 진화 하는 기간에 대 한 승수 `generatorIndex` 입니다.</span><span class="sxs-lookup"><span data-stu-id="3cd9e-111">A multiplier on the duration of time-evolution by the term referenced in `generatorIndex`.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="3cd9e-112">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3cd9e-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3cd9e-113">시간 진화 연산자에 의해 처리 된 등록입니다.</span><span class="sxs-lookup"><span data-stu-id="3cd9e-113">Register acted upon by time-evolution operator.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3cd9e-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3cd9e-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

