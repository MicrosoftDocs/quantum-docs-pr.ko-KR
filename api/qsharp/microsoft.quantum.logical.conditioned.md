---
uid: Microsoft.Quantum.Logical.Conditioned
title: 조건 화 된 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: 8aabe8b018129ddee3b934c207d0a62e59fb6f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720788"
---
# <a name="conditioned-function"></a>조건 화 된 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지 [](https://nuget.org/packages/)


부울 조건 값에 따라 두 값 중 하나를 반환 합니다.

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a>입력

### <a name="condition--bool"></a>조건: [Bool](xref:microsoft.quantum.lang-ref.bool)

반환 되는 입력을 제어 하는 데 사용 되는 조건입니다.


### <a name="iftrue--t"></a>ifTrue: ' '

가 인 경우 반환 될 값 `condition` 입니다 `true` .


### <a name="iffalse--t"></a>ifFalse: ' '

가 인 경우 반환 될 값 `condition` 입니다 `false` .



## <a name="output--t"></a>출력: ' '

`ifTrue``condition`가 이면이 `true` 고, `ifFalse` 그렇지 않으면입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="remarks"></a>설명

연산자와 달리 `?|` 이 함수는 두 입력이 모두 완전히 계산 되도록 하는 짧은 회로는 아닙니다.

단기 동작으로, 다음은 동일 합니다.

```Q#
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```