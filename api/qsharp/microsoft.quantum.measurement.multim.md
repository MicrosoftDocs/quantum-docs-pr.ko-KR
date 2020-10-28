---
uid: Microsoft.Quantum.Measurement.MultiM
title: MultiM 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: 36de9dbdfc96f6e1698ee4537405f7cb74e44262
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711040"
---
# <a name="multim-operation"></a>MultiM 작업

네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)

패키지 [](https://nuget.org/packages/)


지정 된 배열의 각 고 비트를 표준 기준으로 측정 합니다.

```qsharp
operation MultiM (targets : Qubit[]) : Result[]
```


## <a name="input"></a>입력

### <a name="targets--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

측정할 비트의 배열입니다.



## <a name="output--__invalidresult__"></a>출력: __잘못 <Result> 된__ []

측정 결과의 배열입니다.