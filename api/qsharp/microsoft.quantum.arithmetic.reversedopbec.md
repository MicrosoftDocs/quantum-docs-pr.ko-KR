---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEC
title: ReversedOpBEC 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEC
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 5e9aa6e6dfef74bca004170cf2b1cd91aa13f0b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719677"
---
# <a name="reversedopbec-function"></a><span data-ttu-id="069a1-102">ReversedOpBEC 함수</span><span class="sxs-lookup"><span data-stu-id="069a1-102">ReversedOpBEC function</span></span>

<span data-ttu-id="069a1-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="069a1-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="069a1-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="069a1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="069a1-105">빅 endian 입력을 사용 하는 작업의 경우는 작은 endian 입력을 사용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="069a1-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="069a1-106">입력</span><span class="sxs-lookup"><span data-stu-id="069a1-106">Input</span></span>

### <a name="op--bigendian--unit-ctl"></a><span data-ttu-id="069a1-107">op:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="069a1-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="069a1-108">입력이 반전 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="069a1-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit-ctl"></a><span data-ttu-id="069a1-109">출력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="069a1-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="069a1-110">입력을 작은 endian 레지스터로 허용 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="069a1-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="069a1-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="069a1-111">See Also</span></span>

- [<span data-ttu-id="069a1-112">ApplyReversedOpBEC.</span><span class="sxs-lookup"><span data-stu-id="069a1-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="069a1-113">ReversedOpBE.</span><span class="sxs-lookup"><span data-stu-id="069a1-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="069a1-114">ReversedOpBEA.</span><span class="sxs-lookup"><span data-stu-id="069a1-114">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="069a1-115">ReversedOpBECA.</span><span class="sxs-lookup"><span data-stu-id="069a1-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)