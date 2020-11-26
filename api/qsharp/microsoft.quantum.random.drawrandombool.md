---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: DrawRandomBool 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: dbe0836af5aa19f1bdce3cfe93be6833358c22be
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192964"
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