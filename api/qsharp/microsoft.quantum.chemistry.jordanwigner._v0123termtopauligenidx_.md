---
uid: Microsoft.Quantum.Chemistry.JordanWigner._V0123TermToPauliGenIdx_
title: _V0123TermToPauliGenIdx_ 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _V0123TermToPauliGenIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQRS term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: b522691d6826933122e2ebac051b15e35b9902e2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714204"
---
# <a name="_v0123termtopauligenidx_-function"></a><span data-ttu-id="030f7-102">_V0123TermToPauliGenIdx_ 함수</span><span class="sxs-lookup"><span data-stu-id="030f7-102">_V0123TermToPauliGenIdx_ function</span></span>

<span data-ttu-id="030f7-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="030f7-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="030f7-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="030f7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="030f7-105">PQRS 용어를 설명 하는 GeneratorIndex을 Paulis의 식 ' GeneratorIndex [] '로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="030f7-105">Converts a GeneratorIndex describing a PQRS term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _V0123TermToPauliGenIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="030f7-106">입력</span><span class="sxs-lookup"><span data-stu-id="030f7-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="030f7-107">용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="030f7-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="030f7-108">`GeneratorIndex` PQRS 용어를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="030f7-108">`GeneratorIndex` representing a PQRS term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="030f7-109">출력: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="030f7-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="030f7-110">PQRS term을 Pauli 용어로 표현 하는 ' GeneratorIndex [] '</span><span class="sxs-lookup"><span data-stu-id="030f7-110">'GeneratorIndex[]' expressing PQRS term as Pauli terms.</span></span>