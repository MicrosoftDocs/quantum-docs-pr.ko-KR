---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZTermToPauliGenIdx
title: _ZTermToPauliGenIdx 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZTermToPauliGenIdx
qsharp.summary: Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: 1569ec742778549b8754cdca8b2d9872310e8976
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714176"
---
# <a name="_ztermtopauligenidx-function"></a><span data-ttu-id="483ed-102">_ZTermToPauliGenIdx 함수</span><span class="sxs-lookup"><span data-stu-id="483ed-102">_ZTermToPauliGenIdx function</span></span>

<span data-ttu-id="483ed-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="483ed-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="483ed-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="483ed-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="483ed-105">Z 용어를 설명 하는 GeneratorIndex을 Paulis의 ' GeneratorIndex [] ' 식으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="483ed-105">Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.</span></span>

```qsharp
function _ZTermToPauliGenIdx (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="483ed-106">입력</span><span class="sxs-lookup"><span data-stu-id="483ed-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="483ed-107">용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="483ed-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="483ed-108">`GeneratorIndex` Z 용어를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="483ed-108">`GeneratorIndex` representing a Z term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="483ed-109">출력: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="483ed-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="483ed-110">' GeneratorIndex [] ' Z 용어를 Pauli 용어로 표현 합니다.</span><span class="sxs-lookup"><span data-stu-id="483ed-110">'GeneratorIndex[]' expressing Z term as Pauli terms.</span></span>