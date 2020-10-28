---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: IntToPauli 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: f0f1186f14a0dc30bb34bd29f148cdc830fd1337
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724848"
---
# <a name="inttopauli-function"></a><span data-ttu-id="863d0-102">IntToPauli 함수</span><span class="sxs-lookup"><span data-stu-id="863d0-102">IntToPauli function</span></span>

<span data-ttu-id="863d0-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="863d0-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="863d0-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="863d0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="863d0-105">정수를 단일 값 비트 Pauli 연산자로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="863d0-105">Converts a integer to a single-qubit Pauli operator.</span></span>

```qsharp
function IntToPauli (idx : Int) : Pauli
```


## <a name="input"></a><span data-ttu-id="863d0-106">입력</span><span class="sxs-lookup"><span data-stu-id="863d0-106">Input</span></span>

### <a name="idx--int"></a><span data-ttu-id="863d0-107">idx: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="863d0-107">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="863d0-108">`0..3`Pauli 연산자로 변환할 범위의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="863d0-108">Integer in the range `0..3` to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="863d0-109">출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="863d0-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="863d0-110">`Pauli`에서 제공 하는 연산자 `[PauliI, PauliX, PauliY, PauliZ][idx]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="863d0-110">A `Pauli` operator given by `[PauliI, PauliX, PauliY, PauliZ][idx]`.</span></span>