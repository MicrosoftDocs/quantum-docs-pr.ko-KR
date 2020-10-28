---
uid: Microsoft.Quantum.Math.ComplexPolar
title: ComplexPolar 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: 0c18c3f02cb036f22a68b6e4b46fd19049dc34cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709647"
---
# <a name="complexpolar-user-defined-type"></a>ComplexPolar 사용자 정의 형식

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지 [](https://nuget.org/packages/)


극좌표 형식의 복소수를 나타냅니다.

복소수의 극좌표 표현은 $c = r e ^ {i t} $입니다.

```qsharp

newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```



## <a name="named-items"></a>명명 된 항목

### <a name="magnitude--double"></a>크기: [Double](xref:microsoft.quantum.lang-ref.double)

$C $의 \ge $0 $r 절대값입니다.
### <a name="argument--double"></a>인수: [Double](xref:microsoft.quantum.lang-ref.double)

$C $의 단계 $t \in \mathbb R $