---
uid: Microsoft.Quantum.Arrays.IndexOf
title: IndexOf 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: d63b204334611f8f2c3860f9ee1d756f637780e2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221014"
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

