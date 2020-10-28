---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: DrawRandomBool 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 05cf8ad939691aac90625c5d056ea79aa062f553
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720277"
---
# <a name="drawrandombool-operation"></a>DrawRandomBool 작업

네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)

패키지 [](https://nuget.org/packages/)


성공 확률이 지정 된 경우 지정 된 확률을 사용 하 여 true 인 단일 베르누이 평가판을 반환 합니다.

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a>입력

### <a name="successprobability--double"></a>successProbability: [Double](xref:microsoft.quantum.lang-ref.double)

이 반환 되어야 하는 확률 `true` 입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true` 확률 `successProbability` 및 확률을 포함 `false` `1.0 - successProbability` 합니다.