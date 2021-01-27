---
uid: Microsoft.Quantum.Simulation.GeneratorSystem
title: GeneratorSystem 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorSystem
qsharp.summary: >-
  Represents a collection of `GeneratorIndex`es.

  We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.
ms.openlocfilehash: 3748d3fb79597fb526c86a91bc28290155189014
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858422"
---
# <a name="generatorsystem-user-defined-type"></a><span data-ttu-id="73ccb-102">GeneratorSystem 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="73ccb-102">GeneratorSystem user defined type</span></span>

<span data-ttu-id="73ccb-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="73ccb-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="73ccb-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="73ccb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="73ccb-105">Es의 컬렉션을 나타냅니다 `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="73ccb-105">Represents a collection of `GeneratorIndex`es.</span></span>

<span data-ttu-id="73ccb-106">단일 인덱스 정수를 사용 하 여이 컬렉션을 반복 하 고 컬렉션의 크기는 알려진 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73ccb-106">We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.</span></span>

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a><span data-ttu-id="73ccb-107">설명</span><span class="sxs-lookup"><span data-stu-id="73ccb-107">Remarks</span></span>

<span data-ttu-id="73ccb-108">인스턴스 `GeneratorSystem` 는 함수를 사용 하 여 쉽게 정의할 수 있습니다 <xref:microsoft.quantum.arrays.lookupfunction> .</span><span class="sxs-lookup"><span data-stu-id="73ccb-108">Instances of `GeneratorSystem` can be defined easily using the <xref:microsoft.quantum.arrays.lookupfunction> function.</span></span>

## <a name="see-also"></a><span data-ttu-id="73ccb-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="73ccb-109">See Also</span></span>

- [<span data-ttu-id="73ccb-110">Microsoft 양자 함수</span><span class="sxs-lookup"><span data-stu-id="73ccb-110">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)