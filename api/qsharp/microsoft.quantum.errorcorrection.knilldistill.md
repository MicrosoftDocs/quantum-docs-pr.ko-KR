---
uid: Microsoft.Quantum.ErrorCorrection.KnillDistill
title: KnillDistill 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: KnillDistill
qsharp.summary: Implements the Knill magic state distillation algorithm.
ms.openlocfilehash: 4eff99eebb1e271d240513f827c6e93973ef79a6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853112"
---
# <a name="knilldistill-operation"></a><span data-ttu-id="375fc-102">KnillDistill 작업</span><span class="sxs-lookup"><span data-stu-id="375fc-102">KnillDistill operation</span></span>

<span data-ttu-id="375fc-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="375fc-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="375fc-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="375fc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="375fc-105">Knill magic state 추출을 알고리즘을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="375fc-105">Implements the Knill magic state distillation algorithm.</span></span>

```qsharp
operation KnillDistill (roughMagic : Qubit[]) : Bool
```


## <a name="description"></a><span data-ttu-id="375fc-106">설명</span><span class="sxs-lookup"><span data-stu-id="375fc-106">Description</span></span>

<span data-ttu-id="375fc-107">매직 상태 $ $ \begin{align} \cos\frac{\pi} {8} \ket {0} + \sin \frac{\pi} \ket \end{align}의 15 개의 대략적인 {8} 복사본 {1} 을 지정 하면, $ $는 고품질의 복사본 하나를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="375fc-107">Given 15 approximate copies of a magic state $$ \begin{align} \cos\frac{\pi}{8} \ket{0} + \sin \frac{\pi}{8} \ket{1} \end{align}, $$ yields one higher-quality copy.</span></span>

## <a name="input"></a><span data-ttu-id="375fc-108">입력</span><span class="sxs-lookup"><span data-stu-id="375fc-108">Input</span></span>

### <a name="roughmagic--qubit"></a><span data-ttu-id="375fc-109">roughMagic: [](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="375fc-109">roughMagic : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="375fc-110">매직 상태의 대략적인 복사본을 포함 하는 15 개의 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="375fc-110">A register of fifteen qubits containing approximate copies of a magic state.</span></span> <span data-ttu-id="375fc-111">이 추출을 절차의 다음 응용 프로그램에 `roughMagic[0]` 는 고품질 복사본이 하나 포함 되 고 나머지 레지스터는 $ \ket{00\cdots 0} $ 상태로 다시 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="375fc-111">Following application of this distillation procedure, `roughMagic[0]` will contain one higher-quality copy, and the rest of the register will be reset to the $\ket{00\cdots 0}$ state.</span></span>



## <a name="output--bool"></a><span data-ttu-id="375fc-112">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="375fc-112">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="375fc-113">이면 `true` 프로시저 성공 및 고품질 복사를 수락 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="375fc-113">If `true`, then the procedure succeeded and the higher-quality copy should be accepted.</span></span> <span data-ttu-id="375fc-114">이면 `false` 프로시저가 실패 하 고 레지스터의 상태가 undefined로 간주 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="375fc-114">If `false`, the procedure failed, and the state of the register should be considered undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="375fc-115">설명</span><span class="sxs-lookup"><span data-stu-id="375fc-115">Remarks</span></span>

<span data-ttu-id="375fc-116">Knill 알고리즘을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="375fc-116">We follow the algorithm of Knill.</span></span>
<span data-ttu-id="375fc-117">그러나 현재 구현은 너무 많은 비트를 사용 하기 때문에 최적 상태가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="375fc-117">However, the present implementation is far from being optimal, as it uses too many qubits.</span></span>
<span data-ttu-id="375fc-118">매직 상태는이 루틴에 삽입 되며,이 경우 더 나은 프로토콜이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="375fc-118">The magic states are injected in this routine, in which case there are better protocols.</span></span>

## <a name="references"></a><span data-ttu-id="375fc-119">참조</span><span class="sxs-lookup"><span data-stu-id="375fc-119">References</span></span>

- [<span data-ttu-id="375fc-120">Knill</span><span class="sxs-lookup"><span data-stu-id="375fc-120">Knill</span></span>](https://arxiv.org/abs/quant-ph/0402171)