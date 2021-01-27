---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactCP
title: NearEqualityFactCP 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactCP
qsharp.summary: Asserts that a classical complex number has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: 477449913732950ad26adc0cdabaaaab803a20c3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853277"
---
# <a name="nearequalityfactcp-function"></a>NearEqualityFactCP 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


기존 복소수에 필요한 값이 1e-10의 작은 허용 오차 보다 많은 것을 어설션 합니다.

```qsharp
function NearEqualityFactCP (actual : Microsoft.Quantum.Math.ComplexPolar, expected : Microsoft.Quantum.Math.ComplexPolar) : Unit
```


## <a name="input"></a>입력

### <a name="actual--complexpolar"></a>실제: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)

확인할 숫자입니다.


### <a name="expected--complexpolar"></a>예상: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)

예상 값입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

