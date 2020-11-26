---
uid: Microsoft.Quantum.Arrays.Enumerated
title: 열거 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 94e8fdb7288bc43ed84d10a3292819b455a2be31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221422"
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