---
uid: Microsoft.Quantum.Logical.Xor
title: Xor 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Xor
qsharp.summary: Returns the Boolean exclusive disjunction of two values.
ms.openlocfilehash: 4a4af7f628ca64170e046584d9caffe7ceee3d56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848444"
---
# <a name="xor-function"></a>Xor 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


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