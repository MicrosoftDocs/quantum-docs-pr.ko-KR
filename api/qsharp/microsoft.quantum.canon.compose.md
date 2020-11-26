---
uid: Microsoft.Quantum.Canon.Compose
title: 작성 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: f8c6ad36220b48be1723c2d91cbf7c0a4947af14
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216764"
---
# <a name="compose-function"></a>작성 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


두 함수의 컴퍼지션을 반환 합니다.

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a>Description

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