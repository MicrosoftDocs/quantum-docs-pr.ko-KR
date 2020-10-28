---
uid: Microsoft.Quantum.Logical.Xor
title: Xor 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Xor
qsharp.summary: Returns the Boolean exclusive disjunction of two values.
ms.openlocfilehash: ae43545e19e81ed5da17c3d58c62ac0b7ee765f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723294"
---
# <a name="xor-function"></a>Xor 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지 [](https://nuget.org/packages/)


두 값의 부울 배타적 논리합을 반환 합니다.

```qsharp
function Xor (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>입력

### <a name="a--bool"></a>a: [Bool](xref:microsoft.quantum.lang-ref.bool)

고려해 야 할 첫 번째 값입니다.


### <a name="b--bool"></a>b: [Bool](xref:microsoft.quantum.lang-ref.bool)

고려할 두 번째 값입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true` 및 중 하나만 이면이 고, 그렇지 않으면 `a` `b` `true` 입니다.