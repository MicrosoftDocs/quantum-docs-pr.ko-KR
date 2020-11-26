---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLE
title: ApplyReversedOpLE 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLE
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: 16ce6842cdef8e519a13a45640edc3d79cdbce25
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202756"
---
# <a name="applyreversedople-operation"></a><span data-ttu-id="42ac9-102">ApplyReversedOpLE 작업</span><span class="sxs-lookup"><span data-stu-id="42ac9-102">ApplyReversedOpLE operation</span></span>

<span data-ttu-id="42ac9-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="42ac9-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="42ac9-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="42ac9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="42ac9-105">빅 endian 형식을 사용 하 여 부호 없는 정수를 레지스터 인코딩에 사용 하는 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="42ac9-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="42ac9-106">입력</span><span class="sxs-lookup"><span data-stu-id="42ac9-106">Input</span></span>

### <a name="op--littleendian--unit"></a><span data-ttu-id="42ac9-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="42ac9-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="42ac9-108">작은 endian 레지스터에 대해 작동 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="42ac9-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="42ac9-109">레지스터:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="42ac9-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="42ac9-110">변형할 빅 endian 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="42ac9-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="42ac9-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="42ac9-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="42ac9-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="42ac9-112">See Also</span></span>

- [<span data-ttu-id="42ac9-113">ApplyReversedOpLEA.</span><span class="sxs-lookup"><span data-stu-id="42ac9-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="42ac9-114">ApplyReversedOpLEC.</span><span class="sxs-lookup"><span data-stu-id="42ac9-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [<span data-ttu-id="42ac9-115">ApplyReversedOpLECA.</span><span class="sxs-lookup"><span data-stu-id="42ac9-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)