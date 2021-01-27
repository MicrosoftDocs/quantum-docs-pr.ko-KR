---
uid: Microsoft.Quantum.Arrays.Fold
title: 접기 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: d12e070058178ce2cbdd70cade5bc16607a55d5e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848599"
---
# <a name="fold-function"></a>접기 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열을 통해 함수를 반복 `f` `array` 하 여를 반환 `f(f(f(initialState, array[0]), array[1]), ...)` 합니다.

```qsharp
function Fold<'State, 'T> (folder : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State
```


## <a name="input"></a>입력

### <a name="folder--statet---state"></a>폴더: (' 상태, ' ')-> ' 상태

배열에 대해 접힌 함수입니다.


### <a name="state--state"></a>상태: ' 상태 '

폴더의 초기 상태입니다.


### <a name="array--t"></a>배열: ' t []

접을 값의 배열입니다.



## <a name="output--state"></a>출력: ' 상태

의 모든 요소를 반복한 후 폴더에서 반환 되는 최종 상태 `array` 입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="state"></a>' 상태

함수가 작동 하는 상태 유형 (예:)은 `folder` 첫 번째 인수로 수락 하 고를 반환 합니다.
### <a name="t"></a>없습니다

`array`요소의 형식입니다.

## <a name="example"></a>예제

```qsharp
function Plus(a : Double, b : Double) {
    return a + b;
}
function Sum(xs : Double[]) {
    return Fold(Plus, 0.0, xs);
}
```