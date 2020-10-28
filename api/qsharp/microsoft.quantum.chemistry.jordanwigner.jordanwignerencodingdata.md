---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData
title: JordanWignerEncodingData 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerEncodingData
qsharp.summary: Format of data passed from C# to Q# to represent all information for Hamiltonian simulation. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 62988eefa57d8a9e4ed9dcfbdbc6c3b630c6faa2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714050"
---
# <a name="jordanwignerencodingdata-user-defined-type"></a><span data-ttu-id="319f9-102">JordanWignerEncodingData 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="319f9-102">JordanWignerEncodingData user defined type</span></span>

<span data-ttu-id="319f9-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="319f9-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="319f9-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="319f9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="319f9-105">Hamiltonian 시뮬레이션에 대 한 모든 정보를 나타내기 위해 c #에서 Q #으로 전달 되는 데이터의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="319f9-105">Format of data passed from C# to Q# to represent all information for Hamiltonian simulation.</span></span>
<span data-ttu-id="319f9-106">표시 되는 데이터의 의미는 해당 데이터를 수신 하는 알고리즘에 의해 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="319f9-106">The meaning of the data represented is determined by the algorithm that receives it.</span></span>

```qsharp

newtype JordanWignerEncodingData = (Int, Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms, (Int, Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]), Double);
```

