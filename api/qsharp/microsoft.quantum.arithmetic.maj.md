---
uid: Microsoft.Quantum.Arithmetic.MAJ
title: MAJ 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MAJ
qsharp.summary: This applies the in-place majority operation to 3 qubits.
ms.openlocfilehash: c1801d1d7ed04ead11b672f24d44a94989cf8f1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721016"
---
# <a name="maj-operation"></a><span data-ttu-id="34793-102">MAJ 작업</span><span class="sxs-lookup"><span data-stu-id="34793-102">MAJ operation</span></span>

<span data-ttu-id="34793-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="34793-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="34793-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="34793-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="34793-105">이는 내부 과반수 작업을 3 개의 비트에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="34793-105">This applies the in-place majority operation to 3 qubits.</span></span>

```qsharp
operation MAJ (input0 : Qubit, input1 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="34793-106">Description</span><span class="sxs-lookup"><span data-stu-id="34793-106">Description</span></span>

<span data-ttu-id="34793-107">$ \Ket{z} $로 대상의 상태를 표시 하 고 입력의 입력 상태를 $ \ket{x} $ 및 $ \ket{y} $로 표시 하는 경우이 작업은 다음 변환을 수행 합니다. $ \ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="34793-107">If we denote the state of the target qubit as $\ket{z}$, and input states of the input qubits as $\ket{x}$ and $\ket{y}$, then this operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="34793-108">입력</span><span class="sxs-lookup"><span data-stu-id="34793-108">Input</span></span>

### <a name="input0--qubit"></a><span data-ttu-id="34793-109">input0: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="34793-109">input0 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="34793-110">첫 번째 입력 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="34793-110">The first input qubit.</span></span>


### <a name="input1--qubit"></a><span data-ttu-id="34793-111">input1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="34793-111">input1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="34793-112">두 번째 입력 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="34793-112">The second input qubit.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="34793-113">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="34793-113">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="34793-114">과반수 함수가 적용 될 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="34793-114">A qubit onto which the majority function will be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="34793-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="34793-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

