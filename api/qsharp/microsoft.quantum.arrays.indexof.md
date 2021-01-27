---
uid: Microsoft.Quantum.Arrays.IndexOf
title: IndexOf 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 64db55e831078a7130a3ced6a30bfbd2299c392d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848516"
---
# <a name="indexof-function"></a>IndexOf 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열에서 지정 된 조건자를 만족 하는 첫 번째 요소의 첫 번째 인덱스를 반환 합니다. 이러한 요소가 없는 경우-1을 반환 합니다.

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a>입력

### <a name="predicate--t---bool"></a>조건자: ' t-> [Bool](xref:microsoft.quantum.lang-ref.bool)

배열의 요소에 대해 작동 하는 조건자 함수입니다.


### <a name="arr--t"></a>arr: ' t []

지정 된 조건자를 사용 하 여 검색할 배열입니다.



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

True 인 가장 작은 인덱스 이거나 `idx` `predicate(arr[idx])` , 이러한 요소가 없는 경우-1입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="example"></a>예

해당 `IsEven : Int -> Bool` 입력이 이더라도 인 경우에만를 반환 하는 함수 라고 가정 `true` 합니다. 그런 다음와 함께 사용 하 여 `IndexOf` 배열에서 첫 번째 짝수 요소를 찾을 수 있습니다.

```qsharp
let items = [1, 3, 17, 2, 21];
let idx = IndexOf(IsEven, items); // returns 3
```