---
uid: Microsoft.Quantum.Simulation.QuantumWalkByQubitization
title: QuantumWalkByQubitization 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: QuantumWalkByQubitization
qsharp.summary: Converts a block-encoding reflection into a quantum walk.
ms.openlocfilehash: ef9740f1867cee3c79a7ec0bf90f2c2f4b39ad28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725576"
---
# <a name="quantumwalkbyqubitization-function"></a><span data-ttu-id="a89d6-102">QuantumWalkByQubitization 함수</span><span class="sxs-lookup"><span data-stu-id="a89d6-102">QuantumWalkByQubitization function</span></span>

<span data-ttu-id="a89d6-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="a89d6-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="a89d6-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a89d6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a89d6-105">블록 인코딩 리플렉션을 퀀텀 탐색으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a89d6-105">Converts a block-encoding reflection into a quantum walk.</span></span>

```qsharp
function QuantumWalkByQubitization (blockEncoding : Microsoft.Quantum.Simulation.BlockEncodingReflection) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="description"></a><span data-ttu-id="a89d6-106">Description</span><span class="sxs-lookup"><span data-stu-id="a89d6-106">Description</span></span>

<span data-ttu-id="a89d6-107">특정 연산자를 대상으로 하 `BlockEncodingReflection` 는 일부 $H 연산자를 인코딩하는 단일 $U $로 표시 된는 $ \pm e ^ {\pm i\sin ^ {-1} (H)} $의 스펙트럼을 포함 하는 퀀텀 워크 $W $로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a89d6-107">Given a `BlockEncodingReflection` represented by a unitary $U$ that encodes some operator $H$ of interest, converts it into a quantum walk $W$ containing the spectrum of $\pm e^{\pm i\sin^{-1}(H)}$.</span></span>

## <a name="input"></a><span data-ttu-id="a89d6-108">입력</span><span class="sxs-lookup"><span data-stu-id="a89d6-108">Input</span></span>

### <a name="blockencoding--blockencodingreflection"></a><span data-ttu-id="a89d6-109">blockEncoding: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="a89d6-109">blockEncoding : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="a89d6-110">`BlockEncodingReflection`퀀텀 탐색으로 변환할 단일 $U $입니다.</span><span class="sxs-lookup"><span data-stu-id="a89d6-110">A `BlockEncodingReflection` unitary $U$ to be converted into a Quantum walk.</span></span>



## <a name="output--qubitqubit--unit-adj--ctl"></a><span data-ttu-id="a89d6-111">출력: (Adj[[]](xref:microsoft.quantum.lang-ref.qubit)[, []](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="a89d6-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="a89d6-112">퀀텀 탐색 $W $는 레지스터를 공동으로 수행 하 `a` 고 `s` $H $를 차단 하며 $ \pm e ^ {\pm i\sin ^ {-1} (H)} $의 스펙트럼을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a89d6-112">A quantum walk $W$ acting jointly on registers `a` and `s` that block- encodes $H$, and contains the spectrum of $\pm e^{\pm i\sin^{-1}(H)}$.</span></span>

## <a name="references"></a><span data-ttu-id="a89d6-113">참조</span><span class="sxs-lookup"><span data-stu-id="a89d6-113">References</span></span>

- <span data-ttu-id="a89d6-114">Hamiltonian 시뮬레이션의 Guang Jia-hao Low, Isaac Chuang https://arxiv.org/abs/1610.06546</span><span class="sxs-lookup"><span data-stu-id="a89d6-114">Hamiltonian Simulation by Qubitization Guang Hao Low, Isaac L. Chuang https://arxiv.org/abs/1610.06546</span></span>

## <a name="see-also"></a><span data-ttu-id="a89d6-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a89d6-115">See Also</span></span>

- [<span data-ttu-id="a89d6-116">Microsoft 양자. 블록 인코딩</span><span class="sxs-lookup"><span data-stu-id="a89d6-116">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="a89d6-117">BlockEncodingReflection.</span><span class="sxs-lookup"><span data-stu-id="a89d6-117">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)