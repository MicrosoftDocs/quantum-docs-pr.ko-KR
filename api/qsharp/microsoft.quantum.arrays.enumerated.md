---
uid: Microsoft.Quantum.Arrays.Enumerated
title: 열거 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 0a591025a4eef79e08b47527c0bdb556f5645334
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719305"
---
# <a name="enumerated-function"></a>열거 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지 [](https://nuget.org/packages/)


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