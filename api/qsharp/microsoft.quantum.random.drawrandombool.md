---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: DrawRandomBool 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 7c13f8305756421b8d07baf22ff87764efac0418
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853684"
---
# <a name="drawrandombool-operation"></a>DrawRandomBool 작업

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


성공 확률이 지정 된 경우 지정 된 확률을 사용 하 여 true 인 단일 베르누이 평가판을 반환 합니다.

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a>입력

### <a name="successprobability--double"></a>successProbability: [Double](xref:microsoft.quantum.lang-ref.double)

이 반환 되어야 하는 확률 `true` 입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true` 확률 `successProbability` 및 확률을 포함 `false` `1.0 - successProbability` 합니다.

## <a name="example"></a>예

다음 Q # 코드 조각 샘플은 편향 동전에서 대칭 이동 합니다.

```qsharp
let flips = DrawMany(DrawRandomBool, 10, 0.6);
```