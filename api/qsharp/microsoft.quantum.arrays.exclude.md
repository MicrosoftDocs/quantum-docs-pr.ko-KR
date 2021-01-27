---
uid: Microsoft.Quantum.Arrays.Exclude
title: Exclude 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Exclude
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 76cdee56e84951c63e80babfdca6a3de33583cab
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848668"
---
# <a name="exclude-function"></a>Exclude 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 인덱스 목록에서 요소를 제외 하 고 다른 배열의 요소를 포함 하는 배열을 반환 합니다.

```qsharp
function Exclude<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a>입력

### <a name="remove--int"></a>remove: [Int](xref:microsoft.quantum.lang-ref.int)[]

출력에서 제외 해야 하는 요소를 나타내는 인덱스의 배열입니다.


### <a name="array--t"></a>배열: ' t []

출력 배열의 값이 사용 되는 배열입니다.



## <a name="output--t"></a>출력: ' t []

인덱스를 `output` `output[0]` 에 표시 하지 않는의 첫 번째 요소 (예: `array` `remove` `output[1]` 두 번째 요소 등) 인 배열입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

배열 요소의 형식입니다.

## <a name="example"></a>예제

```qsharp
let array = [10, 11, 12, 13, 14, 15];
// The following line returns [10, 12, 15].
let subarray = Exclude([1, 3, 4], array);
```