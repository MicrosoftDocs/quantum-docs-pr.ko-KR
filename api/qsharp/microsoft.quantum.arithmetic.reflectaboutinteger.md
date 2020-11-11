---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: ReflectAboutInteger 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: e034f0a24d5c2f0465ebd1914b28cb8c695d978c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719713"
---
# <a name="reflectaboutinteger-operation"></a><span data-ttu-id="ff947-102">ReflectAboutInteger 작업</span><span class="sxs-lookup"><span data-stu-id="ff947-102">ReflectAboutInteger operation</span></span>

<span data-ttu-id="ff947-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ff947-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ff947-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ff947-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ff947-105">지정 된 기존 정수에 대 한 퀀텀 레지스터를 반영 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff947-105">Reflects a quantum register about a given classical integer.</span></span>

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="ff947-106">Description</span><span class="sxs-lookup"><span data-stu-id="ff947-106">Description</span></span>

<span data-ttu-id="ff947-107">처음에는 $ \ sum_i \ alpha_i \ket{i} $ 상태에 있는 퀀텀 레지스터가 제공 됩니다. 여기서 각 $ \ket{i} $은 정수 $i $를 나타내는 기본 상태 이며 지정 된 정수 $ \ket{j} $, $ $ \ sum_i (-1) ^ {\ delta_ {ij}} \ alpha_i \ket{i} $ $에 대 한 기본 상태에 대 한 레지스터의 상태를 반영 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff947-107">Given a quantum register initially in the state $\sum_i \alpha_i \ket{i}$, where each $\ket{i}$ is a basis state representing an integer $i$, reflects the state of the register about the basis state for a given integer $\ket{j}$, $$ \sum_i (-1)^{ \delta_{ij} } \alpha_i \ket{i} $$</span></span>

## <a name="input"></a><span data-ttu-id="ff947-108">입력</span><span class="sxs-lookup"><span data-stu-id="ff947-108">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="ff947-109">인덱스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ff947-109">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ff947-110">반영할 기준 상태를 인덱싱하는 기존 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="ff947-110">The classical integer indexing the basis state about which to reflect.</span></span>


### <a name="reg--littleendian"></a><span data-ttu-id="ff947-111">reg: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ff947-111">reg : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>





## <a name="output--unit"></a><span data-ttu-id="ff947-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ff947-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ff947-113">설명</span><span class="sxs-lookup"><span data-stu-id="ff947-113">Remarks</span></span>

<span data-ttu-id="ff947-114">추가 보조 비트를 명시적으로 할당 하지 않고이 작업을 내부에서 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff947-114">This operation is implemented in-place, without explicit allocation of additional auxiliary qubits.</span></span>