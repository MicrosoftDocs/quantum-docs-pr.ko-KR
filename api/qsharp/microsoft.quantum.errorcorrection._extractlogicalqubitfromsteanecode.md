---
uid: Microsoft.Quantum.ErrorCorrection._ExtractLogicalQubitFromSteaneCode
title: _ExtractLogicalQubitFromSteaneCode 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: _ExtractLogicalQubitFromSteaneCode
qsharp.summary: >-
  Syndrome measurement and the inverse of embedding.

  $X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit. This asymmetry leads to a different syndrome extraction routine. One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.
ms.openlocfilehash: fe64343e30a0a3f0d05382e7812d37d5b13133d3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853210"
---
# <a name="_extractlogicalqubitfromsteanecode-operation"></a><span data-ttu-id="844b9-102">_ExtractLogicalQubitFromSteaneCode 작업</span><span class="sxs-lookup"><span data-stu-id="844b9-102">_ExtractLogicalQubitFromSteaneCode operation</span></span>

<span data-ttu-id="844b9-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="844b9-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="844b9-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="844b9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="844b9-105">증후군 측정과 포함의 역함수입니다.</span><span class="sxs-lookup"><span data-stu-id="844b9-105">Syndrome measurement and the inverse of embedding.</span></span>

<span data-ttu-id="844b9-106">$X $-및 $Z $-stabilizers은 특정 인코딩 회로 선택 때문에 동일 하 게 처리 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="844b9-106">$X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit.</span></span>
<span data-ttu-id="844b9-107">이 비대칭는 다른 증후군 추출 루틴으로 이어집니다.</span><span class="sxs-lookup"><span data-stu-id="844b9-107">This asymmetry leads to a different syndrome extraction routine.</span></span>
<span data-ttu-id="844b9-108">이는 코드 상태에서 직접 여러 가지 증후군 비트 Pauli 연산자를 측정 하 여이를 측정할 수 있지만 추출을 목적으로 인해 추가 ancillas 없이 증후군 측정값을 수행할 수 있는 단일의 비트에 논리가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="844b9-108">One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.</span></span>

```qsharp
operation _ExtractLogicalQubitFromSteaneCode (code : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit, Int, Int)
```


## <a name="input"></a><span data-ttu-id="844b9-109">입력</span><span class="sxs-lookup"><span data-stu-id="844b9-109">Input</span></span>

### <a name="code--logicalregister"></a><span data-ttu-id="844b9-110">코드: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="844b9-110">code : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>





## <a name="output--qubitintint"></a><span data-ttu-id="844b9-111">Output[: (가,](xref:microsoft.quantum.lang-ref.qubit)[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="844b9-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

<span data-ttu-id="844b9-112">$X $-증후군 및 $Z $-증후군에 대 한 논리 비트 및 정수 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="844b9-112">The logical qubit and a pair of integers for $X$-syndrome and $Z$-syndrome.</span></span>
<span data-ttu-id="844b9-113">이는 단일 $X $ 또는 $Z $-오류가 측정 된 증후군를 발생 시킨 코드의 인덱스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="844b9-113">They represent the index of the code qubit on which a single $X$- or $Z$-error would have caused the measured syndrome.</span></span>

## <a name="remarks"></a><span data-ttu-id="844b9-114">설명</span><span class="sxs-lookup"><span data-stu-id="844b9-114">Remarks</span></span>

<span data-ttu-id="844b9-115">`internal`단위 테스트가이 작업에 직접적으로 종속 되므로이 작업은으로 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="844b9-115">Note that this operation is not marked as `internal`, as unit tests directly depend on this operation.</span></span> <span data-ttu-id="844b9-116">이후 향상 된 기능으로 서, 단위 테스트는 공용 callables에만 종속 되도록 리팩터링 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="844b9-116">As a future improvement, unit tests should be refactored to depend only on public callables directly.</span></span>

> [!WARNING]
> <span data-ttu-id="844b9-117">이 루틴은 Steane의 7abit 코드에 대 한 특정 인코딩 회로에 맞게 조정 됩니다. 인코딩 회로가 수정 되 면 증후군 결과가 다르게 해석 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="844b9-117">This routine is tailored to a particular encoding circuit for Steane's 7 qubit code; if the encoding circuit is modified then the syndrome outcome might have to be interpreted differently.</span></span>