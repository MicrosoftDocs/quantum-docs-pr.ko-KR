---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEA
title: ReversedOpBEA 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 392b97171bcfb9d35a38189fc9c27e61cf9cf7d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846466"
---
# <a name="reversedopbea-function"></a><span data-ttu-id="27340-102">ReversedOpBEA 함수</span><span class="sxs-lookup"><span data-stu-id="27340-102">ReversedOpBEA function</span></span>

<span data-ttu-id="27340-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="27340-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="27340-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="27340-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="27340-105">빅 endian 입력을 사용 하는 작업의 경우는 작은 endian 입력을 사용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="27340-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBEA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="27340-106">입력</span><span class="sxs-lookup"><span data-stu-id="27340-106">Input</span></span>

### <a name="op--bigendian--unit--is-adj"></a><span data-ttu-id="27340-107">op: Adj [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="27340-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="27340-108">입력이 반전 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="27340-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit--is-adj"></a><span data-ttu-id="27340-109">출력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="27340-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="27340-110">입력을 작은 endian 레지스터로 허용 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="27340-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="27340-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="27340-111">See Also</span></span>

- [<span data-ttu-id="27340-112">ApplyReversedOpBEA.</span><span class="sxs-lookup"><span data-stu-id="27340-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="27340-113">ReversedOpBE.</span><span class="sxs-lookup"><span data-stu-id="27340-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="27340-114">ReversedOpBEC.</span><span class="sxs-lookup"><span data-stu-id="27340-114">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [<span data-ttu-id="27340-115">ReversedOpBECA.</span><span class="sxs-lookup"><span data-stu-id="27340-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)