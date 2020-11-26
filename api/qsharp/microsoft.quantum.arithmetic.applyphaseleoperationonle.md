---
uid: Microsoft.Quantum.Arithmetic.ApplyPhaseLEOperationOnLE
title: ApplyPhaseLEOperationOnLE 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyPhaseLEOperationOnLE
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.
ms.openlocfilehash: adccad53e8d874cb2879d7005711624bbcc69201
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190771"
---
# <a name="applyphaseleoperationonle-operation"></a><span data-ttu-id="438b6-102">ApplyPhaseLEOperationOnLE 작업</span><span class="sxs-lookup"><span data-stu-id="438b6-102">ApplyPhaseLEOperationOnLE operation</span></span>

<span data-ttu-id="438b6-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="438b6-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="438b6-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="438b6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="438b6-105"><xref:microsoft.quantum.arithmetic.littleendian>형식의 대상 레지스터에서 등록을 입력으로 사용 하는 작업을 적용 <xref:microsoft.quantum.arithmetic.phaselittleendian> 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b6-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.</span></span>

```qsharp
operation ApplyPhaseLEOperationOnLE (op : (Microsoft.Quantum.Arithmetic.PhaseLittleEndian => Unit), target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="438b6-106">입력</span><span class="sxs-lookup"><span data-stu-id="438b6-106">Input</span></span>

### <a name="op--phaselittleendian--unit"></a><span data-ttu-id="438b6-107">op: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="438b6-107">op : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="438b6-108">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="438b6-108">The operation to be applied.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="438b6-109">대상: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="438b6-109">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="438b6-110">작업이 적용 되는 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="438b6-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="438b6-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="438b6-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="438b6-112">설명</span><span class="sxs-lookup"><span data-stu-id="438b6-112">Remarks</span></span>

<span data-ttu-id="438b6-113">레지스터는를 사용 하 `PhaseLittleEndian` 여로 변환 된 <xref:microsoft.quantum.canon.qftle> 다음의 응용 프로그램 후 원래 표현으로 반환 됩니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="438b6-113">The register is transformed to `PhaseLittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="438b6-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="438b6-114">See Also</span></span>

- [<span data-ttu-id="438b6-115">ApplyPhaseLEOperationonLEA입니다.</span><span class="sxs-lookup"><span data-stu-id="438b6-115">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [<span data-ttu-id="438b6-116">ApplyPhaseLEOperationonLEA입니다.</span><span class="sxs-lookup"><span data-stu-id="438b6-116">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [<span data-ttu-id="438b6-117">ApplyPhaseLEOperationonLECA입니다.</span><span class="sxs-lookup"><span data-stu-id="438b6-117">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA)