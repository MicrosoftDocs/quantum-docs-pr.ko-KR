---
uid: Microsoft.Quantum.Math.RealMod
title: RealMod 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 20916d8462288395384aa875bfae4f042ba6b6ad
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228256"
---
# <a name="realmod-function"></a>RealMod 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


두 실수 사이의 모듈러스를 계산 합니다.

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a>입력

### <a name="value--double"></a>값: [Double](xref:microsoft.quantum.lang-ref.double)

모듈러스를 사용할 실수 $x $입니다.


### <a name="modulo--double"></a>모듈로: [Double](xref:microsoft.quantum.lang-ref.double)

와 관련 하 여 $x $의 모듈러스를 사용 하는 실수입니다.


### <a name="minvalue--double"></a>minValue: [Double](xref:microsoft.quantum.lang-ref.double)

이 함수에서 반환할 최소 값입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>설명

이 함수는 unit 원에 대 한 실제 줄을 래핑하고 입력에 해당 하는 단위 원에서 각도를 찾는 방법으로 실제 모듈러스를 계산 합니다.
`minValue`입력은 unit 원을 잘라낼 위치를 효과적으로 지정 합니다.