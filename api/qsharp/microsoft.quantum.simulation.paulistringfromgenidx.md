---
uid: Microsoft.Quantum.Simulation.PauliStringFromGenIdx
title: PauliStringFromGenIdx 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliStringFromGenIdx
qsharp.summary: Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 048f91411099d24f3c0c5fd8ae3703779e7ab8a2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847902"
---
# <a name="paulistringfromgenidx-function"></a><span data-ttu-id="8d912-102">PauliStringFromGenIdx 함수</span><span class="sxs-lookup"><span data-stu-id="8d912-102">PauliStringFromGenIdx function</span></span>

<span data-ttu-id="8d912-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="8d912-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="8d912-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8d912-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8d912-105">에서 설명 하는 Pauli 문자열 및 해당의 해당 비트 인덱스를 추출 `GeneratorIndex` 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d912-105">Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliStringFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : (Pauli[], Int[])
```


## <a name="input"></a><span data-ttu-id="8d912-106">입력</span><span class="sxs-lookup"><span data-stu-id="8d912-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="8d912-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="8d912-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="8d912-108">`GeneratorIndex` Pauli 용어를 인코딩하는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8d912-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--pauliint"></a><span data-ttu-id="8d912-109">출력: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="8d912-109">Output : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

<span data-ttu-id="8d912-110">에서 설명 하는 용어에 대 한 Pauli 문자열 및이를 실행 하 `GeneratorIndex` 는 것이 적용 되는 요소의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="8d912-110">The Pauli string of the term described by a `GeneratorIndex`, and indices to the qubits it acts on.</span></span>