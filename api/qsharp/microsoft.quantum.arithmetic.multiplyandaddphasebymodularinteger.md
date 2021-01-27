---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger
title: MultiplyAndAddPhaseByModularInteger 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddPhaseByModularInteger
qsharp.summary: The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.
ms.openlocfilehash: b1214acc2cafc3fede9fcb6663a435c0b1d2cf4a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843070"
---
# <a name="multiplyandaddphasebymodularinteger-operation"></a>MultiplyAndAddPhaseByModularInteger 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


MultiplyAndAddByModularInteger와 동일 하지만 summand가 QFT로 정수를 인코딩하는 것으로 가정 합니다.

```qsharp
operation MultiplyAndAddPhaseByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, phaseSummand : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="constmultiplier--int"></a>constMultiplier: [Int](xref:microsoft.quantum.lang-ref.int)

각 기본 상태 레이블에 추가할 정수 $a $입니다.


### <a name="modulus--int"></a>모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)

와 관련 하 여 더하기 및 곱하기를 수행 하는 모듈러스 $N $입니다.


### <a name="multiplier--littleendian"></a>승수: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

값이의 각 기본 상태 레이블에 추가 될 부호 없는 정수를 나타내는 퀀텀 레지스터입니다 `summand` .


### <a name="phasesummand--phaselittleendian"></a>phaseSummand: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

이 작업의 대상으로 사용할 부호 없는 정수를 나타내는 퀀텀 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

에 `phaseSummand` 가장 높은 비트가 0으로 설정 된 것으로 가정 합니다.
또한은 값 `phaseSummand` 이 $ $N 미만 이라고 가정 합니다.

## <a name="see-also"></a>참고 항목

- [MultiplyAndAddByModularInteger.](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger)