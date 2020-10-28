---
uid: Microsoft.Quantum.Logical.NearlyEqualD
title: NearlyEqualD 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NearlyEqualD
qsharp.summary: Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).
ms.openlocfilehash: 332f9ea1753b539eba7b931d5b948b2a238d1abf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709871"
---
# <a name="nearlyequald-function"></a>NearlyEqualD 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지 [](https://nuget.org/packages/)


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