---
uid: Microsoft.Quantum.Canon.Fst
title: Fst 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Fst
qsharp.summary: Given a pair, returns its first element.
ms.openlocfilehash: 88ff5e29de9eeefcc1e207f277c37c63cb0faade
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716185"
---
# <a name="fst-function"></a>Fst 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


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