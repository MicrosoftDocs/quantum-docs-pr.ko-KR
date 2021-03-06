---
uid: Microsoft.Quantum.Diagnostics.EqualityWithinToleranceFact
title: EqualityWithinToleranceFact 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EqualityWithinToleranceFact
qsharp.summary: Represents the claim that a classical floating point value has the expected value up to a given absolute tolerance.
ms.openlocfilehash: ab7e43d951bf741926b15f27f94d176e88609d4a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98828745"
---
# <a name="equalitywithintolerancefact-function"></a>EqualityWithinToleranceFact 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


고전 부동 소수점 값에 지정 된 절대 허용 오차 값이 필요한 값을 포함 하는 클레임을 나타냅니다.

```qsharp
function EqualityWithinToleranceFact (actual : Double, expected : Double, tolerance : Double) : Unit
```


## <a name="input"></a>입력

### <a name="actual--double"></a>실제: [Double](xref:microsoft.quantum.lang-ref.double)

확인할 숫자입니다.


### <a name="expected--double"></a>예상: [Double](xref:microsoft.quantum.lang-ref.double)

예상 값입니다.


### <a name="tolerance--double"></a>허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)

실제 및 예상의 차이에 대 한 절대 허용 오차입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

