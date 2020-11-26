---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: DrawRandomInt 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: f7b6cb75f761e4c45295245ed4bd4fb82c592809
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192913"
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

## <a name="remarks"></a>설명

인 경우 실패 `max <= min` 합니다.

## <a name="see-also"></a>참고 항목

- [DiscreteUniformDistribution](xref:Microsoft.Quantum.DiscreteUniformDistribution)