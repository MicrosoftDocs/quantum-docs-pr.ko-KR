---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLE
title: ReversedOpLE 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLE
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: 6ebc4e97cb6d515e99e85922d03ca246b56084ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719648"
---
# <a name="reversedople-function"></a><span data-ttu-id="d0a28-102">ReversedOpLE 함수</span><span class="sxs-lookup"><span data-stu-id="d0a28-102">ReversedOpLE function</span></span>

<span data-ttu-id="d0a28-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="d0a28-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="d0a28-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d0a28-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d0a28-105">는 작은 endian 입력을 사용 하는 작업에 대해 빅 endian 입력을 사용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a28-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)
```


## <a name="input"></a><span data-ttu-id="d0a28-106">입력</span><span class="sxs-lookup"><span data-stu-id="d0a28-106">Input</span></span>

### <a name="op--littleendian--unit"></a><span data-ttu-id="d0a28-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d0a28-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="d0a28-108">입력이 반전 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="d0a28-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit"></a><span data-ttu-id="d0a28-109">출력:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d0a28-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="d0a28-110">입력을 빅 endian 레지스터로 허용 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="d0a28-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0a28-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d0a28-111">See Also</span></span>

- [<span data-ttu-id="d0a28-112">ApplyReversedOpLE.</span><span class="sxs-lookup"><span data-stu-id="d0a28-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="d0a28-113">ReversedOpLEA.</span><span class="sxs-lookup"><span data-stu-id="d0a28-113">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="d0a28-114">ReversedOpLEC.</span><span class="sxs-lookup"><span data-stu-id="d0a28-114">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [<span data-ttu-id="d0a28-115">ReversedOpLECA.</span><span class="sxs-lookup"><span data-stu-id="d0a28-115">Microsoft.Quantum.Arithmetic.ReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)