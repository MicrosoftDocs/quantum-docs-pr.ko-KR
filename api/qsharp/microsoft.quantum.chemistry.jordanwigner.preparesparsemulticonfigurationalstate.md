---
uid: Microsoft.Quantum.Chemistry.JordanWigner.PrepareSparseMultiConfigurationalState
title: PrepareSparseMultiConfigurationalState 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: PrepareSparseMultiConfigurationalState
qsharp.summary: Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.
ms.openlocfilehash: 1182f79a33784cdb49cb13db5cc97a0a45e59f9f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713847"
---
# <a name="preparesparsemulticonfigurationalstate-operation"></a><span data-ttu-id="78b16-102">PrepareSparseMultiConfigurationalState 작업</span><span class="sxs-lookup"><span data-stu-id="78b16-102">PrepareSparseMultiConfigurationalState operation</span></span>

<span data-ttu-id="78b16-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="78b16-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="78b16-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="78b16-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="78b16-105">초기 평가판 상태에 excitations를 추가 하 여 구성의 스파스 상태 준비 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="78b16-105">Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.</span></span>

```qsharp
operation PrepareSparseMultiConfigurationalState (initialStatePreparation : (Qubit[] => Unit), excitations : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="78b16-106">입력</span><span class="sxs-lookup"><span data-stu-id="78b16-106">Input</span></span>

### <a name="initialstatepreparation--qubit--unit"></a><span data-ttu-id="78b16-107">initialStatePreparation: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="78b16-107">initialStatePreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="78b16-108">초기 평가판 상태를 준비 하기 위한 단일.</span><span class="sxs-lookup"><span data-stu-id="78b16-108">Unitary to prepare initial trial state.</span></span>


### <a name="excitations--jordanwignerinputstate"></a><span data-ttu-id="78b16-109">excitations: [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span><span class="sxs-lookup"><span data-stu-id="78b16-109">excitations : [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span></span>

<span data-ttu-id="78b16-110">Excitation의 진폭으로 표시 되는 초기 평가판 상태와 excitation가 작동 하는 Excitations 비트 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="78b16-110">Excitations of initial trial state represented by the amplitude of the excitation and the qubit indices the excitation acts on.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="78b16-111">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="78b16-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="78b16-112">Hamiltonian의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="78b16-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="78b16-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="78b16-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

