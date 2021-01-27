---
uid: Microsoft.Quantum.Diagnostics.NearEqualityFactD
title: NearEqualityFactD 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: NearEqualityFactD
qsharp.summary: Asserts that a classical floating point value has the expected value up to a small tolerance of 1e-10.
ms.openlocfilehash: d632a7a12c9ebbebfbc7939f2b8a24de8ae1ba2a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827902"
---
# <a name="nearequalityfactd-function"></a>NearEqualityFactD 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


고전적인 부동 소수점 값에 필요한 값이 1e-10의 최대 허용 오차 보다 작은 것을 어설션 합니다.

```qsharp
function NearEqualityFactD (actual : Double, expected : Double) : Unit
```


## <a name="input"></a>입력

### <a name="actual--double"></a>실제: [Double](xref:microsoft.quantum.lang-ref.double)

확인할 숫자입니다.


### <a name="expected--double"></a>예상: [Double](xref:microsoft.quantum.lang-ref.double)

예상 값입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

이는 <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact> 하드 코드 된 허용 오차를 $10 ^ $로 사용 하는 것과 같습니다 {-10} .