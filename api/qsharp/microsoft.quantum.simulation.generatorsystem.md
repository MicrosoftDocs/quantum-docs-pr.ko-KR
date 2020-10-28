---
uid: Microsoft.Quantum.Simulation.GeneratorSystem
title: GeneratorSystem 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorSystem
qsharp.summary: >-
  Represents a collection of `GeneratorIndex`es.

  We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.
ms.openlocfilehash: c03caf99b197410c7fa15021c8acaaf55a728781
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724561"
---
# <a name="generatorsystem-user-defined-type"></a><span data-ttu-id="1e768-102">GeneratorSystem 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="1e768-102">GeneratorSystem user defined type</span></span>

<span data-ttu-id="1e768-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="1e768-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="1e768-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1e768-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1e768-105">Es의 컬렉션을 나타냅니다 `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="1e768-105">Represents a collection of `GeneratorIndex`es.</span></span>

<span data-ttu-id="1e768-106">단일 인덱스 정수를 사용 하 여이 컬렉션을 반복 하 고 컬렉션의 크기는 알려진 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e768-106">We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.</span></span>

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a><span data-ttu-id="1e768-107">설명</span><span class="sxs-lookup"><span data-stu-id="1e768-107">Remarks</span></span>

<span data-ttu-id="1e768-108">인스턴스 `GeneratorSystem` 는 함수를 사용 하 여 쉽게 정의할 수 있습니다 <xref:microsoft.quantum.arrays.lookupfunction> .</span><span class="sxs-lookup"><span data-stu-id="1e768-108">Instances of `GeneratorSystem` can be defined easily using the <xref:microsoft.quantum.arrays.lookupfunction> function.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e768-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1e768-109">See Also</span></span>

- [<span data-ttu-id="1e768-110">Microsoft 양자 함수</span><span class="sxs-lookup"><span data-stu-id="1e768-110">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)