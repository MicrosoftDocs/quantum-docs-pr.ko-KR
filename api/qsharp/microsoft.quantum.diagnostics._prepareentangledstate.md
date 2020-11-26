---
uid: Microsoft.Quantum.Diagnostics._prepareEntangledState
title: _prepareEntangledState 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _prepareEntangledState
qsharp.summary: >-
  Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers. All qubits must start in the |0⟩ state.

  The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.
ms.openlocfilehash: 97a55b4bb85095c7d8e8432dfcd1c6d6f7e93cdc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223938"
---
# <a name="_prepareentangledstate-operation"></a><span data-ttu-id="7681f-102">_prepareEntangledState 작업</span><span class="sxs-lookup"><span data-stu-id="7681f-102">_prepareEntangledState operation</span></span>

<span data-ttu-id="7681f-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="7681f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="7681f-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="7681f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="7681f-105">두 개의 레지스터가 지정 된 경우는 각 레지스터의 각 비트 쌍 간에 최대 entangled 상태를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="7681f-105">Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers.</span></span>
<span data-ttu-id="7681f-106">모든 비트는 | 0 ⟩ 상태에서 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7681f-106">All qubits must start in the |0⟩ state.</span></span>

<span data-ttu-id="7681f-107">결과적으로 각 레지스터의 해당 \bra{\ 쌍은 $ beta_ {00} } \ket{\ beta_ {00} } $에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7681f-107">The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.</span></span>

```qsharp
operation _prepareEntangledState (left : Qubit[], right : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7681f-108">입력</span><span class="sxs-lookup"><span data-stu-id="7681f-108">Input</span></span>

### <a name="left--qubit"></a><span data-ttu-id="7681f-109">left: 좌 [bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7681f-109">left : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7681f-110">$ \Ket{0\cdots 0} $ 상태의 고 비트 배열</span><span class="sxs-lookup"><span data-stu-id="7681f-110">A qubit array in the $\ket{0\cdots 0}$ state</span></span>


### <a name="right--qubit"></a><span data-ttu-id="7681f-111">right: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7681f-111">right : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7681f-112">$ \Ket{0\cdots 0} $ 상태의 고 비트 배열</span><span class="sxs-lookup"><span data-stu-id="7681f-112">A qubit array in the $\ket{0\cdots 0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="7681f-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7681f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

