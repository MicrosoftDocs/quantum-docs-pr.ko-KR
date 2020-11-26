---
uid: Microsoft.Quantum.Simulation.PauliStringFromGenIdx
title: PauliStringFromGenIdx 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliStringFromGenIdx
qsharp.summary: Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: a937dc648c5de5a5f6de7da996448af497b92185
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230313"
---
# <a name="paulistringfromgenidx-function"></a><span data-ttu-id="2f46a-102">PauliStringFromGenIdx 함수</span><span class="sxs-lookup"><span data-stu-id="2f46a-102">PauliStringFromGenIdx function</span></span>

<span data-ttu-id="2f46a-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="2f46a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="2f46a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2f46a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2f46a-105">에서 설명 하는 Pauli 문자열 및 해당의 해당 비트 인덱스를 추출 `GeneratorIndex` 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f46a-105">Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliStringFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : (Pauli[], Int[])
```


## <a name="input"></a><span data-ttu-id="2f46a-106">입력</span><span class="sxs-lookup"><span data-stu-id="2f46a-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="2f46a-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="2f46a-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="2f46a-108">`GeneratorIndex` Pauli 용어를 인코딩하는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="2f46a-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--pauliint"></a><span data-ttu-id="2f46a-109">출력: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="2f46a-109">Output : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

<span data-ttu-id="2f46a-110">에서 설명 하는 용어에 대 한 Pauli 문자열 및이를 실행 하 `GeneratorIndex` 는 것이 적용 되는 요소의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="2f46a-110">The Pauli string of the term described by a `GeneratorIndex`, and indices to the qubits it acts on.</span></span>