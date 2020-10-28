---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerGeneratorSystem
title: JordanWignerGeneratorSystem 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: 30da4129278f83633c2cc76489c7c81304a1f565
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713987"
---
# <a name="jordanwignergeneratorsystem-function"></a><span data-ttu-id="c2ac0-102">JordanWignerGeneratorSystem 함수</span><span class="sxs-lookup"><span data-stu-id="c2ac0-102">JordanWignerGeneratorSystem function</span></span>

<span data-ttu-id="c2ac0-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="c2ac0-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="c2ac0-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c2ac0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c2ac0-105">에 설명 된 Hamiltonian를 `JWOptimizedHTerms` `GeneratorSystem` `GeneratorIndex` 이 파일에 정의 된 규칙의 용어로 표현 된로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.</span></span>

```qsharp
function JordanWignerGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="c2ac0-106">입력</span><span class="sxs-lookup"><span data-stu-id="c2ac0-106">Input</span></span>

### <a name="data--jwoptimizedhterms"></a><span data-ttu-id="c2ac0-107">데이터: [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span><span class="sxs-lookup"><span data-stu-id="c2ac0-107">data : [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span></span>

<span data-ttu-id="c2ac0-108">형식의 Hamiltonian에 대 한 설명 `JWOptimizedHTerms` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="c2ac0-109">출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="c2ac0-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="c2ac0-110">Hamiltonian의 표현 `GeneratorSystem` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c2ac0-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>