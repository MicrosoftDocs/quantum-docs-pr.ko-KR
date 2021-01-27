---
uid: Microsoft.Quantum.Canon.Compose
title: 작성 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 73eab66e2e9a9af56d01db927eb7af38bb56a23e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840900"
---
# <a name="compose-function"></a>작성 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


두 함수의 컴퍼지션을 반환 합니다.

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a>설명

$ 및 $g $ $f 두 개의 함수가 지정 된 경우 $f \circ g $를 나타내는 새 함수를 반환 합니다.

## <a name="input"></a>입력

### <a name="outer--u---v"></a>외부: ' U-> ' V

적용할 두 번째 함수입니다.


### <a name="inner--t---u"></a>inner: ' t-> ' U

적용할 첫 번째 함수입니다.



## <a name="output--t---v"></a>출력: ' t ' > ' V

$, $F (g (x)) = h (x) $ $x 모든 입력에 대 한 새 함수는 $를 $h 합니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

적용할 첫 번째 함수의 입력 형식입니다.
### <a name="u"></a>' U

적용할 첫 번째 함수의 출력 형식과 적용할 두 번째 함수의 입력 형식입니다.
### <a name="v"></a>' V

적용할 두 번째 함수의 출력 형식입니다.