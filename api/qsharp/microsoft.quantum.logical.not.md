---
uid: Microsoft.Quantum.Logical.Not
title: Not 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: f2db43f4a2ce83d8cad1d60aa8c481a33b0c7d44
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197452"
---
# <a name="not-function"></a>Not 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


값의 부울 부정을 반환 합니다.

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a>입력

### <a name="value--bool"></a>값: [Bool](xref:microsoft.quantum.lang-ref.bool)

부정할 값입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true` 가 이면이 고, 그렇지 않으면 `value` `false` 입니다.

## <a name="remarks"></a>설명

다음은 동일 합니다.

```Q#
let x = not value;
let x = Not(value);
```