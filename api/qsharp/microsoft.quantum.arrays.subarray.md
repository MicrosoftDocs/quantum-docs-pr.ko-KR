---
uid: Microsoft.Quantum.Arrays.Subarray
title: 하위 배열 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Subarray
qsharp.summary: Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.
ms.openlocfilehash: ccc041da0213d1f5dc5c8b4ff7a03b8b01ad107d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845426"
---
# <a name="subarray-function"></a>하위 배열 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열 및 위치 목록을 가져오고, 지정 된 위치와 일치 하는 원래 배열의 요소에서 형성 된 새 배열을 생성 합니다.

```qsharp
function Subarray<'T> (indices : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a>입력

### <a name="indices--int"></a>인덱스: [Int](xref:microsoft.quantum.lang-ref.int)[]

하위 배열을 정의 하는 데 사용 되는 정수 목록입니다.


### <a name="array--t"></a>배열: ' t []

에 있는 요소의 배열 `'T` 입니다.



## <a name="output--t"></a>출력: ' t []

`out`해당 인덱스가 하위 배열에 해당 하는 요소의 배열입니다 `out[idx] == array[indices[idx]]` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

`array`요소의 형식입니다.

## <a name="remarks"></a>설명

함수는 제네릭 형식에 대해 정의 됩니다. 즉, 배열 및 하위 배열을 정의 하는 `'T[]` 위치 목록이 있을 때마다입니다. `Int[]`
하위 배열의 구성은 참조를 유지 관리 하는 대신 지정 된 배열의 새 전체 복사본을 생성 하는 것을 기반으로 합니다.

인 경우 `Length(indices) < Length(array)` 이 함수는의 하위 집합을 반환 `array` 합니다. 반면에 반복 되는 요소가 포함 된 경우에는 `indices` 의 해당 요소도 `array` 반복 됩니다.
`indices`및 `array` 의 길이가 같은 경우이 함수는의 순열을 제공 `array` 합니다.