---
uid: Microsoft.Quantum.Simulation.PauliCoefficientFromGenIdx
title: PauliCoefficientFromGenIdx 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliCoefficientFromGenIdx
qsharp.summary: Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: eb4f7a538e85ade4b095aa3ea5eab4448eda2491
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847985"
---
# <a name="paulicoefficientfromgenidx-function"></a><span data-ttu-id="2bb0b-102">PauliCoefficientFromGenIdx 함수</span><span class="sxs-lookup"><span data-stu-id="2bb0b-102">PauliCoefficientFromGenIdx function</span></span>

<span data-ttu-id="2bb0b-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="2bb0b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="2bb0b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2bb0b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2bb0b-105">에서 설명 하는 Pauli 용어의 계수를 추출 `GeneratorIndex` 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bb0b-105">Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliCoefficientFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Double
```


## <a name="input"></a><span data-ttu-id="2bb0b-106">입력</span><span class="sxs-lookup"><span data-stu-id="2bb0b-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="2bb0b-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="2bb0b-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="2bb0b-108">`GeneratorIndex` Pauli 용어를 인코딩하는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="2bb0b-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--double"></a><span data-ttu-id="2bb0b-109">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2bb0b-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2bb0b-110">에 설명 된 용어의 계수입니다 `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="2bb0b-110">The coefficient of the term described by a `GeneratorIndex`.</span></span>