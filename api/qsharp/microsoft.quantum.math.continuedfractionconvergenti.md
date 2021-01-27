---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentI
title: ContinuedFractionConvergentI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentI
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: c5316c13ce499da88c0d5c45b9d8c5e3a8c6162d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853850"
---
# <a name="continuedfractionconvergenti-function"></a>ContinuedFractionConvergentI 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


일치에 가장 가까운 연속 분수를 찾습니다. `fraction``denominatorBound`

```qsharp
function ContinuedFractionConvergentI (fraction : Microsoft.Quantum.Math.Fraction, denominatorBound : Int) : Microsoft.Quantum.Math.Fraction
```


## <a name="input"></a>입력

### <a name="fraction--fraction"></a>분수: [분수](xref:Microsoft.Quantum.Math.Fraction)




### <a name="denominatorbound--int"></a>denominatorBound: [Int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--fraction"></a>출력: [분수](xref:Microsoft.Quantum.Math.Fraction)

분모와 작거나 같은에 가장 가까운 연속 분수 `fraction``denominatorBound`