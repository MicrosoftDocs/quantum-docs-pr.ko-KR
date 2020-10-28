---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerClusterOperatorGeneratorSystem
title: JordanWignerClusterOperatorGeneratorSystem 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerClusterOperatorGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: c75dcd655dafb7048f61f4b07b852cc5f437275d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714057"
---
# <a name="jordanwignerclusteroperatorgeneratorsystem-function"></a><span data-ttu-id="52e1a-102">JordanWignerClusterOperatorGeneratorSystem 함수</span><span class="sxs-lookup"><span data-stu-id="52e1a-102">JordanWignerClusterOperatorGeneratorSystem function</span></span>

<span data-ttu-id="52e1a-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="52e1a-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="52e1a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="52e1a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="52e1a-105">에 설명 된 Hamiltonian를 `JWOptimizedHTerms` `GeneratorSystem` `GeneratorIndex` 이 파일에 정의 된 규칙의 용어로 표현 된로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="52e1a-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.</span></span>

```qsharp
function JordanWignerClusterOperatorGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="52e1a-106">입력</span><span class="sxs-lookup"><span data-stu-id="52e1a-106">Input</span></span>

### <a name="data--jordanwignerinputstate"></a><span data-ttu-id="52e1a-107">데이터: [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span><span class="sxs-lookup"><span data-stu-id="52e1a-107">data : [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span></span>

<span data-ttu-id="52e1a-108">형식의 Hamiltonian에 대 한 설명 `JWOptimizedHTerms` 입니다.</span><span class="sxs-lookup"><span data-stu-id="52e1a-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="52e1a-109">출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="52e1a-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="52e1a-110">Hamiltonian의 표현 `GeneratorSystem` 입니다.</span><span class="sxs-lookup"><span data-stu-id="52e1a-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>