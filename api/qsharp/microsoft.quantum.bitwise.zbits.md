---
uid: Microsoft.Quantum.Bitwise.ZBits
title: ZBits 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: ZBits
qsharp.summary: Returns an integer representing the Z bits of an array of Pauli operators.
ms.openlocfilehash: 3ded981dc53236a48f1fb8f6ae12e39c17469447
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219450"
---
# <a name="zbits-function"></a><span data-ttu-id="33a83-102">ZBits 함수</span><span class="sxs-lookup"><span data-stu-id="33a83-102">ZBits function</span></span>

<span data-ttu-id="33a83-103">네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="33a83-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="33a83-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="33a83-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="33a83-105">Pauli 연산자 배열의 Z 비트를 나타내는 정수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="33a83-105">Returns an integer representing the Z bits of an array of Pauli operators.</span></span>

```qsharp
function ZBits (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="33a83-106">입력</span><span class="sxs-lookup"><span data-stu-id="33a83-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="33a83-107">paulis: [Paulis](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="33a83-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="33a83-108">정수로 나타낼 Pauli 연산자의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="33a83-108">An array of Pauli operators to be represented as an integer.</span></span>



## <a name="output--int"></a><span data-ttu-id="33a83-109">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="33a83-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="33a83-110">정수 $x $ (p_ {62} \, p_ {61} \, \dots .. \, p_0) $ (여기서 $p _i = $0 인 경우 $p _i = $1 인 경우 `paulis[i]` `PauliI` `PauliX` `paulis[i]` 이 고 `PauliY` `PauliZ` , 그렇지 않으면입니다.</span><span class="sxs-lookup"><span data-stu-id="33a83-110">An integer $x$ with binary representation $(p_{62}\,p_{61}\,\dots\,p_0)$, where $p_i = 0$ if `paulis[i]` is `PauliI` or `PauliX` and where $p_i = 1$ if `paulis[i]` is `PauliY` or `PauliZ`.</span></span>

## <a name="remarks"></a><span data-ttu-id="33a83-111">설명</span><span class="sxs-lookup"><span data-stu-id="33a83-111">Remarks</span></span>

<span data-ttu-id="33a83-112">배열의 길이가 63 보다 큰 경우 함수는을 throw 합니다 `paulis` .</span><span class="sxs-lookup"><span data-stu-id="33a83-112">The function will throw if the length of `paulis` array is greater than 63.</span></span>

## <a name="see-also"></a><span data-ttu-id="33a83-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="33a83-113">See Also</span></span>

- [<span data-ttu-id="33a83-114">Microsoft 양자. x x x 비트</span><span class="sxs-lookup"><span data-stu-id="33a83-114">Microsoft.Quantum.Bitwise.XBits</span></span>](xref:Microsoft.Quantum.Bitwise.XBits)