---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactC
title: NearEqualityFactC 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactC
qsharp.summary: Asserts that a classical complex number has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: aef4925452fe2de444b1995f92b8fe1a2894834a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712664"
---
# <a name="nearequalityfactc-function"></a>NearEqualityFactC 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지 [](https://nuget.org/packages/)


기존 복소수에 필요한 값이 1e-10의 작은 허용 오차 보다 많은 것을 어설션 합니다.

```qsharp
function NearEqualityFactC (actual : Microsoft.Quantum.Math.Complex, expected : Microsoft.Quantum.Math.Complex) : Unit
```


## <a name="input"></a>입력

### <a name="actual--complex"></a>실제: [복합](xref:Microsoft.Quantum.Math.Complex)

확인할 숫자입니다.


### <a name="expected--complex"></a>예상: [복합](xref:Microsoft.Quantum.Math.Complex)

예상 값입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

