---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: MAJ 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: 68236f1deeb409a01152d4b7e854202a1134314e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846541"
---
# <a name="maj-operation"></a><span data-ttu-id="07989-102">MAJ 작업</span><span class="sxs-lookup"><span data-stu-id="07989-102">MAJ operation</span></span>

<span data-ttu-id="07989-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="07989-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="07989-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="07989-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="07989-105">이는 내부 과반수 작업을 3 개의 비트에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07989-105">This applies the in-place majority operation to 3 qubits.</span></span>

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="07989-106">설명</span><span class="sxs-lookup"><span data-stu-id="07989-106">Description</span></span>

<span data-ttu-id="07989-107">$ \Ket{z} $로 대상의 상태를 표시 하 고 입력의 입력 상태를 $ \ket{x} $ 및 $ \ket{y} $로 표시 하는 경우이 작업은 다음 변환을 수행 합니다. $ \ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="07989-107">If we denote the state of the target qubit as $\ket{z}$, and input states of the input qubits as $\ket{x}$ and $\ket{y}$, then this operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="07989-108">입력</span><span class="sxs-lookup"><span data-stu-id="07989-108">Input</span></span>

### <a name="input0--qubit"></a><span data-ttu-id="07989-109">input0: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="07989-109">input0 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="07989-110">첫 번째 입력 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="07989-110">The first input qubit.</span></span>


### <a name="input1--qubit"></a><span data-ttu-id="07989-111">input1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="07989-111">input1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="07989-112">두 번째 입력 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="07989-112">The second input qubit.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="07989-113">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="07989-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="07989-114">과반수 함수가 적용 될 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="07989-114">A qubit onto which the majority function will be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="07989-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="07989-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

