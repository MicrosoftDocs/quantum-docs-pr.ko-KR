---
uid: Microsoft.Quantum.Arrays.Partitioned
title: 분할 된 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: e3395afeda206e255a58175b57245f91c588d978
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718976"
---
# <a name="partitioned-function"></a>분할 된 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지 [](https://nuget.org/packages/)


배열을 여러 부분으로 분할 합니다.

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a>입력

### <a name="nelements--int"></a>nElements: [Int](xref:microsoft.quantum.lang-ref.int)[]

배열의 각 부분에 있는 요소 수


### <a name="arr--t"></a>arr: ' t []

분할할 입력 배열입니다.



## <a name="output--t"></a>출력: ' t [] []

첫 번째 배열이 첫 번째 배열이 `nElements[0]` `arr` 고 두 번째 배열이 그 다음 `nElements[1]` 인 여러 배열 `arr` 마지막 배열은 나머지 모든 요소를 포함 합니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

