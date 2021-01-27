---
uid: Microsoft.Quantum.Arrays.Partitioned
title: 분할 된 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: 43d99a0e33a813e4af23a3890ace808e91c1049c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845553"
---
# <a name="partitioned-function"></a>분할 된 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="example"></a>예제

```qsharp
// The following returns [[1, 5], [3], [7]];
let split = Partitioned([2,1], [1,5,3,7]);
```