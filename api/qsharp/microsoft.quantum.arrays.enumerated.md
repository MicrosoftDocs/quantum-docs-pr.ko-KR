---
uid: Microsoft.Quantum.Arrays.Enumerated
title: 열거 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: adb13d8b25c9e4a6011ade119ffa3cb2783f60e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848137"
---
# <a name="enumerated-function"></a>열거 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열이 지정 된 경우 각 요소의 인덱스와 함께 원래 배열의 요소를 포함 하는 새 배열을 반환 합니다.

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a>입력

### <a name="array--telement"></a>배열: ' TElement []

해당 요소를 열거할 배열입니다.



## <a name="output--inttelement"></a>Output: ([Int](xref:microsoft.quantum.lang-ref.int), ' TElement) []

인덱스와 함께 원래 배열의 요소를 포함 하는 새 배열입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="telement"></a>' TElement

배열의 요소 형식입니다.

## <a name="example"></a>예

다음 `for` 루프는 동일 합니다.

```qsharp
for (idx in IndexRange(array)) {
    let element = array[idx];
    ...
}
for ((idx, element) in Enumerated(array)) { ... }
```