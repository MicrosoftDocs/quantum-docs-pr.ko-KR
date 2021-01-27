---
uid: Microsoft.Quantum.Arithmetic.PrepareFxP
title: PrepareFxP 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PrepareFxP
qsharp.summary: Initialize a quantum fixed-point number to a classical constant.
ms.openlocfilehash: 31ed1a170a47c77c21aa8b5c291860e422af2e3d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845807"
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

