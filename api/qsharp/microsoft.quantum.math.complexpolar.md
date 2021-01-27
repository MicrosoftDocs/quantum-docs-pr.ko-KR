---
uid: Microsoft.Quantum.Math.ComplexPolar
title: ComplexPolar 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: 174e75b82a3ee740cd4d07e5bcd091de65bbc6b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847341"
---
# <a name="complexpolar-user-defined-type"></a>ComplexPolar 사용자 정의 형식

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


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