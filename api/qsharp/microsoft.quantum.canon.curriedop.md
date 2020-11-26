---
uid: Microsoft.Quantum.Canon.CurriedOp
title: CurriedOp 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: 6c1917d6f1ee69cb29fed1ab173106af1e206533
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216628"
---
# <a name="curriedop-function"></a>CurriedOp 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


두 입력에 대해 변환 된 작업 버전을 반환 합니다.

즉, 두 개의 입력으로 작업을 제공 하는 경우이 함수는 isomorphism $f (x, y) \equiv f (x) (y) $를 적용 하 여 한 입력의 작업을 반환 하는 하나의 입력 작업을 반환 합니다.

```qsharp
function CurriedOp<'T, 'U> (op : (('T, 'U) => Unit)) : ('T -> ('U => Unit))
```


## <a name="input"></a>입력

### <a name="op--tu--unit"></a>op: (' t ', ' U) => [Unit](xref:microsoft.quantum.lang-ref.unit) 

입력이 쌍 인 작업입니다.



## <a name="output--t---u--unit"></a>출력: ' U ' > ' U => [단위](xref:microsoft.quantum.lang-ref.unit) 

쌍의 첫 번째 요소를 수락 하 고 원래 작업의 입력에 대 한 두 번째 요소를 입력으로 받아 들이는 작업을 반환 하는 작업입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

쌍에 정의 된 함수의 첫 번째 구성 요소 형식입니다.
### <a name="u"></a>' U

쌍에 정의 된 함수의 두 번째 구성 요소 형식입니다.

## <a name="remarks"></a>설명

다음은 동일 합니다.

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```