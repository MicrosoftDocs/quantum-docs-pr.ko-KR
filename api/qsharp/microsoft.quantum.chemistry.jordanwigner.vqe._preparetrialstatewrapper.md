---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE._prepareTrialStateWrapper
title: _prepareTrialStateWrapper 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: _prepareTrialStateWrapper
qsharp.summary: Private wrapper around PrepareTrialState to make it compatible with EstimateFrequencyA by defining an adjoint. EstimateFrequencyA has built-in emulation feature when targeting the QuantumSimulator, which speeds up its execution.
ms.openlocfilehash: bfd7b9ce8e8b2c8f322d676c640f8c2488655516
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713763"
---
# <a name="_preparetrialstatewrapper-operation"></a><span data-ttu-id="e5a33-102">_prepareTrialStateWrapper 작업</span><span class="sxs-lookup"><span data-stu-id="e5a33-102">_prepareTrialStateWrapper operation</span></span>

<span data-ttu-id="e5a33-103">네임 스페이스: [JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="e5a33-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="e5a33-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e5a33-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e5a33-105">Adjoint를 정의 하 여 EstimateFrequencyA와 호환 되도록 PrepareTrialState에 대 한 개인 래퍼입니다.</span><span class="sxs-lookup"><span data-stu-id="e5a33-105">Private wrapper around PrepareTrialState to make it compatible with EstimateFrequencyA by defining an adjoint.</span></span>
<span data-ttu-id="e5a33-106">EstimateFrequencyA는 QuantumSimulator를 대상으로 하는 경우 기본 제공 에뮬레이션 기능을 제공 하므로 실행 속도가 빨라집니다.</span><span class="sxs-lookup"><span data-stu-id="e5a33-106">EstimateFrequencyA has built-in emulation feature when targeting the QuantumSimulator, which speeds up its execution.</span></span>

```qsharp
operation _prepareTrialStateWrapper (inputState : (Int, Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]), qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e5a33-107">입력</span><span class="sxs-lookup"><span data-stu-id="e5a33-107">Input</span></span>

### <a name="inputstate--intjordanwignerinputstate"></a><span data-ttu-id="e5a33-108">inputState: ([Int](xref:microsoft.quantum.lang-ref.int),[JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[])</span><span class="sxs-lookup"><span data-stu-id="e5a33-108">inputState : ([Int](xref:microsoft.quantum.lang-ref.int),[JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[])</span></span>

<span data-ttu-id="e5a33-109">PrepareTrialState를 실행 하는 데 필요한 Jordan-Wigner 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="e5a33-109">The Jordan-Wigner input required for PrepareTrialState to run.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="e5a33-110">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e5a33-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e5a33-111">고 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="e5a33-111">A qubit register.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e5a33-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e5a33-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

