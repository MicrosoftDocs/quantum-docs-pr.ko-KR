---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBECA
title: ReversedOpBECA 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBECA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 09bb99645d5946af0e0c654500165077691f8da3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846404"
---
# <a name="reversedopbeca-function"></a><span data-ttu-id="71bd6-102">ReversedOpBECA 함수</span><span class="sxs-lookup"><span data-stu-id="71bd6-102">ReversedOpBECA function</span></span>

<span data-ttu-id="71bd6-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="71bd6-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="71bd6-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="71bd6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="71bd6-105">빅 endian 입력을 사용 하는 작업의 경우는 작은 endian 입력을 사용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="71bd6-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBECA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="71bd6-106">입력</span><span class="sxs-lookup"><span data-stu-id="71bd6-106">Input</span></span>

### <a name="op--bigendian--unit--is-adj--ctl"></a><span data-ttu-id="71bd6-107">op: [](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="71bd6-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="71bd6-108">입력이 반전 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="71bd6-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="71bd6-109">출력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="71bd6-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="71bd6-110">입력을 작은 endian 레지스터로 허용 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="71bd6-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="71bd6-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="71bd6-111">See Also</span></span>

- [<span data-ttu-id="71bd6-112">ApplyReversedOpBECA.</span><span class="sxs-lookup"><span data-stu-id="71bd6-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)
- [<span data-ttu-id="71bd6-113">ReversedOpBE.</span><span class="sxs-lookup"><span data-stu-id="71bd6-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="71bd6-114">ReversedOpBEA.</span><span class="sxs-lookup"><span data-stu-id="71bd6-114">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="71bd6-115">ReversedOpBEC.</span><span class="sxs-lookup"><span data-stu-id="71bd6-115">Microsoft.Quantum.Arithmetic.ReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)