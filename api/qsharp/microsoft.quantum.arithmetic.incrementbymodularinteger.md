---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: IncrementByModularInteger 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: f5bacef299ab0b3627e757abdcaa798cf9b2e7b3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846596"
---
# <a name="incrementbymodularinteger-operation"></a>IncrementByModularInteger 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


정수 상수를 기준으로 하는 이상 비트 레지스터의 모듈식 증분을 수행 합니다.

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>설명

`increment`$A $, `modulus` $N $ 및 $y $로 인코딩된 정수를 사용 하 여 나타냅니다 `target` .
그런 다음이 작업은 다음 변환을 수행 합니다. \begin{align} \ket{y} \maps\ket{(y + a) \operatorname{mod} N} \end{align} 정수는 작은 endian 형식으로 인코딩됩니다.

## <a name="input"></a>입력

### <a name="increment--int"></a>증가값: [Int](xref:microsoft.quantum.lang-ref.int)

$Y $에 더할 정수 증가값 $a $입니다.


### <a name="modulus--int"></a>모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)

Mods $y + a $의 정수 $N $입니다.


### <a name="target--littleendian"></a>대상: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

`LittleEndian` `increment` $A $가에 추가 되는 형식의 정수 $y $입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

Target의 초기 값이 $ $N 보다 작고 증분 $a $가 $N $ 보다 작은 것으로 가정 합니다.
에서는 <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> 동일한 작업을 기준으로 구현 합니다 `PhaseLittleEndian` .

## <a name="see-also"></a>참고 항목

- [IncrementPhaseByModularInteger.](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)