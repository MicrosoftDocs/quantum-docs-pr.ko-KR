---
uid: Microsoft.Quantum.Bitwise.XBits
title: XBits 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: XBits
qsharp.summary: Returns an integer representing the X bits of an array of Pauli operators.
ms.openlocfilehash: 91619803c7efe56e617b16637f5302aa0b7978ec
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718561"
---
# <a name="xbits-function"></a><span data-ttu-id="f3a3c-102">XBits 함수</span><span class="sxs-lookup"><span data-stu-id="f3a3c-102">XBits function</span></span>

<span data-ttu-id="f3a3c-103">네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="f3a3c-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="f3a3c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f3a3c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f3a3c-105">Pauli 연산자 배열의 X 비트를 나타내는 정수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a3c-105">Returns an integer representing the X bits of an array of Pauli operators.</span></span>

```qsharp
function XBits (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="f3a3c-106">입력</span><span class="sxs-lookup"><span data-stu-id="f3a3c-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="f3a3c-107">paulis: [Paulis](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="f3a3c-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="f3a3c-108">정수로 나타낼 Pauli 연산자의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f3a3c-108">An array of Pauli operators to be represented as an integer.</span></span>



## <a name="output--int"></a><span data-ttu-id="f3a3c-109">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f3a3c-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f3a3c-110">정수 $x $ (p_ {62} \, p_ {61} \, \dots .. \, p_0) $ (여기서 $p _i = $0 인 경우 $p _i = $1 인 경우 `paulis[i]` `PauliI` `PauliZ` `paulis[i]` 이 고 `PauliX` `PauliY` , 그렇지 않으면입니다.</span><span class="sxs-lookup"><span data-stu-id="f3a3c-110">An integer $x$ with binary representation $(p_{62}\,p_{61}\,\dots\,p_0)$, where $p_i = 0$ if `paulis[i]` is `PauliI` or `PauliZ` and where $p_i = 1$ if `paulis[i]` is `PauliX` or `PauliY`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3a3c-111">설명</span><span class="sxs-lookup"><span data-stu-id="f3a3c-111">Remarks</span></span>

<span data-ttu-id="f3a3c-112">배열의 길이가 63 보다 큰 경우 함수는을 throw 합니다 `paulis` .</span><span class="sxs-lookup"><span data-stu-id="f3a3c-112">The function will throw if the length of `paulis` array is greater than 63.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3a3c-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f3a3c-113">See Also</span></span>

- [<span data-ttu-id="f3a3c-114">Microsoft 양자. i m b 비트</span><span class="sxs-lookup"><span data-stu-id="f3a3c-114">Microsoft.Quantum.Bitwise.ZBits</span></span>](xref:Microsoft.Quantum.Bitwise.ZBits)