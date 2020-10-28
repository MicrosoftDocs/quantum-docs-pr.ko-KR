---
uid: Microsoft.Quantum.Math.PlusA
title: PlusA 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PlusA
qsharp.summary: Returns the sum (concatenation) of two inputs.
ms.openlocfilehash: 0c6fdcf7c59dc5d89bf83e285339046b5ad5a57e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709605"
---
# <a name="plusa-function"></a>PlusA 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지 [](https://nuget.org/packages/)


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