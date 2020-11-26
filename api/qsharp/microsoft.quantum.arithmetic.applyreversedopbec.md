---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC
title: ApplyReversedOpBEC 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBEC
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 3a5fef3bb4549433540b2a7b5e94d3cd2d527639
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202773"
---
# <a name="applyreversedopbec-operation"></a><span data-ttu-id="41591-102">ApplyReversedOpBEC 작업</span><span class="sxs-lookup"><span data-stu-id="41591-102">ApplyReversedOpBEC operation</span></span>

<span data-ttu-id="41591-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="41591-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="41591-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="41591-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="41591-105">빅 endian 입력을 사용 하는 작업을 작은 endian 형식을 사용 하 여 부호 없는 정수로 등록 인코딩에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="41591-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="41591-106">입력</span><span class="sxs-lookup"><span data-stu-id="41591-106">Input</span></span>

### <a name="op--bigendian--unit--is-ctl"></a><span data-ttu-id="41591-107">op: [이상](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) 이 고가는 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="41591-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="41591-108">빅 endian 레지스터에 대해 작동 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="41591-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="41591-109">등록: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="41591-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="41591-110">변형할 작은 endian 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="41591-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="41591-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="41591-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="41591-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="41591-112">See Also</span></span>

- [<span data-ttu-id="41591-113">ApplyReversedOpBE.</span><span class="sxs-lookup"><span data-stu-id="41591-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [<span data-ttu-id="41591-114">ApplyReversedOpBEA.</span><span class="sxs-lookup"><span data-stu-id="41591-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="41591-115">ApplyReversedOpBECA.</span><span class="sxs-lookup"><span data-stu-id="41591-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)