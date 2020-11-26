---
uid: Microsoft.Quantum.Simulation.PauliCoefficientFromGenIdx
title: PauliCoefficientFromGenIdx 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliCoefficientFromGenIdx
qsharp.summary: Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 59ddadabb5c77cdb0d2e3620a09433992e85f663
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225060"
---
# <a name="paulicoefficientfromgenidx-function"></a><span data-ttu-id="92177-102">PauliCoefficientFromGenIdx 함수</span><span class="sxs-lookup"><span data-stu-id="92177-102">PauliCoefficientFromGenIdx function</span></span>

<span data-ttu-id="92177-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="92177-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="92177-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="92177-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="92177-105">에서 설명 하는 Pauli 용어의 계수를 추출 `GeneratorIndex` 합니다.</span><span class="sxs-lookup"><span data-stu-id="92177-105">Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliCoefficientFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Double
```


## <a name="input"></a><span data-ttu-id="92177-106">입력</span><span class="sxs-lookup"><span data-stu-id="92177-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="92177-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="92177-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="92177-108">`GeneratorIndex` Pauli 용어를 인코딩하는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="92177-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--double"></a><span data-ttu-id="92177-109">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="92177-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="92177-110">에 설명 된 용어의 계수입니다 `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="92177-110">The coefficient of the term described by a `GeneratorIndex`.</span></span>