---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedGeneratorSystem
title: JWOptimizedGeneratorSystem 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: 8e4c06b9447a2e5838cced876febee03d1af5315
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710781"
---
# <a name="jwoptimizedgeneratorsystem-function"></a><span data-ttu-id="41819-102">JWOptimizedGeneratorSystem 함수</span><span class="sxs-lookup"><span data-stu-id="41819-102">JWOptimizedGeneratorSystem function</span></span>

<span data-ttu-id="41819-103">네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="41819-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="41819-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="41819-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="41819-105">에 설명 된 Hamiltonian를 `JWOptimizedHTerms` `GeneratorSystem` `GeneratorIndex` 이 파일에 정의 된 규칙의 용어로 표현 된로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="41819-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.</span></span>

```qsharp
function JWOptimizedGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="41819-106">입력</span><span class="sxs-lookup"><span data-stu-id="41819-106">Input</span></span>

### <a name="data--jwoptimizedhterms"></a><span data-ttu-id="41819-107">데이터: [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span><span class="sxs-lookup"><span data-stu-id="41819-107">data : [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span></span>

<span data-ttu-id="41819-108">형식의 Hamiltonian에 대 한 설명 `JWOptimizedHTerms` 입니다.</span><span class="sxs-lookup"><span data-stu-id="41819-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="41819-109">출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="41819-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="41819-110">Hamiltonian의 표현 `GeneratorSystem` 입니다.</span><span class="sxs-lookup"><span data-stu-id="41819-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>