---
uid: Microsoft.Quantum.Arrays.All
title: All 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: All
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.
ms.openlocfilehash: 17e61ea161b90fe089b7df7c10188d604d72dcfa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842892"
---
# <a name="all-function"></a>All 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 요소에 대해 정의 된 배열과 조건자가 지정 된 경우 및 배열의 모든 요소가 조건자를 충족 하는지 확인 합니다.

```qsharp
function All<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a>입력

### <a name="predicate--t---bool"></a>조건자: ' t-> [Bool](xref:microsoft.quantum.lang-ref.bool)

에서 요소를 `'T` `Bool` 확인 하는 데 사용 하는 함수입니다.


### <a name="array--t"></a>배열: ' t []

에 있는 요소의 배열 `'T` 입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`Bool`모든 요소에 적용 되는 조건자의 AND 함수 값입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

`array`요소의 형식입니다.

## <a name="example"></a>예

다음 코드는 배열의 모든 요소가 0이 아닌지 여부를 확인 합니다.

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function AllDemo() : Unit {
    let predicate = NotEqualI(_, 0);
    let isNonZero = All(predicate, [2, 3, 4, 5, 6, 0]);
    Message($"{isNonZero}");
}
```

## <a name="remarks"></a>설명

함수는 제네릭 형식에 대해 정의 됩니다. 즉, 배열 및 함수가 있을 때마다 `'T[]` `predicate: 'T -> Bool` `Bool` 모든 요소가 만족 하는지 여부를 나타내는 값을 생성할 수 있습니다 `predicate` .