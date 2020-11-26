---
uid: Microsoft.Quantum.Arithmetic.CompareGreaterThanFxP
title: CompareGreaterThanFxP 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGreaterThanFxP
qsharp.summary: Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.
ms.openlocfilehash: 1e9afc7645f62b932fa8ebc3d33e21a2a5182361
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223530"
---
# <a name="comparegreaterthanfxp-operation"></a>CompareGreaterThanFxP 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)


퀀텀 레지스터에 저장 된 두 개의 고정 소수점 숫자를 비교 하 고 결과에서 대칭 이동을 제어 합니다.

```qsharp
operation CompareGreaterThanFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="fp1--fixedpoint"></a>fp1: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

비교할 첫 번째 고정 소수점 숫자입니다.


### <a name="fp2--fixedpoint"></a>fp2: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

비교할 두 번째 고정 소수점 숫자입니다.


### <a name="result--qubit"></a>결과: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

비교 결과입니다. 인 경우가 대칭 이동 됩니다 `fp1 > fp2` .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

현재 구현에서는 두 개의 고정 소수점 숫자가 동일한 점 위치와 동일한 수의 값을 갖도록 요구 합니다.