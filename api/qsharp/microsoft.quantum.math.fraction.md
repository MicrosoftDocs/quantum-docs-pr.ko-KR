---
uid: Microsoft.Quantum.Math.Fraction
title: 분수 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 350d470c374fc8e0a3f4c4a9a68ad8566ab88727
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723658"
---
# <a name="fraction-user-defined-type"></a>분수 사용자 정의 형식

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지 [](https://nuget.org/packages/)


폼의 유리수를 나타냅니다 `p/q` . 정수 `p` 는 튜플의 첫 번째 요소이 고 `q` 는 튜플의 두 번째 요소입니다.

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a>명명 된 항목

### <a name="numerator--int"></a>분자: [Int](xref:microsoft.quantum.lang-ref.int)

분수의 분자입니다.
### <a name="denominator--int"></a>분모: [Int](xref:microsoft.quantum.lang-ref.int)

분수의 분모입니다.