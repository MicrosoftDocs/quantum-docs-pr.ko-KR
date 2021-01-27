---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: DrawRandomInt 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: ebed7f52b7c4a8c538ed9d718c486b5aa94a0327
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851134"
---
# <a name="drawrandomint-operation"></a>DrawRandomInt 작업

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


지정 된 포함 범위에서 임의의 정수를 그립니다.

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a>입력

### <a name="min--int"></a>min: [Int](xref:microsoft.quantum.lang-ref.int)

그릴 가장 작은 정수입니다.


### <a name="max--int"></a>최대: [Int](xref:microsoft.quantum.lang-ref.int)

그릴 가장 큰 정수입니다.



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

의 포함 범위에서에 해당 하는 정수 `min` `max` 입니다.

## <a name="example"></a>예

다음 Q # 코드 조각은 임의로 6 면 주사위를 롤업 합니다.

```qsharp
let roll = DrawRandomInt(1, 6);
```

## <a name="remarks"></a>설명

인 경우 실패 `max <= min` 합니다.

## <a name="see-also"></a>참고 항목

- [DiscreteUniformDistribution](xref:Microsoft.Quantum.DiscreteUniformDistribution)