---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLE
title: ReversedOpLE 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLE
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: d02817e5372b841f3ab633cafa22af603c5310c2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846389"
---
# <a name="reversedople-function"></a><span data-ttu-id="64484-102">ReversedOpLE 함수</span><span class="sxs-lookup"><span data-stu-id="64484-102">ReversedOpLE function</span></span>

<span data-ttu-id="64484-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="64484-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="64484-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="64484-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="64484-105">는 작은 endian 입력을 사용 하는 작업에 대해 빅 endian 입력을 사용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="64484-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)
```


## <a name="input"></a><span data-ttu-id="64484-106">입력</span><span class="sxs-lookup"><span data-stu-id="64484-106">Input</span></span>

### <a name="op--littleendian--unit"></a><span data-ttu-id="64484-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="64484-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="64484-108">입력이 반전 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="64484-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit"></a><span data-ttu-id="64484-109">출력:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="64484-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="64484-110">입력을 빅 endian 레지스터로 허용 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="64484-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="64484-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="64484-111">See Also</span></span>

- [<span data-ttu-id="64484-112">ApplyReversedOpLE.</span><span class="sxs-lookup"><span data-stu-id="64484-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="64484-113">ReversedOpLEA.</span><span class="sxs-lookup"><span data-stu-id="64484-113">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="64484-114">ReversedOpLEC.</span><span class="sxs-lookup"><span data-stu-id="64484-114">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [<span data-ttu-id="64484-115">ReversedOpLECA.</span><span class="sxs-lookup"><span data-stu-id="64484-115">Microsoft.Quantum.Arithmetic.ReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)