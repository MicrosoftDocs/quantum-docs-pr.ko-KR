---
uid: Microsoft.Quantum.Preparation._ApproximatelyUnprepareArbitraryStatePlan
title: _ApproximatelyUnprepareArbitraryStatePlan 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: _ApproximatelyUnprepareArbitraryStatePlan
qsharp.summary: Implementation step of arbitrary state preparation procedure.
ms.openlocfilehash: 4050a65b0830da4c3d73e84942780aa7c2643c76
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724204"
---
# <a name="_approximatelyunpreparearbitrarystateplan-function"></a>_ApproximatelyUnprepareArbitraryStatePlan 함수

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지 [](https://nuget.org/packages/)


임의 상태 준비 절차의 구현 단계입니다.

```qsharp
function _ApproximatelyUnprepareArbitraryStatePlan (tolerance : Double, coefficients : Microsoft.Quantum.Math.ComplexPolar[], (rngControl : Range, idxTarget : Int)) : (Qubit[] => Unit is Adj + Ctl)[]
```


## <a name="input"></a>입력

### <a name="tolerance--double"></a>허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)




### <a name="coefficients--complexpolar"></a>계수: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]




### <a name="rngcontrol--range"></a>rngControl: [범위](xref:microsoft.quantum.lang-ref.range)




### <a name="idxtarget--int"></a>idxTarget: [Int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--qubit--unit-adj--ctl"></a>출력: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl []



## <a name="see-also"></a>참고 항목

- [PrepareArbitraryState.](xref:Microsoft.Quantum.Preparation.PrepareArbitraryState)
- [MultiplexPauli입니다.](xref:Microsoft.Quantum.Canon.MultiplexPauli)