---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZZTermToPauliMajIdx_
title: _ZZTermToPauliMajIdx_ 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZZTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a ZZ term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: 8c9223d54585f91e1616021bf0643e558d57589c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714127"
---
# <a name="_zztermtopaulimajidx_-function"></a><span data-ttu-id="e0ebf-102">_ZZTermToPauliMajIdx_ 함수</span><span class="sxs-lookup"><span data-stu-id="e0ebf-102">_ZZTermToPauliMajIdx_ function</span></span>

<span data-ttu-id="e0ebf-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="e0ebf-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="e0ebf-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e0ebf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e0ebf-105">ZZ 용어를 설명 하는 GeneratorIndex을 Paulis 라는 식의 ' GeneratorIndex [] ' 식으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0ebf-105">Converts a GeneratorIndex describing a ZZ term to an expression 'GeneratorIndex[]' in terms of Paulis.</span></span>

```qsharp
function _ZZTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a><span data-ttu-id="e0ebf-106">입력</span><span class="sxs-lookup"><span data-stu-id="e0ebf-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="e0ebf-107">용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="e0ebf-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="e0ebf-108">`GeneratorIndex` ZZ 용어를 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="e0ebf-108">`GeneratorIndex` representing a ZZ term.</span></span>



## <a name="output--optimizedbetermindex"></a><span data-ttu-id="e0ebf-109">출력: [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span><span class="sxs-lookup"><span data-stu-id="e0ebf-109">Output : [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span></span>

<span data-ttu-id="e0ebf-110">' GeneratorIndex [] '는 ZZ 용어를 Pauli 용어로 표현 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0ebf-110">'GeneratorIndex[]' expressing ZZ term as Pauli terms.</span></span>