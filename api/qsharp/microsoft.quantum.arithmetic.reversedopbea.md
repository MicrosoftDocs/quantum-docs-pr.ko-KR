---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEA
title: ReversedOpBEA 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: b2418911e71c0b98e1a78247b2ae066887d89cd8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719696"
---
# <a name="reversedopbea-function"></a><span data-ttu-id="6d181-102">ReversedOpBEA 함수</span><span class="sxs-lookup"><span data-stu-id="6d181-102">ReversedOpBEA function</span></span>

<span data-ttu-id="6d181-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="6d181-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="6d181-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6d181-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6d181-105">빅 endian 입력을 사용 하는 작업의 경우는 작은 endian 입력을 사용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d181-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBEA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="6d181-106">입력</span><span class="sxs-lookup"><span data-stu-id="6d181-106">Input</span></span>

### <a name="op--bigendian--unit-adj"></a><span data-ttu-id="6d181-107">op: Adj [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6d181-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="6d181-108">입력이 반전 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="6d181-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit-adj"></a><span data-ttu-id="6d181-109">출력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="6d181-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="6d181-110">입력을 작은 endian 레지스터로 허용 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="6d181-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d181-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6d181-111">See Also</span></span>

- [<span data-ttu-id="6d181-112">ApplyReversedOpBEA.</span><span class="sxs-lookup"><span data-stu-id="6d181-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="6d181-113">ReversedOpBE.</span><span class="sxs-lookup"><span data-stu-id="6d181-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="6d181-114">ReversedOpBEC.</span><span class="sxs-lookup"><span data-stu-id="6d181-114">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [<span data-ttu-id="6d181-115">ReversedOpBECA.</span><span class="sxs-lookup"><span data-stu-id="6d181-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)