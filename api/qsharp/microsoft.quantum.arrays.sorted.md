---
uid: Microsoft.Quantum.Arrays.Sorted
title: 정렬 된 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: cb8a1ef438d798c8201ed9f52677e253770df1d3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845436"
---
# <a name="sorted-function"></a>정렬 된 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열이 지정 된 경우 지정 된 비교 함수를 기준으로 정렬 된 해당 배열의 요소를 반환 합니다.

```qsharp
function Sorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a>입력

### <a name="comparison--tt---bool"></a>비교: (' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)

`a`가 이면 보다 작거나 같은 두 요소를 비교 하는 함수입니다 `b` `comparison(a, b)` `true` .


### <a name="array--t"></a>배열: ' t []

정렬할 배열입니다.



## <a name="output--t"></a>출력: ' t []



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

에 있는 각 요소의 형식입니다 `array` .

## <a name="example"></a>예

다음 코드 조각은 오름차순으로 발생 하는 정수 배열을 정렬 합니다.

```qsharp
let sortedArray = Sorted(LessThanOrEqualI, [3, 17, 11, -201, -11]);
```

## <a name="remarks"></a>설명

함수는 `comparison` 전이적으로 간주 됩니다. 예를 들어 및 인 경우에는를로 `comparison(a, b)` `comparison(b, c)` `comparison(a, c)` 가정 합니다. 이 속성이 없으면이 함수의 출력이 올바르지 않을 수 있습니다.

이는 함수 이기 때문에 두 요소가 같은 것으로 간주 되는 경우에도 결과는 완전히 결정적 `comparison` . 즉, `comparison(a, b)` 와 `comparison(b, a)` 가 둘 다 `true` 인 경우에도 마찬가지입니다.
특히이 함수에서 수행 하는 정렬의 안정성은 안정적인 것으로 간주 되므로 및 내에서 두 개의 요소가 및에서 동일한 순서로 발생 하는 경우에는 `a` `b` `array` `comparison` `a` 출력의 앞에도 표시 됩니다 `b` .

예를 들어:

```qsharp
function LastDigitLessThanOrEqual(left : Int, right : Int) : Bool {
    return LessThanOrEqualI(
        left % 10, right % 10
    );
}

function SortedByLastDigit() : Int[] {
    return Sorted(LastDigitLessThanOrEqual, [3, 37, 11, 17]);
}
// returns [11, 3, 37, 17].
```