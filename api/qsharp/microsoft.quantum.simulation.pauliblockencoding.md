---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: PauliBlockEncoding 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: b1df6d239e6ef061cf0a4784c652e9dd126991d5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230432"
---
# <a name="pauliblockencoding-function"></a><span data-ttu-id="1c503-102">PauliBlockEncoding 함수</span><span class="sxs-lookup"><span data-stu-id="1c503-102">PauliBlockEncoding function</span></span>

<span data-ttu-id="1c503-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="1c503-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="1c503-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1c503-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1c503-105">Hamiltonian에 대 한 블록 인코딩 단일를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c503-105">Creates a block-encoding unitary for a Hamiltonian.</span></span>

<span data-ttu-id="1c503-106">Hamiltonian $H = \ sum_ {j} \ alpha_j P_j $는 각각 실제 계수 $ \ $P $를 포함 하는 Pauli 용어 _j alpha_j의 합계로 설명 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c503-106">The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.</span></span>

```qsharp
function PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a><span data-ttu-id="1c503-107">입력</span><span class="sxs-lookup"><span data-stu-id="1c503-107">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="1c503-108">generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="1c503-108">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="1c503-109">`GeneratorSystem`$H $를 Pauli 용어의 합계로 설명 하는입니다.</span><span class="sxs-lookup"><span data-stu-id="1c503-109">A `GeneratorSystem` that describes $H$ as a sum of Pauli terms</span></span>



## <a name="output--doubleblockencodingreflection"></a><span data-ttu-id="1c503-110">출력: ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span><span class="sxs-lookup"><span data-stu-id="1c503-110">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="1c503-111">첫 번째 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1c503-111">First parameter</span></span>

<span data-ttu-id="1c503-112">계수 $ \alpha = \ sum_ {j} | \ alpha_j | $ 인 1-표준을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c503-112">The one-norm of coefficients $\alpha=\sum_{j}|\alpha_j|$.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="1c503-113">두 번째 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1c503-113">Second parameter</span></span>

<span data-ttu-id="1c503-114">`BlockEncodingReflection`Hamiltonian $H $의 단일 $U $입니다.</span><span class="sxs-lookup"><span data-stu-id="1c503-114">A `BlockEncodingReflection` unitary $U$ of the Hamiltonian $H$.</span></span> <span data-ttu-id="1c503-115">이 단일 항목은 $U ^ 2 = I $를 충족 하므로 리플렉션 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c503-115">As this unitary satisfies $U^2 = I$, it is also a reflection.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c503-116">설명</span><span class="sxs-lookup"><span data-stu-id="1c503-116">Remarks</span></span>

<span data-ttu-id="1c503-117">이는 $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ 상태를 준비 하 고 준비 하지 않으며 곱셈 제어 된 단일 및을 생성 하 여 얻을 수 <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c503-117">This is obtained by preparing and unpreparing the state $\sum_{j}\sqrt{\alpha_j/\alpha}\ket{j}$, and constructing a multiply-controlled unitary <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> and <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator>.</span></span>