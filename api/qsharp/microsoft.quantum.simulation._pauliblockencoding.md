---
uid: Microsoft.Quantum.Simulation._PauliBlockEncoding
title: _PauliBlockEncoding 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: c27ef1a6b7cd7c84defe2a783e9fb1610e52d1e7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851074"
---
# <a name="_pauliblockencoding-function"></a><span data-ttu-id="e0569-102">_PauliBlockEncoding 함수</span><span class="sxs-lookup"><span data-stu-id="e0569-102">_PauliBlockEncoding function</span></span>

<span data-ttu-id="e0569-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e0569-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e0569-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e0569-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e0569-105">Hamiltonian에 대 한 블록 인코딩 단일를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0569-105">Creates a block-encoding unitary for a Hamiltonian.</span></span>

<span data-ttu-id="e0569-106">Hamiltonian $H = \ sum_ {j} \ alpha_j P_j $는 각각 실제 계수 $ \ $P $를 포함 하는 Pauli 용어 _j alpha_j의 합계로 설명 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0569-106">The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.</span></span>

```qsharp
function _PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem, statePrepUnitary : (Double[] -> (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)), multiplexer : ((Int, (Int -> (Qubit[] => Unit is Adj + Ctl))) -> ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a><span data-ttu-id="e0569-107">입력</span><span class="sxs-lookup"><span data-stu-id="e0569-107">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="e0569-108">generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="e0569-108">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="e0569-109">`GeneratorSystem`$H $를 Pauli 용어의 합계로 설명 하는입니다.</span><span class="sxs-lookup"><span data-stu-id="e0569-109">A `GeneratorSystem` that describes $H$ as a sum of Pauli terms</span></span>


### <a name="stateprepunitary--double---littleendian--unit--is-adj--ctl"></a><span data-ttu-id="e0569-110">statePrepUnitary: [Double](xref:microsoft.quantum.lang-ref.double)[]-> [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="e0569-110">statePrepUnitary : [Double](xref:microsoft.quantum.lang-ref.double)[] -> [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="e0569-111">J\rightarrow V_j $ $f 함수를 지정 하 여 인덱스 $ \ket{j} $에 의해 제어 되는 단일 $V _j $를 적용 하는 단일 연산 $V $입니다.</span><span class="sxs-lookup"><span data-stu-id="e0569-111">A unitary operation $V$ that applies the unitary $V_j$ controlled on index $\ket{j}$, given a function $f: j\rightarrow V_j$.</span></span>


### <a name="multiplexer--intint---qubit--unit--is-adj--ctl---littleendianqubit--unit--is-adj--ctl"></a><span data-ttu-id="e0569-112">멀티플렉서: ([int](xref:microsoft.quantum.lang-ref.int),[int, int](xref:microsoft.quantum.lang-ref.int) -> [](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) is Adj + ctl)-> ([LittleEndian,](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[sbit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) is Adj + ctl</span><span class="sxs-lookup"><span data-stu-id="e0569-112">multiplexer : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl) -> ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>





## <a name="output--doubleblockencodingreflection"></a><span data-ttu-id="e0569-113">출력: ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span><span class="sxs-lookup"><span data-stu-id="e0569-113">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="e0569-114">첫 번째 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e0569-114">First parameter</span></span>

<span data-ttu-id="e0569-115">계수 $ \alpha = \ sum_ {j} | \ alpha_j | $ 인 1-표준을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0569-115">The one-norm of coefficients $\alpha=\sum_{j}|\alpha_j|$.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="e0569-116">두 번째 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e0569-116">Second parameter</span></span>

<span data-ttu-id="e0569-117">`BlockEncodingReflection`Hamiltonian $U $의 단일 $U $입니다.</span><span class="sxs-lookup"><span data-stu-id="e0569-117">A `BlockEncodingReflection` unitary $U$ of the Hamiltonian $U$.</span></span> <span data-ttu-id="e0569-118">이 단일 항목은 $U ^ 2 = I $를 충족 하므로 리플렉션 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0569-118">As this unitary satisfies $U^2 = I$, it is also a reflection.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0569-119">설명</span><span class="sxs-lookup"><span data-stu-id="e0569-119">Remarks</span></span>

<span data-ttu-id="e0569-120">작업 예: $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $의 상태를 준비 하 고 준비 하지 않으며, 곱하기 제어 되는 단일 구성 작업은 <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> 및 <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> 입니다.</span><span class="sxs-lookup"><span data-stu-id="e0569-120">Example operations the prepare and unpreparing the state $\sum_{j}\sqrt{\alpha_j/\alpha}\ket{j}$, and construct a multiply-controlled unitary are <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> and <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator>.</span></span>