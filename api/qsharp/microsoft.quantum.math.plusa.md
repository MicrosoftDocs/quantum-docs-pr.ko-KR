---
uid: Microsoft.Quantum.Math.PlusA
title: PlusA 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PlusA
qsharp.summary: Returns the sum (concatenation) of two inputs.
ms.openlocfilehash: 14e9bfdbe4b70b4730e5bfc64a0ee81ab3cecaaf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842711"
---
# <a name="plusa-function"></a>PlusA 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


두 입력의 합 (연결)을 반환 합니다.

```qsharp
function PlusA<'Element> (a : 'Element[], b : 'Element[]) : 'Element[]
```


## <a name="input"></a>입력

### <a name="a--element"></a>a: ' 요소 []

합계를 구할 첫 번째 입력 $a $입니다.


### <a name="b--element"></a>b: ' 요소 []

합계를 구할 두 번째 입력 $b $입니다.



## <a name="output--element"></a>Output: ' 요소 []

Sum $a + b $입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="element"></a>' 요소

두 입력 배열의 각 요소에 대 한 형식입니다.