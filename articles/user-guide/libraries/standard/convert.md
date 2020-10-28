---
title: '표준 라이브러리의 형식 변환 :::no-loc(Q#):::'
description: '표준 라이브러리의 공용 및 사용자 정의 형식 변환 함수에 대해 알아봅니다 :::no-loc(Q#)::: .'
author: cgranade
uid: microsoft.quantum.libraries.convert
ms.author: chgranad
ms.topic: article
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: 9ec3a2ecd2aa59a10a7033e7b3067eb147ce4035
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691108"
---
# <a name="type-conversions"></a><span data-ttu-id="813ca-103">형식 변환</span><span class="sxs-lookup"><span data-stu-id="813ca-103">Type Conversions</span></span> #

<span data-ttu-id="813ca-104">:::no-loc(Q#)::: 는 **강력한** 형식의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="813ca-104">:::no-loc(Q#)::: is a **strongly-typed** language.</span></span>
<span data-ttu-id="813ca-105">특히 :::no-loc(Q#)::: 은 고유 형식 간에 암시적으로 캐스팅 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="813ca-105">In particular, :::no-loc(Q#)::: does not implicitly cast between distinct types.</span></span> <span data-ttu-id="813ca-106">예를 들어 `1 + 2.0` 은 유효한 식이 아닙니다 :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="813ca-106">For instance, `1 + 2.0` is not a valid :::no-loc(Q#)::: expression.</span></span>
<span data-ttu-id="813ca-107">대신는 :::no-loc(Q#)::: 지정 된 형식의 새 값을 생성 하기 위한 다양 한 형식 변환 함수를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="813ca-107">Rather, :::no-loc(Q#)::: provides a variety of type conversion functions for constructing new values of a given type.</span></span>

<span data-ttu-id="813ca-108">예를 들어에는 <xref:Microsoft.Quantum.Core.Length> 의 출력 형식이 `Int` 있으므로 `Double` 부동 소수점 식의 일부로 사용 하려면 먼저 해당 출력을로 변환 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="813ca-108">For example, <xref:Microsoft.Quantum.Core.Length> has an output type of `Int`, so its output must first be converted to a `Double` before it can be used as a part of a floating-point expression.</span></span>
<span data-ttu-id="813ca-109">함수를 사용 하 여이 작업을 수행할 수 있습니다 <xref:Microsoft.Quantum.Convert.IntAsDouble> .</span><span class="sxs-lookup"><span data-stu-id="813ca-109">This can be done using the <xref:Microsoft.Quantum.Convert.IntAsDouble> function:</span></span>

```qsharp
open Microsoft.Quantum.Convert as Convert;

function HalfLength<'T>(arr : 'T[]) : Double {
    return Convert.IntAsDouble(Length(arr)) / 2.0;
}
```

<span data-ttu-id="813ca-110"><xref:Microsoft.Quantum.Convert>네임 스페이스는,,, 및와 같은 기본 제공 형식으로 작업 하기 위한 일반적인 형식 변환 함수를 제공 합니다 `Int` `Double` `BigInt` `Result` `Bool` .</span><span class="sxs-lookup"><span data-stu-id="813ca-110">The <xref:Microsoft.Quantum.Convert> namespace provides common type conversion functions for working with the basic built-in types, such as `Int`, `Double`, `BigInt`, `Result`, and `Bool`:</span></span>

```qsharp
let bool = Convert.ResultAsBool(One);        // true
let big = Convert.IntAsBigInt(271);          // 271L
let indices = Convert.RangeAsIntArray(0..4); // [0, 1, 2, 3, 4]
```

<span data-ttu-id="813ca-111"><xref:Microsoft.Quantum.Convert>네임 스페이스는 `FunctionAsOperation` 함수를 새 작업으로 변환 하는 등의 몇 가지 exotic 변환을 제공 `'T -> 'U` `'T => 'U` 합니다.</span><span class="sxs-lookup"><span data-stu-id="813ca-111">The <xref:Microsoft.Quantum.Convert> namespace also provides some more exotic conversions, such as `FunctionAsOperation`, which converts functions `'T -> 'U` into new operations `'T => 'U`.</span></span>

<span data-ttu-id="813ca-112">마지막으로, :::no-loc(Q#)::: 표준 라이브러리는 및와 같은 다양 한 사용자 정의 형식을 제공 <xref:Microsoft.Quantum.Math.Complex> 합니다 <xref:Microsoft.Quantum.Arithmetic.LittleEndian> .</span><span class="sxs-lookup"><span data-stu-id="813ca-112">Finally, the :::no-loc(Q#)::: standard library provides a number of user-defined types such as <xref:Microsoft.Quantum.Math.Complex> and <xref:Microsoft.Quantum.Arithmetic.LittleEndian>.</span></span>
<span data-ttu-id="813ca-113">이러한 형식과 함께 표준 라이브러리는 다음과 같은 함수를 제공 합니다 <xref:Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian> .</span><span class="sxs-lookup"><span data-stu-id="813ca-113">Along with these types, the standard library provides functions such as <xref:Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian>:</span></span>

```:::no-loc(Q#):::
open Microsoft.Quantum.Arithmetic as Arithmetic;

let register = Arithmetic.BigEndian(qubits);
IncrementByInteger(Arithmetic.BigEndianAsLittleEndian(register));
```
