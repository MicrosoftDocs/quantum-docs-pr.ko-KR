---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLECA
title: ReversedOpLECA 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLECA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: b5413e43ad50ba7252705ef53b21e63650dbb2a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719617"
---
# <a name="reversedopleca-function"></a><span data-ttu-id="3ce56-102">ReversedOpLECA 함수</span><span class="sxs-lookup"><span data-stu-id="3ce56-102">ReversedOpLECA function</span></span>

<span data-ttu-id="3ce56-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3ce56-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3ce56-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3ce56-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3ce56-105">는 작은 endian 입력을 사용 하는 작업에 대해 빅 endian 입력을 사용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce56-105">Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.</span></span>

```qsharp
function ReversedOpLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="3ce56-106">입력</span><span class="sxs-lookup"><span data-stu-id="3ce56-106">Input</span></span>

### <a name="op--littleendian--unit-adj--ctl"></a><span data-ttu-id="3ce56-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="3ce56-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="3ce56-108">입력이 반전 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="3ce56-108">The operation whose input is to be reversed.</span></span>



## <a name="output--bigendian--unit-adj--ctl"></a><span data-ttu-id="3ce56-109">출력: Adj [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="3ce56-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="3ce56-110">입력을 빅 endian 레지스터로 허용 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="3ce56-110">A new operation that accepts its input as a big-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ce56-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3ce56-111">See Also</span></span>

- [<span data-ttu-id="3ce56-112">ApplyReversedOpLECA.</span><span class="sxs-lookup"><span data-stu-id="3ce56-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)
- [<span data-ttu-id="3ce56-113">ReversedOpLE.</span><span class="sxs-lookup"><span data-stu-id="3ce56-113">Microsoft.Quantum.Arithmetic.ReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [<span data-ttu-id="3ce56-114">ReversedOpLEA.</span><span class="sxs-lookup"><span data-stu-id="3ce56-114">Microsoft.Quantum.Arithmetic.ReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [<span data-ttu-id="3ce56-115">ReversedOpLEC.</span><span class="sxs-lookup"><span data-stu-id="3ce56-115">Microsoft.Quantum.Arithmetic.ReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)