---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: ConstantArray 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: a3ad8a18856888a0ca6f9dd691242156b0c044d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846239"
---
# <a name="constantarray-function"></a>ConstantArray 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


모든 요소가 지정 된 값과 같은 지정 된 길이의 배열을 만듭니다.

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a>입력

### <a name="length--int"></a>길이: [Int](xref:microsoft.quantum.lang-ref.int)

새 배열의 길이입니다.


### <a name="value--t"></a>값: ' '

새 배열의 각 요소에 대 한 값입니다.



## <a name="output--t"></a>출력: ' t []

모든 요소가 인 새 길이 배열입니다 `length` `value` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="example"></a>예

다음 코드는 각각와 같은 3 개의 부울 값 배열을 만듭니다 `true` .

```qsharp
let array = ConstantArray(3, true);
```