---
uid: Microsoft.Quantum.Simulation.PauliCoefficientFromGenIdx
title: PauliCoefficientFromGenIdx 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliCoefficientFromGenIdx
qsharp.summary: Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 5bbc8d6113fb36bfd4050b98538bb61bbac02185
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720212"
---
# <a name="paulicoefficientfromgenidx-function"></a><span data-ttu-id="916d0-102">PauliCoefficientFromGenIdx 함수</span><span class="sxs-lookup"><span data-stu-id="916d0-102">PauliCoefficientFromGenIdx function</span></span>

<span data-ttu-id="916d0-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="916d0-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="916d0-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="916d0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="916d0-105">에서 설명 하는 Pauli 용어의 계수를 추출 `GeneratorIndex` 합니다.</span><span class="sxs-lookup"><span data-stu-id="916d0-105">Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliCoefficientFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Double
```


## <a name="input"></a><span data-ttu-id="916d0-106">입력</span><span class="sxs-lookup"><span data-stu-id="916d0-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="916d0-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="916d0-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="916d0-108">`GeneratorIndex` Pauli 용어를 인코딩하는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="916d0-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--double"></a><span data-ttu-id="916d0-109">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="916d0-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="916d0-110">에 설명 된 용어의 계수입니다 `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="916d0-110">The coefficient of the term described by a `GeneratorIndex`.</span></span>