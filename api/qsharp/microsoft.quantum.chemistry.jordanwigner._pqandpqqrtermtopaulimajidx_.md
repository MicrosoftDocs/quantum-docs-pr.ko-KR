---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQandPQQRTermToPauliMajIdx_
title: _PQandPQQRTermToPauliMajIdx_ 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQandPQQRTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ or PQQR term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 4ba13f42064d9311ffb29dbd9363aa3be978e702
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714365"
---
# <a name="_pqandpqqrtermtopaulimajidx_-function"></a><span data-ttu-id="df710-102">_PQandPQQRTermToPauliMajIdx_ 함수</span><span class="sxs-lookup"><span data-stu-id="df710-102">_PQandPQQRTermToPauliMajIdx_ function</span></span>

<span data-ttu-id="df710-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="df710-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="df710-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="df710-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="df710-105">PQ 또는 PQQR 항을 설명 하는 GeneratorIndex을 Paulis 라는 식의 ' GeneratorIndex [] ' 식으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="df710-105">Converts a GeneratorIndex describing a PQ or PQQR term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _PQandPQQRTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a><span data-ttu-id="df710-106">입력</span><span class="sxs-lookup"><span data-stu-id="df710-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="df710-107">용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="df710-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="df710-108">`GeneratorIndex` PQ 또는 PQQR term을 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="df710-108">`GeneratorIndex` representing a PQ or PQQR term.</span></span>



## <a name="output--optimizedbetermindex"></a><span data-ttu-id="df710-109">출력: [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span><span class="sxs-lookup"><span data-stu-id="df710-109">Output : [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span></span>

<span data-ttu-id="df710-110">PQ 또는 PQQR 항을 Pauli 용어로 표현 하는 ' GeneratorIndex [] '</span><span class="sxs-lookup"><span data-stu-id="df710-110">'GeneratorIndex[]' expressing PQ or PQQR term as Pauli terms.</span></span>