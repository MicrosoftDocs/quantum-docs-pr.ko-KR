---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorIndex
title: IdentityGeneratorIndex 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorIndex
qsharp.summary: Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: d2af2dafaf75a68546cb3f16c04cf4c7ee50c6ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724540"
---
# <a name="identitygeneratorindex-function"></a><span data-ttu-id="aac7f-102">IdentityGeneratorIndex 함수</span><span class="sxs-lookup"><span data-stu-id="aac7f-102">IdentityGeneratorIndex function</span></span>

<span data-ttu-id="aac7f-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="aac7f-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="aac7f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aac7f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aac7f-105">Id 진화 작업에 해당 하는 0 Hamiltonian와 일치 하는 생성기 인덱스를 반환 합니다 `H = 0` .</span><span class="sxs-lookup"><span data-stu-id="aac7f-105">Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.</span></span>

```qsharp
function IdentityGeneratorIndex (idxTerm : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="aac7f-106">입력</span><span class="sxs-lookup"><span data-stu-id="aac7f-106">Input</span></span>

### <a name="idxterm--int"></a><span data-ttu-id="aac7f-107">idxTerm: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="aac7f-107">idxTerm : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="aac7f-108">이 입력은 무시 되며 사용자 정의 형식과의 일관성을 위해 정의 됩니다 <xref:microsoft.quantum.simulation.generatorsystem> .</span><span class="sxs-lookup"><span data-stu-id="aac7f-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.simulation.generatorsystem> user-defined type.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="aac7f-109">출력: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="aac7f-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="aac7f-110">Hamiltonian $H = $0의 진화를 나타내는 생성기 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="aac7f-110">A generator index representing evolution under the Hamiltonian $H = 0$.</span></span>