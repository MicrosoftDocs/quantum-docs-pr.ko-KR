---
uid: Microsoft.Quantum.Arrays.IsSorted
title: IsSorted 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsSorted
qsharp.summary: Given an array, returns whether that array is sorted as defined by a given comparison function.
ms.openlocfilehash: 330c1f789585f64cf255bc74f8a9c1ccf81b009e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719101"
---
# <a name="issorted-function"></a>IsSorted 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지 [](https://nuget.org/packages/)


배열이 지정 된 경우 지정 된 비교 함수에 의해 정의 된 대로 배열이 정렬 되는지 여부를 반환 합니다.

```qsharp
function IsSorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a>입력

### <a name="comparison--tt---bool"></a>비교: (' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)

`a`가 이면 보다 작거나 같은 두 요소를 비교 하는 함수입니다 `b` `comparison(a, b)` `true` .


### <a name="array--t"></a>배열: ' t []

확인할 배열입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true` 각 요소 쌍에 대해 및이 순서 대로 발생 하는 경우에만 `a` `b` 가입니다 `array` `comparison(a, b)` `true` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

에 있는 각 요소의 형식입니다 `array` .

## <a name="remarks"></a>설명

함수는 `comparison` 전이적으로 간주 됩니다. 예를 들어 및 인 경우에는를로 `comparison(a, b)` `comparison(b, c)` `comparison(a, c)` 가정 합니다. 이 속성이 없으면이 함수의 출력이 올바르지 않을 수 있습니다.