---
uid: Microsoft.Quantum.Math.BigFraction
title: 이상 소수 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: bfbf49e7a3d060417e506a1977c20adc08b81f0e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846912"
---
# <a name="bigfraction-user-defined-type"></a>이상 소수 사용자 정의 형식

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


폼의 유리수를 나타냅니다 `p/q` . 정수 `p` 는 튜플의 첫 번째 요소이 고 `q` 는 튜플의 두 번째 요소입니다.

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a>명명 된 항목

### <a name="numerator--bigint"></a>분자: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

분수의 분자입니다.
### <a name="denominator--bigint"></a>분모: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

분수의 분모입니다.