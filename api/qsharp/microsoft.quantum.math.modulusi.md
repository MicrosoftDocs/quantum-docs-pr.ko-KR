---
uid: Microsoft.Quantum.Math.ModulusI
title: ModulusI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 7bad044db9e2229c85cb3909dc4802bceaee6382
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847300"
---
# <a name="modulusi-function"></a>ModulusI 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


모듈로 정식 residue을 계산 `value` `modulus` 합니다.

```qsharp
function ModulusI (value : Int, modulus : Int) : Int
```


## <a name="input"></a>입력

### <a name="value--int"></a>값: [Int](xref:microsoft.quantum.lang-ref.int)

Residue 계산 된 값입니다.


### <a name="modulus--int"></a>모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)

Residues를 사용 하는 모듈러스는 양수 여야 합니다.



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

`modulus - 1` `value - r` 모듈러스로 나눌 수 있는 0에서 사이의 정수 $r $

## <a name="remarks"></a>설명

이 함수는 c #에서 연산자가 작동 하는 방식과 다른 방식으로 동작 `%` 하며 `modulus - 1` , 값이 음수인 경우에도 결과에는 항상 0과 사이의 음수가 아닌 정수가 있습니다.