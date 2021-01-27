---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBE
title: ReversedOpBE 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBE
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 878b0fae8a803b3136d1537309c945c052e1052c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846477"
---
# <a name="reversedopbe-function"></a><span data-ttu-id="cd52c-102">ReversedOpBE 함수</span><span class="sxs-lookup"><span data-stu-id="cd52c-102">ReversedOpBE function</span></span>

<span data-ttu-id="cd52c-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="cd52c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="cd52c-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cd52c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cd52c-105">빅 endian 입력을 사용 하는 작업의 경우는 작은 endian 입력을 사용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd52c-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)
```


## <a name="input"></a><span data-ttu-id="cd52c-106">입력</span><span class="sxs-lookup"><span data-stu-id="cd52c-106">Input</span></span>

### <a name="op--bigendian--unit"></a><span data-ttu-id="cd52c-107">op:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cd52c-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="cd52c-108">입력이 반전 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="cd52c-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit"></a><span data-ttu-id="cd52c-109">출력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cd52c-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="cd52c-110">입력을 작은 endian 레지스터로 허용 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="cd52c-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd52c-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cd52c-111">See Also</span></span>

- [<span data-ttu-id="cd52c-112">ApplyReversedOpBE.</span><span class="sxs-lookup"><span data-stu-id="cd52c-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="cd52c-113">ReversedOpBEA.</span><span class="sxs-lookup"><span data-stu-id="cd52c-113">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="cd52c-114">ReversedOpBEC.</span><span class="sxs-lookup"><span data-stu-id="cd52c-114">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [<span data-ttu-id="cd52c-115">ReversedOpBECA.</span><span class="sxs-lookup"><span data-stu-id="cd52c-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)