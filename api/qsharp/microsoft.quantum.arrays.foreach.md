---
uid: Microsoft.Quantum.Arrays.ForEach
title: ForEach 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: 90dd6f94408d37d2b32d82e772a482b0e69c523f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848596"
---
# <a name="foreach-operation"></a>ForEach 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 요소에 대해 정의 된 배열과 작업이 지정 된 경우 작업에서 원래 배열의 이미지로 구성 된 새 배열을 반환 합니다.

```qsharp
operation ForEach<'T, 'U> (action : ('T => 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a>입력

### <a name="action--t--u"></a>작업: ' t => ' U 

`'T` `'U` 각 요소에 적용 되는에서로의 작업입니다.


### <a name="array--t"></a>배열: ' t []

에 있는 요소의 배열 `'T` 입니다.



## <a name="output--u"></a>출력: ' U []

`'U[]`작업에 의해 매핑되는 요소의 배열입니다 `action` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

`array`요소의 형식입니다.
### <a name="u"></a>' U

작업의 결과 형식 `action` 입니다.

## <a name="remarks"></a>설명

작업은 제네릭 형식에 대해 정의 됩니다. 즉, 배열 및 작업이 있을 때마다 `'T[]` `action : 'T -> 'U` 배열의 요소를 매핑하고 형식의 새 배열을 생성할 수 있습니다 `'U[]` .