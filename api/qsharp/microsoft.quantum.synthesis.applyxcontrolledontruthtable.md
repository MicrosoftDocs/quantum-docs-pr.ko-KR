---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable
title: ApplyXControlledOnTruthTable 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTable
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: 6e956038f7cd15db7348ff830da8bc9eae53aa61
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855555"
---
# <a name="applyxcontrolledontruthtable-operation"></a><span data-ttu-id="8311d-102">ApplyXControlledOnTruthTable 작업</span><span class="sxs-lookup"><span data-stu-id="8311d-102">ApplyXControlledOnTruthTable operation</span></span>

<span data-ttu-id="8311d-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="8311d-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="8311d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8311d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8311d-105">@"microsoft.quantum.intrinsic.x" `target` `func` 의 기존 할당에 대해 부울 함수가 true로 평가 되는 경우에 작업을 적용 합니다 `controlRegister` .</span><span class="sxs-lookup"><span data-stu-id="8311d-105">Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.</span></span>

```qsharp
operation ApplyXControlledOnTruthTable (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="8311d-106">설명</span><span class="sxs-lookup"><span data-stu-id="8311d-106">Description</span></span>

<span data-ttu-id="8311d-107">작업은 단일 작업 \begin{align} U\ket {x} \ k {y} = \ket{x}\ket{y \oplus f (x)} \end{align}을 구현 합니다. 여기서 $x $ 및 $y $는 `controlRegister` `target` 각각 및를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8311d-107">The operation implements the unitary operation \begin{align} U\ket{x}\ket{y} = \ket{x}\ket{y \oplus f(x)} \end{align} where $x$ and $y$ represent `controlRegister` and `target`, respectively.</span></span>

<span data-ttu-id="8311d-108">부울 함수 $f $는 큰 정수를 기준으로 참 테이블로 표현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8311d-108">The Boolean function $f$ is represented as a truth table in terms of a big integer.</span></span>
<span data-ttu-id="8311d-109">예를 들어 세 입력의 과반수 함수는 bitstring으로 표현 됩니다 `11101000` . 여기서 가장 중요 한 비트는 `1` 입력 할당에 해당 하 `(1, 1, 1)` 고 가장 중요 한 비트는 `0` 입력 할당에 해당 합니다 `(0, 0, 0)` .</span><span class="sxs-lookup"><span data-stu-id="8311d-109">For example, the majority function on three inputs is represented by the bitstring `11101000`, where the most significant bit `1` corresponds to the input assignment `(1, 1, 1)`, and the least significant bit `0` corresponds to the input assignment `(0, 0, 0)`.</span></span>
<span data-ttu-id="8311d-110">이 값은 `0xE8L` 16 진수 표기법으로 큰 정수 또는 10 진수 표기법으로 나타낼 수 있습니다 `232L` .</span><span class="sxs-lookup"><span data-stu-id="8311d-110">It can be represented by the big integer `0xE8L` in hexadecimal notation or as `232L` in decimal notation.</span></span>  <span data-ttu-id="8311d-111">`L`접미사는 상수가 형식 임을 나타냅니다 `BigInt` .</span><span class="sxs-lookup"><span data-stu-id="8311d-111">The `L` suffix indicates that the constant is of type `BigInt`.</span></span>
<span data-ttu-id="8311d-112">이 표현에 대 한 자세한 내용은 [kata 테이블](https://github.com/microsoft/QuantumKatas/tree/main/TruthTables)에서도 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8311d-112">More details on this representation can also be found in the [truth tables kata](https://github.com/microsoft/QuantumKatas/tree/main/TruthTables).</span></span>

<span data-ttu-id="8311d-113">구현에서는 @"microsoft.quantum.intrinsic.cnot" 및 게이트를 사용 @"microsoft.quantum.intrinsic.r1" 합니다.</span><span class="sxs-lookup"><span data-stu-id="8311d-113">The implementation makes use of @"microsoft.quantum.intrinsic.cnot" and @"microsoft.quantum.intrinsic.r1" gates.</span></span>

## <a name="input"></a><span data-ttu-id="8311d-114">입력</span><span class="sxs-lookup"><span data-stu-id="8311d-114">Input</span></span>

### <a name="func--bigint"></a><span data-ttu-id="8311d-115">func: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="8311d-115">func : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="8311d-116">큰 정수로 표시 되는 부울 참 테이블</span><span class="sxs-lookup"><span data-stu-id="8311d-116">Boolean truth table represented as big integer</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="8311d-117">controlRegister: [bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8311d-117">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="8311d-118">컨트롤의 등록</span><span class="sxs-lookup"><span data-stu-id="8311d-118">Register of control qubits</span></span>


### <a name="target--qubit"></a><span data-ttu-id="8311d-119">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8311d-119">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8311d-120">대상 비트</span><span class="sxs-lookup"><span data-stu-id="8311d-120">Target qubit</span></span>



## <a name="output--unit"></a><span data-ttu-id="8311d-121">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8311d-121">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="8311d-122">참조</span><span class="sxs-lookup"><span data-stu-id="8311d-122">References</span></span>

- [<span data-ttu-id="8311d-123">*Schuch*, *Siewert*, prl 91, 027902, 2003, arxiv:/0303063</span><span class="sxs-lookup"><span data-stu-id="8311d-123">*N. Schuch*, *J. Siewert*, PRL 91, no. 027902, 2003, arXiv:quant-ph/0303063</span></span>](https://arxiv.org/abs/quant-ph/0303063)
- [<span data-ttu-id="8311d-124">*Mathias Soeken*, *Martin Roetteler*, arxiv: 2005.12310</span><span class="sxs-lookup"><span data-stu-id="8311d-124">*Mathias Soeken*, *Martin Roetteler*, arXiv:2005.12310</span></span>](https://arxiv.org/abs/2005.12310)

## <a name="see-also"></a><span data-ttu-id="8311d-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8311d-125">See Also</span></span>

- [<span data-ttu-id="8311d-126">ApplyXControlledOnTruthTableWithCleanTarget.</span><span class="sxs-lookup"><span data-stu-id="8311d-126">Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget)