---
title: 'Q # 표준 라이브러리의 형식 변환'
description: 'Q # 표준 라이브러리의 공용 및 사용자 정의 형식 변환 함수에 대해 알아봅니다.'
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: e941d7e3d76459546861410e91a03d7315183867
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275737"
---
# <a name="type-conversions"></a>형식 변환 #

Q #은 **강력한** 형식의 언어입니다.
특히, Q #은 고유 형식 간에 암시적으로 캐스팅 되지 않습니다. 예를 들어 `1 + 2.0` 는 유효한 Q # 식이 아닙니다.
대신, Q #에서는 지정 된 형식의 새 값을 생성 하기 위한 다양 한 형식 변환 함수를 제공 합니다.

예를 들어에는 <xref:microsoft.quantum.core.length> 의 출력 형식이 `Int` 있으므로 `Double` 부동 소수점 식의 일부로 사용 하려면 먼저 해당 출력을로 변환 해야 합니다.
함수를 사용 하 여이 작업을 수행할 수 있습니다 <xref:microsoft.quantum.convert.intasdouble> .

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<xref:microsoft.quantum.convert>네임 스페이스는,,, 및와 같은 기본 제공 형식으로 작업 하기 위한 일반적인 형식 변환 함수를 제공 합니다 `Int` `Double` `BigInt` `Result` `Bool` .

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

<xref:microsoft.quantum.convert>네임 스페이스는 `FunctionAsOperation` 함수를 새 작업으로 변환 하는 등의 몇 가지 exotic 변환을 제공 `'T -> 'U` `'T => 'U` 합니다.

마지막으로 Q # 표준 라이브러리는 및와 같은 다양 한 사용자 정의 형식을 제공 합니다 <xref:microsoft.quantum.math.complex> <xref:microsoft.quantum.arithmetic.littleendian> .
이러한 형식과 함께 표준 라이브러리는 다음과 같은 함수를 제공 합니다 <xref:microsoft.quantum.arithmetic.bigendianaslittleendian> .

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
