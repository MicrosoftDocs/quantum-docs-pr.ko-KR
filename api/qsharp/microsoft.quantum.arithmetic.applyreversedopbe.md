---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBE
title: ApplyReversedOpBE 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBE
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: bf2d43d4e870150f8e6d51dc2f5fb37bdf01d6ec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843607"
---
# <a name="applyreversedopbe-operation"></a><span data-ttu-id="8dbd6-102">ApplyReversedOpBE 작업</span><span class="sxs-lookup"><span data-stu-id="8dbd6-102">ApplyReversedOpBE operation</span></span>

<span data-ttu-id="8dbd6-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8dbd6-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8dbd6-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8dbd6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8dbd6-105">빅 endian 입력을 사용 하는 작업을 작은 endian 형식을 사용 하 여 부호 없는 정수로 등록 인코딩에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dbd6-105">Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.</span></span>

```qsharp
operation ApplyReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="8dbd6-106">입력</span><span class="sxs-lookup"><span data-stu-id="8dbd6-106">Input</span></span>

### <a name="op--bigendian--unit"></a><span data-ttu-id="8dbd6-107">op:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8dbd6-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8dbd6-108">빅 endian 레지스터에 대해 작동 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="8dbd6-108">Operation that acts on a big-endian register.</span></span>


### <a name="register--littleendian"></a><span data-ttu-id="8dbd6-109">등록: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8dbd6-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="8dbd6-110">변형할 작은 endian 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="8dbd6-110">A little-endian register to be transformed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8dbd6-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8dbd6-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="8dbd6-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8dbd6-112">See Also</span></span>

- [<span data-ttu-id="8dbd6-113">ApplyReversedOpBEA.</span><span class="sxs-lookup"><span data-stu-id="8dbd6-113">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [<span data-ttu-id="8dbd6-114">ApplyReversedOpBEC.</span><span class="sxs-lookup"><span data-stu-id="8dbd6-114">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="8dbd6-115">ApplyReversedOpBECA.</span><span class="sxs-lookup"><span data-stu-id="8dbd6-115">Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)