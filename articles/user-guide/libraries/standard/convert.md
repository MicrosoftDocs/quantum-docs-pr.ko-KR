---
title: 표준 라이브러리의 형식 변환 Q#
description: 표준 라이브러리의 공용 및 사용자 정의 형식 변환 함수에 대해 알아봅니다 Q# .
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad
ms.topic: conceptual
no-loc:
- Q#
- $$v
ms.openlocfilehash: 67f47339363a52097f342c8ae4e43a8a93d606a8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858017"
---
# <a name="type-conversions"></a>형식 변환 #

Q# 는 **강력한** 형식의 언어입니다.
특히 Q# 은 고유 형식 간에 암시적으로 캐스팅 되지 않습니다. 예를 들어 `1 + 2.0` 은 유효한 식이 아닙니다 Q# .
대신는 Q# 지정 된 형식의 새 값을 생성 하기 위한 다양 한 형식 변환 함수를 제공 합니다.

예를 들어에는 <xref:Microsoft.Quantum.Core.Length> 의 출력 형식이 `Int` 있으므로 `Double` 부동 소수점 식의 일부로 사용 하려면 먼저 해당 출력을로 변환 해야 합니다.
함수를 사용 하 여이 작업을 수행할 수 있습니다 <xref:Microsoft.Quantum.Convert.IntAsDouble> .

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<xref:Microsoft.Quantum.Convert>네임 스페이스는,,, 및와 같은 기본 제공 형식으로 작업 하기 위한 일반적인 형식 변환 함수를 제공 합니다 `Int` `Double` `BigInt` `Result` `Bool` .

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

<xref:Microsoft.Quantum.Convert>네임 스페이스는 `FunctionAsOperation` 함수를 새 작업으로 변환 하는 등의 몇 가지 exotic 변환을 제공 `'T -> 'U` `'T => 'U` 합니다.

마지막으로, Q# 표준 라이브러리는 및와 같은 다양 한 사용자 정의 형식을 제공 <xref:Microsoft.Quantum.Math.Complex> 합니다 <xref:Microsoft.Quantum.Arithmetic.LittleEndian> .
이러한 형식과 함께 표준 라이브러리는 다음과 같은 함수를 제공 합니다 <xref:Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian> .

```qsharp
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
