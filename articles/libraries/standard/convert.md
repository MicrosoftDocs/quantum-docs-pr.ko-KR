---
title: 'Q # 표준 라이브러리의 형식 변환'
description: 'Q # 표준 라이브러리의 공용 및 사용자 정의 형식 변환 함수에 대해 알아봅니다.'
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: e941d7e3d76459546861410e91a03d7315183867
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907803"
---
# <a name="type-conversions"></a>형식 변환 #

Q #은 **강력한** 형식의 언어입니다.
특히, Q #은 고유 형식 간에 암시적으로 캐스팅 되지 않습니다. 예를 들어 `1 + 2.0`은 올바른 Q # 식이 아닙니다.
대신, Q #에서는 지정 된 형식의 새 값을 생성 하기 위한 다양 한 형식 변환 함수를 제공 합니다.

예를 들어 <xref:microsoft.quantum.core.length>에는 `Int`의 출력 형식이 있으므로 부동 소수점 식의 일부로 사용 하려면 먼저 해당 출력을 `Double`로 변환 해야 합니다.
<xref:microsoft.quantum.convert.intasdouble> 함수를 사용 하 여이 작업을 수행할 수 있습니다.

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<xref:microsoft.quantum.convert> 네임 스페이스는 `Int`, `Double`, `BigInt`, `Result`, `Bool`등의 기본 제공 형식으로 작업 하기 위한 일반적인 형식 변환 함수를 제공 합니다.

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

또한 <xref:microsoft.quantum.convert> 네임 스페이스는 함수 `'T -> 'U`를 새 작업 `'T => 'U`변환 하는 `FunctionAsOperation`와 같은 몇 가지 exotic 변환을 제공 합니다.

마지막으로 Q # 표준 라이브러리는 <xref:microsoft.quantum.math.complex> 및 <xref:microsoft.quantum.arithmetic.littleendian>와 같은 여러 사용자 정의 형식을 제공 합니다.
이러한 형식과 함께 표준 라이브러리는 <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>와 같은 함수를 제공 합니다.

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
