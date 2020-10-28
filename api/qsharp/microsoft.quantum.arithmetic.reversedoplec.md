---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLEC
title: ReversedOpLEC 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLEC
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: 3a4872be6b81498c26ab9a14134940c5ef8628b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719636"
---
# <a name="reversedoplec-function"></a><span data-ttu-id="41d71-102">ReversedOpLEC 함수</span><span class="sxs-lookup"><span data-stu-id="41d71-102">ReversedOpLEC function</span></span>

<span data-ttu-id="41d71-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="41d71-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="41d71-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="41d71-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="41d71-105">는 작은 endian 입력을 사용 하는 작업에 대해 빅 endian 입력을 사용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="41d71-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="41d71-106">입력</span><span class="sxs-lookup"><span data-stu-id="41d71-106">Input</span></span>

### <a name="op--littleendian--unit-ctl"></a><span data-ttu-id="41d71-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="41d71-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="41d71-108">입력이 반전 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="41d71-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit-ctl"></a><span data-ttu-id="41d71-109">출력:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl</span><span class="sxs-lookup"><span data-stu-id="41d71-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="41d71-110">입력을 빅 endian 레지스터로 허용 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="41d71-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="41d71-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="41d71-111">See Also</span></span>

- [<span data-ttu-id="41d71-112">ApplyReversedOpLEC.</span><span class="sxs-lookup"><span data-stu-id="41d71-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [<span data-ttu-id="41d71-113">ReversedOpLE.</span><span class="sxs-lookup"><span data-stu-id="41d71-113">Microsoft.Quantum.Arithmetic.ReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [<span data-ttu-id="41d71-114">ReversedOpLEA.</span><span class="sxs-lookup"><span data-stu-id="41d71-114">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="41d71-115">ReversedOpLECA.</span><span class="sxs-lookup"><span data-stu-id="41d71-115">Microsoft.Quantum.Arithmetic.ReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)