---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterCDKMAdder
title: ApplyOuterCDKMAdder 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterCDKMAdder
qsharp.summary: Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below. Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.
ms.openlocfilehash: acaa563245bb7c701316d2dfd35b5be03d8e024d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843717"
---
# <a name="applyoutercdkmadder-operation"></a><span data-ttu-id="a8c8c-102">ApplyOuterCDKMAdder 작업</span><span class="sxs-lookup"><span data-stu-id="a8c8c-102">ApplyOuterCDKMAdder operation</span></span>

<span data-ttu-id="a8c8c-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a8c8c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a8c8c-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a8c8c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a8c8c-105">해독 가능한 내부 ripple 작업은 아래 RippleCarryAdderCDKM 정수 더하기 연산에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8c8c-105">Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below.</span></span>
<span data-ttu-id="a8c8c-106">두 개의 두 가지 비트 레지스터 `xs` 와 `ys` 길이가 동일한 경우 작업은 CNOT 및 ccnot 게이트의 ripple 작업 시퀀스를의 `xs` 및의 `ys` 컨트롤 및 컨트롤 및의에 있는 컨트롤 및의 컨트롤 및의에 대 한으로 적용 합니다 `xs` .</span><span class="sxs-lookup"><span data-stu-id="a8c8c-106">Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.</span></span>

```qsharp
operation ApplyOuterCDKMAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a8c8c-107">입력</span><span class="sxs-lookup"><span data-stu-id="a8c8c-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="a8c8c-108">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a8c8c-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a8c8c-109">컨트롤 및 대상을 포함 하는 첫 번째 비트율 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="a8c8c-109">First qubit register, containing controls and targets.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="a8c8c-110">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a8c8c-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a8c8c-111">컨트롤에 영향을 주는 두 번째 비트율 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="a8c8c-111">Second qubit register, contributing to the controls.</span></span>


### <a name="ancilla--qubit"></a><span data-ttu-id="a8c8c-112">ancilla: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a8c8c-112">ancilla : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a8c8c-113">이 작업에 전달 된 RippleCarryAdderCDKM에서 사용 되는 ancilla 이상 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="a8c8c-113">The ancilla qubit used in RippleCarryAdderCDKM passed to this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a8c8c-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a8c8c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="a8c8c-115">참조</span><span class="sxs-lookup"><span data-stu-id="a8c8c-115">References</span></span>

- <span data-ttu-id="a8c8c-116">Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new 퀀텀 ripple and A new, 2004.</span><span class="sxs-lookup"><span data-stu-id="a8c8c-116">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1