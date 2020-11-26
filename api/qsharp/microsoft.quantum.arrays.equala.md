---
uid: Microsoft.Quantum.Arrays.EqualA
title: EqualA 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: 176e15139a27d375fb047c07fa1ee778dc8cc2ce
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221371"
---
# <a name="equala-function"></a>EqualA 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


동일한 형식의 두 배열과 배열의 요소 쌍에 대해 정의 된 조건자가 지정 된 경우 배열이 같은지 여부를 확인 합니다.

```qsharp
function EqualA<'T> (equal : (('T, 'T) -> Bool), array1 : 'T[], array2 : 'T[]) : Bool
```


## <a name="input"></a>입력

### <a name="equal--tt---bool"></a>같음: (' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)

튜플의 `('T, 'T)` `Bool` 두 요소가 같은지 여부를 확인 하는 데 사용 되는 튜플의 함수입니다.


### <a name="array1--t"></a>: ' t []

비교할 첫 번째 배열입니다.


### <a name="array2--t"></a>: ' t []

비교할 두 번째 배열입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

와가 같으면 값이이 고, 그렇지 않으면 `true` `array1` `array2` 입니다.
즉, 두 배열의 길이가 같고 모든 요소가에서 정의한 것과 같은 경우입니다 `equal` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

각 배열의 요소 형식입니다.

## <a name="remarks"></a>설명

이 함수는 제네릭 형식에 대해 정의 됩니다. 즉, 두 개의 배열과 함수가 있을 때마다 `'T[]` `equal: ('T, 'T) -> Bool` 이 함수는 `Bool` 배열이 같은지 여부를 나타내는 값을 반환 합니다.
두 배열이 동일한 것으로 간주 되려면 길이가 같아야 하 고 배열의 같은 위치에 있는 요소가 같아야 합니다.