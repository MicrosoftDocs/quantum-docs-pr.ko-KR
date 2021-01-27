---
uid: Microsoft.Quantum.Bitwise.Parity
title: 패리티 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Parity
qsharp.summary: Returns the bitwise PARITY of an integer (1 if its binary representation contains odd number of ones and 0 otherwise).
ms.openlocfilehash: b34ef36b0336ec1dea7fdbd878c6d695b38d623e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842136"
---
# <a name="parity-function"></a><span data-ttu-id="13026-102">패리티 함수</span><span class="sxs-lookup"><span data-stu-id="13026-102">Parity function</span></span>

<span data-ttu-id="13026-103">네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="13026-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="13026-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="13026-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="13026-105">정수의 비트 패리티를 반환 합니다 (이진 표현에 홀수 개의 숫자가 포함 된 경우 1, 그렇지 않은 경우 0).</span><span class="sxs-lookup"><span data-stu-id="13026-105">Returns the bitwise PARITY of an integer (1 if its binary representation contains odd number of ones and 0 otherwise).</span></span>

```qsharp
function Parity (a : Int) : Int
```


## <a name="input"></a><span data-ttu-id="13026-106">입력</span><span class="sxs-lookup"><span data-stu-id="13026-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="13026-107">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="13026-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="13026-108">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="13026-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="example"></a><span data-ttu-id="13026-109">예제</span><span class="sxs-lookup"><span data-stu-id="13026-109">Example</span></span>

```qsharp
let a = 248;
let x = Parity(a); // x : Int = 1.
```