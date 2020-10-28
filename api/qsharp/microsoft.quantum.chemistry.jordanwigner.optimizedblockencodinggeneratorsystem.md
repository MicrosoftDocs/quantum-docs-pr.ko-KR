---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBlockEncodingGeneratorSystem
title: OptimizedBlockEncodingGeneratorSystem 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBlockEncodingGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the Pauli `GeneratorIndex`.
ms.openlocfilehash: c3e48cb5dde36b694a5b16f25333cf0dad6c0f61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713896"
---
# <a name="optimizedblockencodinggeneratorsystem-function"></a><span data-ttu-id="96657-102">OptimizedBlockEncodingGeneratorSystem 함수</span><span class="sxs-lookup"><span data-stu-id="96657-102">OptimizedBlockEncodingGeneratorSystem function</span></span>

<span data-ttu-id="96657-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="96657-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="96657-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="96657-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="96657-105">에 설명 된 Hamiltonian를 `JWOptimizedHTerms` Pauli로 표현 된로 변환 합니다 `GeneratorSystem` `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="96657-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the Pauli `GeneratorIndex`.</span></span>

```qsharp
function OptimizedBlockEncodingGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem
```


## <a name="input"></a><span data-ttu-id="96657-106">입력</span><span class="sxs-lookup"><span data-stu-id="96657-106">Input</span></span>

### <a name="data--jwoptimizedhterms"></a><span data-ttu-id="96657-107">데이터: [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span><span class="sxs-lookup"><span data-stu-id="96657-107">data : [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span></span>

<span data-ttu-id="96657-108">형식의 Hamiltonian에 대 한 설명 `JWOptimizedHTerms` 입니다.</span><span class="sxs-lookup"><span data-stu-id="96657-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--optimizedbegeneratorsystem"></a><span data-ttu-id="96657-109">출력: [OptimizedBEGeneratorSystem](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="96657-109">Output : [OptimizedBEGeneratorSystem](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem)</span></span>

<span data-ttu-id="96657-110">Hamiltonian의 표현 `GeneratorSystem` 입니다.</span><span class="sxs-lookup"><span data-stu-id="96657-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>