---
uid: Microsoft.Quantum.Logical.Not
title: Not 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: 3a688aac0178a2f4127496c1009fe7d5ee7ae198
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709864"
---
# <a name="not-function"></a>Not 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지 [](https://nuget.org/packages/)


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