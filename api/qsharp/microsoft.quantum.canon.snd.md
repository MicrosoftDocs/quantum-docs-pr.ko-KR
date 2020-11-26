---
uid: Microsoft.Quantum.Canon.Snd
title: Snd 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Snd
qsharp.summary: Given a pair, returns its second element.
ms.openlocfilehash: c935a2bc9e3f5ab32669feae2bfc0f2ebf57e744
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205323"
---
# <a name="snd-function"></a>Snd 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


쌍이 지정 된 경우 두 번째 요소를 반환 합니다.

```qsharp
function Snd<'T, 'U> (pair : ('T, 'U)) : 'U
```


## <a name="input"></a>입력

### <a name="pair--tu"></a>pair: (' t ', ' U)

두 개의 요소가 포함 된 튜플입니다.



## <a name="output--u"></a>출력: ' U

의 두 번째 요소 `pair` 입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

쌍의 첫 번째 멤버의 형식입니다.
### <a name="u"></a>' U

쌍의 두 번째 멤버의 형식입니다.