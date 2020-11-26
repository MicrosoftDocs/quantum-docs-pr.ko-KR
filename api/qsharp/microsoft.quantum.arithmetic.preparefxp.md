---
uid: Microsoft.Quantum.Arithmetic.PrepareFxP
title: PrepareFxP 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PrepareFxP
qsharp.summary: Initialize a quantum fixed-point number to a classical constant.
ms.openlocfilehash: 29ba66700db83d0786a70841c7b03843a9ae6219
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222408"
---
# <a name="preparefxp-operation"></a>PrepareFxP 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)


퀀텀 고정 소수점 수를 기존 상수로 초기화 합니다.

```qsharp
operation PrepareFxP (constant : Double, fp : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="constant--double"></a>상수: [Double](xref:microsoft.quantum.lang-ref.double)

퀀텀 고정 소수점 수를 초기화할 상수입니다.


### <a name="fp--fixedpoint"></a>fp: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

초기화할 고정 소수점 숫자 (FixedPoint 형식)입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

