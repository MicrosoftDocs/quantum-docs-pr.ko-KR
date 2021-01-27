---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC
title: ApplyReversedOpLEC 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpLEC
qsharp.summary: Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.
ms.openlocfilehash: 74ecc705a6e3d1d59c4c4ae71d30171c12fa45ae
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843511"
---
# <a name="applyreversedoplec-operation"></a><span data-ttu-id="87e9d-102">ApplyReversedOpLEC 작업</span><span class="sxs-lookup"><span data-stu-id="87e9d-102">ApplyReversedOpLEC operation</span></span>

<span data-ttu-id="87e9d-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="87e9d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="87e9d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="87e9d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="87e9d-105">빅 endian 형식을 사용 하 여 부호 없는 정수를 레지스터 인코딩에 사용 하는 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="87e9d-105">Applies an operation that takes little-endian input to a register encoding an unsigned integer using big-endian format.</span></span>

```qsharp
operation ApplyReversedOpLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl), register : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="87e9d-106">입력</span><span class="sxs-lookup"><span data-stu-id="87e9d-106">Input</span></span>

### <a name="op--littleendian--unit--is-ctl"></a><span data-ttu-id="87e9d-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="87e9d-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="87e9d-108">작은 endian 레지스터에 대해 작동 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="87e9d-108">Operation that acts on a little-endian register.</span></span>


### <a name="register--bigendian"></a><span data-ttu-id="87e9d-109">레지스터:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="87e9d-109">register : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="87e9d-110">변형할 빅 endian 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="87e9d-110">A big-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="87e9d-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="87e9d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="87e9d-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="87e9d-112">See Also</span></span>

- [<span data-ttu-id="87e9d-113">ApplyReversedOpLE.</span><span class="sxs-lookup"><span data-stu-id="87e9d-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpLE</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [<span data-ttu-id="87e9d-114">ApplyReversedOpLEA.</span><span class="sxs-lookup"><span data-stu-id="87e9d-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEA)
- [<span data-ttu-id="87e9d-115">ApplyReversedOpLECA.</span><span class="sxs-lookup"><span data-stu-id="87e9d-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)