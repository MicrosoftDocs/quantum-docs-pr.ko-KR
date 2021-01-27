---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEC
title: ReversedOpBEC 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEC
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 0674567f5d45890aa2f631b2e0e4d75d20a72449
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846445"
---
# <a name="reversedopbec-function"></a><span data-ttu-id="80eba-102">ReversedOpBEC 함수</span><span class="sxs-lookup"><span data-stu-id="80eba-102">ReversedOpBEC function</span></span>

<span data-ttu-id="80eba-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="80eba-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="80eba-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="80eba-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="80eba-105">빅 endian 입력을 사용 하는 작업의 경우는 작은 endian 입력을 사용 하는 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="80eba-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="80eba-106">입력</span><span class="sxs-lookup"><span data-stu-id="80eba-106">Input</span></span>

### <a name="op--bigendian--unit--is-ctl"></a><span data-ttu-id="80eba-107">op: [이상](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [](xref:microsoft.quantum.lang-ref.unit) 이 고가는 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="80eba-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="80eba-108">입력이 반전 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="80eba-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit--is-ctl"></a><span data-ttu-id="80eba-109">출력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="80eba-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="80eba-110">입력을 작은 endian 레지스터로 허용 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="80eba-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="80eba-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="80eba-111">See Also</span></span>

- [<span data-ttu-id="80eba-112">ApplyReversedOpBEC.</span><span class="sxs-lookup"><span data-stu-id="80eba-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="80eba-113">ReversedOpBE.</span><span class="sxs-lookup"><span data-stu-id="80eba-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="80eba-114">ReversedOpBEA.</span><span class="sxs-lookup"><span data-stu-id="80eba-114">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="80eba-115">ReversedOpBECA.</span><span class="sxs-lookup"><span data-stu-id="80eba-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)