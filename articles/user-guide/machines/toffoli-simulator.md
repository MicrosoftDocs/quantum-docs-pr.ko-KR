---
title: 퀀텀 개발 키트 Toffoli 시뮬레이터
description: 수백만 개의 다양 한 비트와 함께 사용할 수 있는 특별 한 용도의 퀀텀 시뮬레이터 인 Microsoft QDK Toffoli 시뮬레이터에 대해 알아봅니다.
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 01/16/2019
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
ms.openlocfilehash: 8a29caaa0fa058600a74e7d130e644374cbfa19c
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85276032"
---
# <a name="quantum-development-kit-toffoli-simulator"></a><span data-ttu-id="7f851-103">퀀텀 개발 키트 Toffoli 시뮬레이터</span><span class="sxs-lookup"><span data-stu-id="7f851-103">Quantum Development Kit Toffoli Simulator</span></span>

<span data-ttu-id="7f851-104">퀀텀 개발 키트는 Toffoli 시뮬레이터를 제공 합니다 .이 시뮬레이터는 X, CNOT 및 다중 제어 된 X 퀀텀 작업으로 제한 되는 퀀텀 알고리즘을 시뮬레이션할 수 있는 특수 한 용도의 시뮬레이터입니다. 모든 기존 논리 및 계산을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f851-104">The Quantum Development Kit provides a Toffoli simulator, which is a special-purpose simulator that can simulate quantum algorithms that are limited to X, CNOT, and multi-controlled X quantum operations (all classical logic and computations are available).</span></span>

<span data-ttu-id="7f851-105">Toffoli 시뮬레이터는 [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)보다 작업에서 훨씬 더 제한적 이지만 훨씬 더 많은 비트를 시뮬레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f851-105">While the Toffoli simulator is much more restricted in operation than the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator), it can simulate far more qubits.</span></span>
<span data-ttu-id="7f851-106">Toffoli 시뮬레이터는 수백만 개의 다양 한 비트와 함께 사용할 수 있지만 전체 상태 시뮬레이터는 일반적으로 약 30 개로 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f851-106">The Toffoli simulator can be used with millions of qubits, while the full state simulator is generally limited to about 30.</span></span>
<span data-ttu-id="7f851-107">컴퓨터에서 Q #으로 작성 된 제한 된 퀀텀 알고리즘 집합을 실행 하 고 디버그할 수 있습니다. 예를 들어, 부울 함수를 평가 하는 oracles는 이러한 게이트를 사용 하 여 구현 될 수 있으므로이 시뮬레이터를 사용 하 여 많은 수의 다양 한 수의로 테스트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f851-107">It can execute and debug a limited set of quantum algorithms written in Q# on your computer; for instance, oracles that evaluate Boolean functions can be implemented using these gates and so tested on vary large numbers of qubits using this simulator.</span></span>

<span data-ttu-id="7f851-108">이 퀀텀 시뮬레이터는 클래스를 통해 노출 됩니다 `ToffoliSimulator` .</span><span class="sxs-lookup"><span data-stu-id="7f851-108">This quantum simulator is exposed via the `ToffoliSimulator` class.</span></span>
<span data-ttu-id="7f851-109">시뮬레이터를 사용 하려면이 클래스의 인스턴스를 만들어 `Run` 나머지 매개 변수와 함께 실행 하려는 퀀텀 작업의 메서드에 전달 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f851-109">To use the simulator, simply create an instance of this class and pass it to the `Run` method of the quantum operation you want to execute along with the rest of the parameters:</span></span>

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

## <a name="other-operations"></a><span data-ttu-id="7f851-110">기타 작업</span><span class="sxs-lookup"><span data-stu-id="7f851-110">Other Operations</span></span>

<span data-ttu-id="7f851-111">는 `ToffoliSimulator` `R` `Exp` 결과 작업이 또는 id와 같은 경우 및와 같은 회전 및 지수화 paulis를 지원 합니다 `X` .</span><span class="sxs-lookup"><span data-stu-id="7f851-111">The `ToffoliSimulator` supports rotations and exponentiated Paulis, such as `R` and `Exp`, when the resulting operation is equal to `X` or to the identity.</span></span>

<span data-ttu-id="7f851-112">측정 및 어설션이 지원 되지만, Pauli로만 지원 됩니다 `Z` .</span><span class="sxs-lookup"><span data-stu-id="7f851-112">Measurement and assert are supported, but only in the Pauli `Z` basis.</span></span>
<span data-ttu-id="7f851-113">일부 측정의 확률은 항상 0 또는 1입니다. Toffoli 시뮬레이터에는 임의성이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7f851-113">Note that the probability of some measurement is always either 0 or 1; there is no randomness in the Toffoli simulator.</span></span>

<span data-ttu-id="7f851-114">`DumpMachine`와 `DumpRegister`가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f851-114">`DumpMachine` and `DumpRegister` are supported.</span></span>
<span data-ttu-id="7f851-115">두 가지 모두 `Z` 각 비트의 현재 기반 상태를 선 마다 하나씩 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f851-115">They both output the current `Z`-basis state of each qubit, one qubit per line.</span></span>

## <a name="qubitcount"></a><span data-ttu-id="7f851-116">고 비트 수</span><span class="sxs-lookup"><span data-stu-id="7f851-116">QubitCount</span></span>

<span data-ttu-id="7f851-117">기본적으로는 `ToffoliSimulator` 65536의 공간을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f851-117">By default, the `ToffoliSimulator` allocates space for 65,536 qubits.</span></span>
<span data-ttu-id="7f851-118">알고리즘에이 보다 많은 값이 필요한 경우에는 매개 변수의 값을 생성자에 제공 하 여 원하는 비트 수를 변경할 수 있습니다 `qubitCount` .</span><span class="sxs-lookup"><span data-stu-id="7f851-118">If your algorithm requires more than this, you can change the qubit count by providing a value for the `qubitCount` parameter to the constructor.</span></span>
<span data-ttu-id="7f851-119">각 추가 비트에는 추가 바이트의 메모리가 필요 하므로 필요한 overestimating의 수를 크게 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f851-119">Each additional qubit requires an additional byte of memory, so there is no significant cost to overestimating the number of qubits you'll need.</span></span>

<span data-ttu-id="7f851-120">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="7f851-120">For example:</span></span>

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```
