---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms
title: JWOptimizedHTerms 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JWOptimizedHTerms
qsharp.summary: Format of data passed from C# to Q# to represent terms of the Hamiltonian. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: d75737f23db84f2a21daff7a0ebcb8ae51feb642
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713966"
---
# <a name="jwoptimizedhterms-user-defined-type"></a><span data-ttu-id="6513f-102">JWOptimizedHTerms 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="6513f-102">JWOptimizedHTerms user defined type</span></span>

<span data-ttu-id="6513f-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="6513f-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="6513f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6513f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6513f-105">Hamiltonian 용어를 나타내기 위해 c #에서 Q #으로 전달 되는 데이터의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="6513f-105">Format of data passed from C# to Q# to represent terms of the Hamiltonian.</span></span>
<span data-ttu-id="6513f-106">표시 되는 데이터의 의미는 해당 데이터를 수신 하는 알고리즘에 의해 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6513f-106">The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype JWOptimizedHTerms = (Microsoft.Quantum.Chemistry.HTerm[], Microsoft.Quantum.Chemistry.HTerm[], Microsoft.Quantum.Chemistry.HTerm[], Microsoft.Quantum.Chemistry.HTerm[]);
```

