---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBlockEncodingGeneratorSystem
title: OptimizedBlockEncodingGeneratorSystem 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBlockEncodingGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the Pauli `GeneratorIndex`.
ms.openlocfilehash: 1d59c7655b5534465717dd816848011527df4a42
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214588"
---
# <a name="optimizedblockencodinggeneratorsystem-function"></a><span data-ttu-id="f4af5-102">OptimizedBlockEncodingGeneratorSystem 함수</span><span class="sxs-lookup"><span data-stu-id="f4af5-102">OptimizedBlockEncodingGeneratorSystem function</span></span>

<span data-ttu-id="f4af5-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="f4af5-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="f4af5-104">패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f4af5-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="f4af5-105">에 설명 된 Hamiltonian를 `JWOptimizedHTerms` Pauli로 표현 된로 변환 합니다 `GeneratorSystem` `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="f4af5-105">Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the Pauli `GeneratorIndex`.</span></span>

```qsharp
function OptimizedBlockEncodingGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem
```


## <a name="input"></a><span data-ttu-id="f4af5-106">입력</span><span class="sxs-lookup"><span data-stu-id="f4af5-106">Input</span></span>

### <a name="data--jwoptimizedhterms"></a><span data-ttu-id="f4af5-107">데이터: [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span><span class="sxs-lookup"><span data-stu-id="f4af5-107">data : [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)</span></span>

<span data-ttu-id="f4af5-108">형식의 Hamiltonian에 대 한 설명 `JWOptimizedHTerms` 입니다.</span><span class="sxs-lookup"><span data-stu-id="f4af5-108">Description of Hamiltonian in `JWOptimizedHTerms` format.</span></span>



## <a name="output--optimizedbegeneratorsystem"></a><span data-ttu-id="f4af5-109">출력: [OptimizedBEGeneratorSystem](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="f4af5-109">Output : [OptimizedBEGeneratorSystem](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem)</span></span>

<span data-ttu-id="f4af5-110">Hamiltonian의 표현 `GeneratorSystem` 입니다.</span><span class="sxs-lookup"><span data-stu-id="f4af5-110">Representation of Hamiltonian as `GeneratorSystem`.</span></span>