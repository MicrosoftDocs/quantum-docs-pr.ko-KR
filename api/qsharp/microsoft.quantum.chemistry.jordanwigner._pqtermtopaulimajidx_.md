---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQTermToPauliMajIdx_
title: _PQTermToPauliMajIdx_ 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: b75e9b61e05d6451bab378108c75b10334ac1e44
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714330"
---
# <a name="_pqtermtopaulimajidx_-function"></a><span data-ttu-id="2aa43-102">_PQTermToPauliMajIdx_ 함수</span><span class="sxs-lookup"><span data-stu-id="2aa43-102">_PQTermToPauliMajIdx_ function</span></span>

<span data-ttu-id="2aa43-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="2aa43-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="2aa43-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2aa43-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2aa43-105">PQ 용어를 설명 하는 GeneratorIndex을 Paulis의 식 ' GeneratorIndex [] '로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa43-105">Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _PQTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a><span data-ttu-id="2aa43-106">입력</span><span class="sxs-lookup"><span data-stu-id="2aa43-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="2aa43-107">용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="2aa43-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="2aa43-108">`GeneratorIndex` PQ 용어를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa43-108">`GeneratorIndex` representing a PQ term.</span></span>



## <a name="output--optimizedbetermindex"></a><span data-ttu-id="2aa43-109">출력: [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span><span class="sxs-lookup"><span data-stu-id="2aa43-109">Output : [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span></span>

<span data-ttu-id="2aa43-110">PQ term을 Pauli 용어로 표현 하는 ' GeneratorIndex [] '</span><span class="sxs-lookup"><span data-stu-id="2aa43-110">'GeneratorIndex[]' expressing PQ term as Pauli terms.</span></span>