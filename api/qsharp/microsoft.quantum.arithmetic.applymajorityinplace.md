---
uid: Microsoft.Quantum.Arithmetic.ApplyMajorityInPlace
title: ApplyMajorityInPlace 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyMajorityInPlace
qsharp.summary: Applies the three-qubit majority operation in-place on a register of qubits.
ms.openlocfilehash: c32d7546fb753f78a72479cec11a6ed09c5e6179
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190737"
---
# <a name="applymajorityinplace-operation"></a><span data-ttu-id="5c7de-102">ApplyMajorityInPlace 작업</span><span class="sxs-lookup"><span data-stu-id="5c7de-102">ApplyMajorityInPlace operation</span></span>

<span data-ttu-id="5c7de-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5c7de-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5c7de-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5c7de-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5c7de-105">은 (는) 다양 한 비트의 레지스터에 세 가지 주요 비트 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c7de-105">Applies the three-qubit majority operation in-place on a register of qubits.</span></span>

```qsharp
operation ApplyMajorityInPlace (output : Qubit, input : Qubit[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="5c7de-106">Description</span><span class="sxs-lookup"><span data-stu-id="5c7de-106">Description</span></span>

<span data-ttu-id="5c7de-107">이 작업을 수행 하면 3 개의 환경에서 과반수 함수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c7de-107">This operation computes the majority function in-place on 3 qubits.</span></span>

<span data-ttu-id="5c7de-108">출력을 $z $로 표시 하 고 입력을 $x $ 및 $y $로 표시 하는 경우 작업은 $ \ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $ 변환을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c7de-108">If we denote output qubit as $z$ and input qubits as $x$ and $y$, the operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="5c7de-109">입력</span><span class="sxs-lookup"><span data-stu-id="5c7de-109">Input</span></span>

### <a name="output--qubit"></a><span data-ttu-id="5c7de-110">출력: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5c7de-110">output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5c7de-111">첫 번째 입력 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7de-111">First input qubit.</span></span> <span data-ttu-id="5c7de-112">출력은 내부에서 계산 된 후에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c7de-112">Note that the output is computed in-place and stored in this qubit.</span></span>


### <a name="input--qubit"></a><span data-ttu-id="5c7de-113">input: [bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5c7de-113">input : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5c7de-114">두 번째 및 세 번째 입력 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7de-114">Second and third input qubits.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5c7de-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5c7de-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

