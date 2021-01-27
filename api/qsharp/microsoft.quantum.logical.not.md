---
uid: Microsoft.Quantum.Logical.Not
title: Not 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: bf09cac8d126371df6218b7e92d68a881b732dc8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849084"
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

```qsharp
let x = not value;
let x = Not(value);
```