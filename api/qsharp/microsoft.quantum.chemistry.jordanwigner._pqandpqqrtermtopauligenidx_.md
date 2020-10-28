---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQandPQQRTermToPauliGenIdx_
title: _PQandPQQRTermToPauliGenIdx_ 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQandPQQRTermToPauliGenIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ or PQQR term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 44a6d6b63d2f6bc8b628603e78931570d1ec22eb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714372"
---
# <a name="_pqandpqqrtermtopauligenidx_-function"></a><span data-ttu-id="a6081-102">_PQandPQQRTermToPauliGenIdx_ 함수</span><span class="sxs-lookup"><span data-stu-id="a6081-102">_PQandPQQRTermToPauliGenIdx_ function</span></span>

<span data-ttu-id="a6081-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="a6081-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="a6081-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a6081-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a6081-105">PQ 또는 PQQR 항을 설명 하는 GeneratorIndex을 Paulis 라는 식의 ' GeneratorIndex [] ' 식으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6081-105">Converts a GeneratorIndex describing a PQ or PQQR term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _PQandPQQRTermToPauliGenIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="a6081-106">입력</span><span class="sxs-lookup"><span data-stu-id="a6081-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="a6081-107">용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="a6081-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="a6081-108">`GeneratorIndex` PQ 또는 PQQR term을 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="a6081-108">`GeneratorIndex` representing a PQ or PQQR term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="a6081-109">출력: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="a6081-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="a6081-110">PQ 또는 PQQR 항을 Pauli 용어로 표현 하는 ' GeneratorIndex [] '</span><span class="sxs-lookup"><span data-stu-id="a6081-110">'GeneratorIndex[]' expressing PQ or PQQR term as Pauli terms.</span></span>