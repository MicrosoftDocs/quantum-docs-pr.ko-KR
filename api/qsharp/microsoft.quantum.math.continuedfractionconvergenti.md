---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentI
title: ContinuedFractionConvergentI 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentI
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: d37bf1c10899d06e798d29c68f88b06f2d5918a9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195565"
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