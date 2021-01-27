---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: IntToPauli 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: 76f482b86ff4a27b6e6ce6ae4ec3d59422563f12
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842241"
---
# <a name="inttopauli-function"></a><span data-ttu-id="417c6-102">IntToPauli 함수</span><span class="sxs-lookup"><span data-stu-id="417c6-102">IntToPauli function</span></span>

<span data-ttu-id="417c6-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="417c6-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="417c6-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="417c6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="417c6-105">정수를 단일 값 비트 Pauli 연산자로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c6-105">Converts a integer to a single-qubit Pauli operator.</span></span>

```qsharp
function IntToPauli (idx : Int) : Pauli
```


## <a name="input"></a><span data-ttu-id="417c6-106">입력</span><span class="sxs-lookup"><span data-stu-id="417c6-106">Input</span></span>

### <a name="idx--int"></a><span data-ttu-id="417c6-107">idx: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="417c6-107">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="417c6-108">`0..3`Pauli 연산자로 변환할 범위의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="417c6-108">Integer in the range `0..3` to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="417c6-109">출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="417c6-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="417c6-110">`Pauli`에서 제공 하는 연산자 `[PauliI, PauliX, PauliY, PauliZ][idx]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="417c6-110">A `Pauli` operator given by `[PauliI, PauliX, PauliY, PauliZ][idx]`.</span></span>