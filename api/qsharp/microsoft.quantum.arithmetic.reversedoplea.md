---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLEA
title: ReversedOpLEA 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLEA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: b0fcf1c735bb19308a381307e64314d9d961e5da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846423"
---
# <a name="reversedoplea-function"></a><span data-ttu-id="b3505-102">ReversedOpLEA 함수</span><span class="sxs-lookup"><span data-stu-id="b3505-102">ReversedOpLEA function</span></span>

<span data-ttu-id="b3505-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b3505-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b3505-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b3505-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b3505-105">는 작은 endian 입력을 사용 하는 작업에 대해 빅 endian 입력을 사용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3505-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLEA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="b3505-106">입력</span><span class="sxs-lookup"><span data-stu-id="b3505-106">Input</span></span>

### <a name="op--littleendian--unit--is-adj"></a><span data-ttu-id="b3505-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="b3505-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="b3505-108">입력이 반전 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b3505-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit--is-adj"></a><span data-ttu-id="b3505-109">출력: Adj [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b3505-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="b3505-110">입력을 빅 endian 레지스터로 허용 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b3505-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3505-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b3505-111">See Also</span></span>

- [<span data-ttu-id="b3505-112">ApplyReversedOpLEA.</span><span class="sxs-lookup"><span data-stu-id="b3505-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="b3505-113">ReversedOpLE.</span><span class="sxs-lookup"><span data-stu-id="b3505-113">Microsoft.Quantum.Arithmetic.ReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [<span data-ttu-id="b3505-114">ReversedOpLEC.</span><span class="sxs-lookup"><span data-stu-id="b3505-114">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [<span data-ttu-id="b3505-115">ReversedOpLECA.</span><span class="sxs-lookup"><span data-stu-id="b3505-115">Microsoft.Quantum.Arithmetic.ReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)