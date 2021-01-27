---
uid: Microsoft.Quantum.Arithmetic.AddFxP
title: AddFxP 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddFxP
qsharp.summary: Adds two fixed-point numbers stored in quantum registers.
ms.openlocfilehash: 60b7cad3d0bd8800e67830ca921f8e2d705b8f39
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843866"
---
# <a name="addfxp-operation"></a>AddFxP 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)


퀀텀 레지스터에 저장 된 두 개의 고정 소수점 숫자를 추가 합니다.

```qsharp
operation AddFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="description"></a>설명

각각 $ \ket{f_1} $ 및 $ \ket{f_2} $ 상태에서 두 개의 고정 소수점 레지스터가 지정 된 경우, 작업 $ \ket{f_1} \ket{f_2} \maps\ket{f_1} \ket{f_1 + f_2} $를 수행 합니다.

## <a name="input"></a>입력

### <a name="fp1--fixedpoint"></a>fp1: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

첫 번째 고정 소수점 숫자


### <a name="fp2--fixedpoint"></a>fp2: [Fixedpoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

두 번째 고정 소수점 숫자는 두 입력의 합계를 포함 하도록 업데이트 됩니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

현재 구현에서는 두 개의 고정 소수점 숫자가 최하위 비트에서 동일한 점 위치를 계산 해야 합니다. 즉, $n _i $ 및 $p _i $가 동일 해야 합니다.