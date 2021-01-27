---
uid: Microsoft.Quantum.Arithmetic.GreaterThan
title: GreaterThan 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: GreaterThan
qsharp.summary: Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.
ms.openlocfilehash: 553efb0fc83f24235cb4a77933bd1d547bbd1fed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846626"
---
# <a name="greaterthan-operation"></a>GreaterThan 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


비교 결과에 따라 대상의 범위를 대칭 이동 하는 두 개의 정수를 해당 형식으로 인코딩된 두 정수 사이에 보다 큼 비교를 적용 합니다.

```qsharp
operation GreaterThan (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>설명

$ 및 $y $ $x 두 정수의 비교를 엄격 하 게 비교 합니다. Y $를 > $x 경우에는 결과의 비트가 대칭 이동 됩니다. 그렇지 않으면 결과의 비트가 상태를 유지 합니다.

## <a name="input"></a>입력

### <a name="xs--littleendian"></a>xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian vebit는 첫 번째 정수 $x $로 인코딩합니다.


### <a name="ys--littleendian"></a>작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian cobit $y $의 두 번째 정수를 등록 합니다.


### <a name="result--qubit"></a>결과: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

$X > y $ 인 경우 대칭 이동 될 단일 비트입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

는 $x-y = (x ' + y) ' $를 사용 합니다. 여기서은 1의 보수를 나타냅니다.

## <a name="references"></a>참조

- Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new 퀀텀 ripple and A new, 2004.
  https://arxiv.org/abs/quant-ph/0410184v1

- Thomas Haener, Martin Roetteler, Krysta M. Svore: "2n를 사용 하는 Toffoli + 2 based 모듈형 곱셈", 2016 https://arxiv.org/abs/1611.07995