---
title: 'Q # 표준 라이브러리-형식 변환 | Microsoft Docs'
description: 'Q # 표준 라이브러리-형식 변환'
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: 4716f0d9562229f08ef6f0f5f80961f793de4c5c
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2019
ms.locfileid: "73184477"
---
# <a name="type-conversions"></a><span data-ttu-id="d2472-103">형식 변환</span><span class="sxs-lookup"><span data-stu-id="d2472-103">Type Conversions</span></span> #

<span data-ttu-id="d2472-104">Q #은 **강력한** 형식의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="d2472-104">Q# is a **strongly-typed** language.</span></span>
<span data-ttu-id="d2472-105">특히, Q #은 고유 형식 간에 암시적으로 캐스팅 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2472-105">In particular, Q# does not implicitly cast between distinct types.</span></span> <span data-ttu-id="d2472-106">예를 들어 `1 + 2.0`은 올바른 Q # 식이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="d2472-106">For instance, `1 + 2.0` is not a valid Q# expression.</span></span>
<span data-ttu-id="d2472-107">대신, Q #에서는 지정 된 형식의 새 값을 생성 하기 위한 다양 한 형식 변환 함수를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2472-107">Rather, Q# provides a variety of type conversion functions for constructing new values of a given type.</span></span>

<span data-ttu-id="d2472-108">예를 들어 <xref:microsoft.quantum.core.length>에는 `Int`의 출력 형식이 있으므로 부동 소수점 식의 일부로 사용 하려면 먼저 해당 출력을 `Double`로 변환 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2472-108">For example, <xref:microsoft.quantum.core.length> has an output type of `Int`, so its output must first be converted to a `Double` before it can be used as a part of a floating-point expression.</span></span>
<span data-ttu-id="d2472-109"><xref:microsoft.quantum.convert.intasdouble> 함수를 사용 하 여이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2472-109">This can be done using the <xref:microsoft.quantum.convert.intasdouble> function:</span></span>

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<span data-ttu-id="d2472-110"><xref:microsoft.quantum.convert> 네임 스페이스는 `Int`, `Double`, `BigInt`, `Result`, `Bool`등의 기본 제공 형식으로 작업 하기 위한 일반적인 형식 변환 함수를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2472-110">The <xref:microsoft.quantum.convert> namespace provides common type conversion functions for working with the basic built-in types, such as `Int`, `Double`, `BigInt`, `Result`, and `Bool`:</span></span>

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

<span data-ttu-id="d2472-111">또한 <xref:microsoft.quantum.convert> 네임 스페이스는 함수 `'T -> 'U`를 새 작업 `'T => 'U`변환 하는 `FunctionAsOperation`와 같은 몇 가지 exotic 변환을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2472-111">The <xref:microsoft.quantum.convert> namespace also provides some more exotic conversions, such as `FunctionAsOperation`, which converts functions `'T -> 'U` into new operations `'T => 'U`.</span></span>

<span data-ttu-id="d2472-112">마지막으로 Q # 표준 라이브러리는 <xref:microsoft.quantum.math.complex> 및 <xref:microsoft.quantum.arithmetic.littleendian>와 같은 여러 사용자 정의 형식을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2472-112">Finally, the Q# standard library provides a number of user-defined types such as <xref:microsoft.quantum.math.complex> and <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>
<span data-ttu-id="d2472-113">이러한 형식과 함께 표준 라이브러리는 <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>와 같은 함수를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2472-113">Along with these types, the standard library provides functions such as <xref:microsoft.quantum.arithmetic.bigendianaslittleendian>:</span></span>

```Q#
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
