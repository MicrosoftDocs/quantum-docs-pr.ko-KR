---
uid: Microsoft.Quantum.Arrays.Padded
title: 채워진 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 2b7a80d1cf5c82a1ff52bc4aa207cfe335b40061
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220538"
---
# <a name="padded-function"></a>채워진 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 값을 사용 하 여 지정 된 길이까지 채워진 배열을 반환 합니다.

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a>입력

### <a name="nelementstotal--int"></a>nElementsTotal: [Int](xref:microsoft.quantum.lang-ref.int)

패딩 된 배열의 길이입니다. 이가 양수인 경우 `inputArray` 는 헤드에 채워집니다. 이가 음수 이면 `inputArray` 꼬리에 채워집니다.


### <a name="defaultelement--t"></a>defaultElement: ' '

요소 패딩에 사용할 기본값입니다.


### <a name="inputarray--t"></a>inputArray: ' t []

출력 배열의 헤드에 값이 있는 배열입니다.



## <a name="output--t"></a>출력: ' t []

에 `output` `inputArray` `defaultElement` 길이가 있을 때까지 s로 채워진의 배열입니다. `output``nElementsTotal`

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

배열 요소의 형식입니다.