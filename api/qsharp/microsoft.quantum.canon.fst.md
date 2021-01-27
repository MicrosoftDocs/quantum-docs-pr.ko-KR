---
uid: Microsoft.Quantum.Canon.Fst
title: Fst 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: cd5746358c8323f8d2dbca44965fa5dbac0a84c1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840510"
---
# <a name="fst-function"></a>Fst 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


쌍이 지정 된 경우 첫 번째 요소를 반환 합니다.

```qsharp
function Fst<'T, 'U> (pair : ('T, 'U)) : 'T
```


## <a name="input"></a>입력

### <a name="pair--tu"></a>pair: (' t ', ' U)

두 개의 요소가 포함 된 튜플입니다.



## <a name="output--t"></a>출력: ' '

`pair`의 첫 번째 요소입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

쌍의 첫 번째 멤버의 형식입니다.
### <a name="u"></a>' U

쌍의 두 번째 멤버의 형식입니다.