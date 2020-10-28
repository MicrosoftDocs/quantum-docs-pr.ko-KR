---
uid: Microsoft.Quantum.Research.Chemistry.OptimizedTrotterStepOracle
title: OptimizedTrotterStepOracle 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: OptimizedTrotterStepOracle
qsharp.summary: Returns optimized Trotter step operation and the parameters necessary to run it.
ms.openlocfilehash: f78d80f7ab71f4fc759d8045c9a134d7178aaa15
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710753"
---
# <a name="optimizedtrottersteporacle-function"></a><span data-ttu-id="44bd8-102">OptimizedTrotterStepOracle 함수</span><span class="sxs-lookup"><span data-stu-id="44bd8-102">OptimizedTrotterStepOracle function</span></span>

<span data-ttu-id="44bd8-103">네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="44bd8-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="44bd8-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="44bd8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="44bd8-105">최적화 된 Trotter step 작업 및이 작업을 실행 하는 데 필요한 매개 변수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="44bd8-105">Returns optimized Trotter step operation and the parameters necessary to run it.</span></span>

```qsharp
function OptimizedTrotterStepOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, trotterStepSize : Double, trotterOrder : Int) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a><span data-ttu-id="44bd8-106">입력</span><span class="sxs-lookup"><span data-stu-id="44bd8-106">Input</span></span>

### <a name="qsharpdata--jordanwignerencodingdata"></a><span data-ttu-id="44bd8-107">qSharpData: [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="44bd8-107">qSharpData : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="44bd8-108">Hamiltonian은 형식으로 설명 `JordanWignerEncodingData` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="44bd8-108">Hamiltonian described by `JordanWignerEncodingData` format.</span></span>


### <a name="trotterstepsize--double"></a><span data-ttu-id="44bd8-109">trotterStepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="44bd8-109">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="44bd8-110">Trotter 통합자의 단계 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="44bd8-110">Step size of Trotter integrator.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="44bd8-111">trotterOrder: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="44bd8-111">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="44bd8-112">Trotter 통합자의 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="44bd8-112">Order of Trotter integrator.</span></span>



## <a name="output--intdoublequbit--unit-adj--ctl"></a><span data-ttu-id="44bd8-113">Output: ([Int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[intbit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl))</span><span class="sxs-lookup"><span data-stu-id="44bd8-113">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl))</span></span>

<span data-ttu-id="44bd8-114">튜플:은 `Int` 할당 된 값이 `Double` `1.0/trotterStepSize` 고,은 이며, 작업은 Trotter 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="44bd8-114">A tuple where: `Int` is the number of qubits allocated, `Double` is `1.0/trotterStepSize`, and the operation is the Trotter step.</span></span>