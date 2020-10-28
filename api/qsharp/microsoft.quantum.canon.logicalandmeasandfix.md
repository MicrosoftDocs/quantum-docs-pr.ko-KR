---
uid: Microsoft.Quantum.Canon.LogicalANDMeasAndFix
title: LogicalANDMeasAndFix 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: LogicalANDMeasAndFix
qsharp.summary: Computes the logical AND of multiple qubits.
ms.openlocfilehash: 86e4b9a8c6ed5f4f56db0ceefc8051d34e911c4c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715926"
---
# <a name="logicalandmeasandfix-operation"></a><span data-ttu-id="25a14-102">LogicalANDMeasAndFix 작업</span><span class="sxs-lookup"><span data-stu-id="25a14-102">LogicalANDMeasAndFix operation</span></span>

<span data-ttu-id="25a14-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="25a14-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="25a14-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="25a14-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="25a14-105">여러 비트의 논리적 AND를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a14-105">Computes the logical AND of multiple qubits.</span></span>

```qsharp
operation LogicalANDMeasAndFix (ctrlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="25a14-106">입력</span><span class="sxs-lookup"><span data-stu-id="25a14-106">Input</span></span>

### <a name="ctrlregister--qubit"></a><span data-ttu-id="25a14-107">ctrlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="25a14-107">ctrlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="25a14-108">다중 입력 및 게이트에 대 한 비트 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="25a14-108">Qubits input to the multiple-input AND gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="25a14-109">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="25a14-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="25a14-110">및의 출력이에 기록 되는 데 사용할입니다.</span><span class="sxs-lookup"><span data-stu-id="25a14-110">Qubit on which output of AND is written to.</span></span> <span data-ttu-id="25a14-111">이는 항상 $ \ket $ 상태에서 시작 하는 것으로 간주 됩니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="25a14-111">This is assumed to always start in the $\ket{0}$ state.</span></span>



## <a name="output--unit"></a><span data-ttu-id="25a14-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="25a14-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="25a14-113">설명</span><span class="sxs-lookup"><span data-stu-id="25a14-113">Remarks</span></span>

<span data-ttu-id="25a14-114">`ctrlRegister`에 정확히 $2 $ stbits가 있는 경우이는 작업과 동일 `CCNOT` 하지만 $ \ket {001} $ 및 $ \ket {101} $ 및 $ \ket $의 $-e ^ {i \ pi/2} $에 $e ^ {i \ pi/2} $의 {011} 단계가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25a14-114">When `ctrlRegister` has exactly $2$ qubits, this is equivalent to the `CCNOT` operation but phase with a phase $e^{i\Pi/2}$ on $\ket{001}$ and $-e^{i\Pi/2}$ on $\ket{101}$ and $\ket{011}$.</span></span>
<span data-ttu-id="25a14-115">또한 Adjoint는 특수 한 경우에만 원래 작업의 역함수 인 측정 및 수정 방법입니다 (참조 참조). 단 더 작은 게이트 게이트를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a14-115">The Adjoint is also measure-and-fixup approach that is the inverse of the original operation only in special cases (see references), but uses fewer T-gates.</span></span>

## <a name="references"></a><span data-ttu-id="25a14-116">참조</span><span class="sxs-lookup"><span data-stu-id="25a14-116">References</span></span>

- [<span data-ttu-id="25a14-117">*Craig Gidney* , 1709.06648</span><span class="sxs-lookup"><span data-stu-id="25a14-117"> *Craig Gidney* , 1709.06648</span></span>](https://arxiv.org/abs/1709.06648)