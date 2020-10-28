---
uid: Microsoft.Quantum.Diagnostics._prepareEntangledState
title: _prepareEntangledState 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _prepareEntangledState
qsharp.summary: >-
  Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers. All qubits must start in the |0⟩ state.

  The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.
ms.openlocfilehash: 384dad5905cec50b500028e1bc352a742122b299
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713133"
---
# <a name="_prepareentangledstate-operation"></a><span data-ttu-id="a92cc-102">_prepareEntangledState 작업</span><span class="sxs-lookup"><span data-stu-id="a92cc-102">_prepareEntangledState operation</span></span>

<span data-ttu-id="a92cc-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="a92cc-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="a92cc-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a92cc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a92cc-105">두 개의 레지스터가 지정 된 경우는 각 레지스터의 각 비트 쌍 간에 최대 entangled 상태를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92cc-105">Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers.</span></span>
<span data-ttu-id="a92cc-106">모든 비트는 | 0 ⟩ 상태에서 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92cc-106">All qubits must start in the |0⟩ state.</span></span>

<span data-ttu-id="a92cc-107">결과적으로 각 레지스터의 해당 \bra{\ 쌍은 $ beta_ {00} } \ket{\ beta_ {00} } $에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a92cc-107">The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.</span></span>

```qsharp
operation _prepareEntangledState (left : Qubit[], right : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="a92cc-108">입력</span><span class="sxs-lookup"><span data-stu-id="a92cc-108">Input</span></span>

### <a name="left--qubit"></a><span data-ttu-id="a92cc-109">left: 좌 [bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a92cc-109">left : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a92cc-110">$ \Ket{0\cdots 0} $ 상태의 고 비트 배열</span><span class="sxs-lookup"><span data-stu-id="a92cc-110">A qubit array in the $\ket{0\cdots 0}$ state</span></span>


### <a name="right--qubit"></a><span data-ttu-id="a92cc-111">right: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a92cc-111">right : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a92cc-112">$ \Ket{0\cdots 0} $ 상태의 고 비트 배열</span><span class="sxs-lookup"><span data-stu-id="a92cc-112">A qubit array in the $\ket{0\cdots 0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="a92cc-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a92cc-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

