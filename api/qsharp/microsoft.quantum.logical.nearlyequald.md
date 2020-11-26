---
uid: Microsoft.Quantum.Logical.NearlyEqualD
title: NearlyEqualD 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NearlyEqualD
qsharp.summary: Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).
ms.openlocfilehash: 246fad15c691a53fcc5be10f2c713672e0b54e6b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197469"
---
# <a name="nearlyequald-function"></a>NearlyEqualD 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


두 입력이 거의 동일한 경우에만 true를 반환 합니다. 즉, 허용 오차의 허용 오차 범위 내에 있습니다.

```qsharp
function NearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a>입력

### <a name="a--double"></a>a: [Double](xref:microsoft.quantum.lang-ref.double)

비교할 첫 번째 값입니다.


### <a name="b--double"></a>b: [Double](xref:microsoft.quantum.lang-ref.double)

비교할 두 번째 값입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`가와 거의 같은 경우에만입니다 `b` .

## <a name="remarks"></a>설명

다음은 동일 합니다.

```Q#
let cond = Microsoft.Quantum.Math.AbsD(a - b) < 1e-12;
let cond = NearlyEqualD(a, b);
```