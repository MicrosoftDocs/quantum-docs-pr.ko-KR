---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: CumulativeFolded 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: 95cd5233a09a1234bba4de9fe870b9d93c0f86a4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846232"
---
# <a name="cumulativefolded-function"></a>CumulativeFolded 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


매핑된 및 접기를 단일 함수로 결합 합니다.

```qsharp
function CumulativeFolded<'State, 'T> (fn : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State[]
```


## <a name="description"></a>설명

이 함수는 초기 상태 `fn` 에서 시작 하 여 배열을 통해 함수를 반복 하 `state` 고 초기 상태를 포함 하지 않고 모든 중간 값을 반환 합니다.

## <a name="input"></a>입력

### <a name="fn--statet---state"></a>fn: (' State, t)-> ' 상태

배열에 대해 접힌 함수


### <a name="state--state"></a>상태: ' 상태 '

접은 초기 상태


### <a name="array--t"></a>배열: ' t []

접기 될 값의 배열입니다.



## <a name="output--state"></a>출력: ' State []

최종 상태를 포함 하지만 초기 상태를 포함 하지 않는 모든 중간 상태입니다.
출력 배열의 길이가와 같은 길이입니다 `array` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="state"></a>' 상태

함수가 작동 하는 상태 유형 (예:)은 `fn` 첫 번째 입력으로 수락 하 고를 반환 합니다.
### <a name="t"></a>없습니다

`array`요소의 형식입니다.

## <a name="example"></a>예제

```qsharp
// same as sums = [1, 3, 6, 10, 15]
let sums = CumulativeFolded(PlusI, 0, SequenceI(1, 5));
```