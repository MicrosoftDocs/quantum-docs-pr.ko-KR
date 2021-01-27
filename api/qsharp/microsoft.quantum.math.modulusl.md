---
uid: Microsoft.Quantum.Math.ModulusL
title: ModulusL 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 6be2edb052cf55f8e8465c76b5dcadeb61ff11ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842739"
---
# <a name="modulusl-function"></a>ModulusL 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


모듈로 정식 residue을 계산 `value` `modulus` 합니다.

```qsharp
function ModulusL (value : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a>입력

### <a name="value--bigint"></a>값: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

Residue 계산 된 값입니다.


### <a name="modulus--bigint"></a>모듈러스: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

Residues를 사용 하는 모듈러스는 양수 여야 합니다.



## <a name="output--bigint"></a>출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

`modulus - 1` `value - r` 모듈러스로 나눌 수 있는 0에서 사이의 정수 $r $

## <a name="remarks"></a>설명

이 함수는 c #에서 연산자가 작동 하는 방식과 다른 방식으로 동작 `%` 하며 `modulus - 1` , 값이 음수인 경우에도 결과에는 항상 0과 사이의 음수가 아닌 정수가 있습니다.