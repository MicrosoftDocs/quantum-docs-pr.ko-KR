---
uid: Microsoft.Quantum.Arithmetic.ApplyPhaseLEOperationOnLE
title: ApplyPhaseLEOperationOnLE 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyPhaseLEOperationOnLE
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.
ms.openlocfilehash: dacc52766cf72d2bd562b76fc4939f962133e9a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721549"
---
# <a name="applyphaseleoperationonle-operation"></a><span data-ttu-id="79858-102">ApplyPhaseLEOperationOnLE 작업</span><span class="sxs-lookup"><span data-stu-id="79858-102">ApplyPhaseLEOperationOnLE operation</span></span>

<span data-ttu-id="79858-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="79858-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="79858-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="79858-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="79858-105"><xref:microsoft.quantum.arithmetic.littleendian>형식의 대상 레지스터에서 등록을 입력으로 사용 하는 작업을 적용 <xref:microsoft.quantum.arithmetic.phaselittleendian> 합니다.</span><span class="sxs-lookup"><span data-stu-id="79858-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.</span></span>

```qsharp
operation ApplyPhaseLEOperationOnLE (op : (Microsoft.Quantum.Arithmetic.PhaseLittleEndian => Unit), target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="79858-106">입력</span><span class="sxs-lookup"><span data-stu-id="79858-106">Input</span></span>

### <a name="op--phaselittleendian--unit"></a><span data-ttu-id="79858-107">op: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="79858-107">op : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="79858-108">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="79858-108">The operation to be applied.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="79858-109">대상: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="79858-109">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="79858-110">작업이 적용 되는 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="79858-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="79858-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="79858-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="79858-112">설명</span><span class="sxs-lookup"><span data-stu-id="79858-112">Remarks</span></span>

<span data-ttu-id="79858-113">레지스터는를 사용 하 `PhaseLittleEndian` 여로 변환 된 <xref:microsoft.quantum.canon.qftle> 다음의 응용 프로그램 후 원래 표현으로 반환 됩니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="79858-113">The register is transformed to `PhaseLittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="79858-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="79858-114">See Also</span></span>

- [<span data-ttu-id="79858-115">ApplyPhaseLEOperationonLEA입니다.</span><span class="sxs-lookup"><span data-stu-id="79858-115">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [<span data-ttu-id="79858-116">ApplyPhaseLEOperationonLEA입니다.</span><span class="sxs-lookup"><span data-stu-id="79858-116">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [<span data-ttu-id="79858-117">ApplyPhaseLEOperationonLECA입니다.</span><span class="sxs-lookup"><span data-stu-id="79858-117">Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA</span></span>](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA)