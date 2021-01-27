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
# <a name="generatorsystem-user-defined-type"></a>GeneratorSystem 사용자 정의 형식

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Es의 컬렉션을 나타냅니다 `GeneratorIndex` .

단일 인덱스 정수를 사용 하 여이 컬렉션을 반복 하 고 컬렉션의 크기는 알려진 것으로 간주 됩니다.

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a>설명

인스턴스 `GeneratorSystem` 는 함수를 사용 하 여 쉽게 정의할 수 있습니다 <xref:microsoft.quantum.arrays.lookupfunction> .

## <a name="see-also"></a>참고 항목

- [Microsoft 양자 함수](xref:Microsoft.Quantum.Arrays.LookupFunction)