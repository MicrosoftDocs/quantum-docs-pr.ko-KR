---
uid: Microsoft.Quantum.Arrays.Any
title: 모든 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Any
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.
ms.openlocfilehash: 717ab9ebcbb864a6faf1c14cd36125e589849f2e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221660"
---
# <a name="any-function"></a>모든 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 요소에 대해 정의 된 배열과 조건자가 지정 된 경우는 배열의 요소 중 하나 이상이 조건자를 충족 하는지 확인 합니다.

```qsharp
function Any<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a>입력

### <a name="predicate--t---bool"></a>조건자: ' t-> [Bool](xref:microsoft.quantum.lang-ref.bool)

에서 요소를 `'T` `Bool` 확인 하는 데 사용 하는 함수입니다.


### <a name="array--t"></a>배열: ' t []

에 있는 요소의 배열 `'T` 입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`Bool`모든 요소에 적용 되는 조건자의 또는 함수 값입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

`array`요소의 형식입니다.

## <a name="remarks"></a>설명

함수는 제네릭 형식에 대해 정의 됩니다. 즉, 배열 및 함수가 있을 때마다 `'T[]` `predicate: 'T -> Bool` `Bool` 일부 요소가 충족 되는지 여부를 나타내는 값을 생성할 수 있습니다 `predicate` .