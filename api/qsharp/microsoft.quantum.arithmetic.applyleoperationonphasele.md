---
uid: Microsoft.Quantum.Arithmetic.ApplyLEOperationOnPhaseLE
title: ApplyLEOperationOnPhaseLE 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyLEOperationOnPhaseLE
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.
ms.openlocfilehash: ff8e9424b1fc179f25ca926520338a4bbbcd04c0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721633"
---
# <a name="applyleoperationonphasele-operation"></a><span data-ttu-id="13070-102">ApplyLEOperationOnPhaseLE 작업</span><span class="sxs-lookup"><span data-stu-id="13070-102">ApplyLEOperationOnPhaseLE operation</span></span>

<span data-ttu-id="13070-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="13070-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="13070-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="13070-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="13070-105"><xref:microsoft.quantum.arithmetic.phaselittleendian>형식의 대상 레지스터에서 등록을 입력으로 사용 하는 작업을 적용 <xref:microsoft.quantum.arithmetic.littleendian> 합니다.</span><span class="sxs-lookup"><span data-stu-id="13070-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>

```qsharp
operation ApplyLEOperationOnPhaseLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit), target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="13070-106">입력</span><span class="sxs-lookup"><span data-stu-id="13070-106">Input</span></span>

### <a name="op--littleendian--unit"></a><span data-ttu-id="13070-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="13070-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="13070-108">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="13070-108">The operation to be applied.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="13070-109">대상: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="13070-109">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="13070-110">작업이 적용 되는 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="13070-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="13070-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="13070-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="13070-112">설명</span><span class="sxs-lookup"><span data-stu-id="13070-112">Remarks</span></span>

<span data-ttu-id="13070-113">레지스터는를 사용 하 `LittleEndian` 여로 변환 된 <xref:microsoft.quantum.canon.qftle> 다음의 응용 프로그램 후 원래 표현으로 반환 됩니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="13070-113">The register is transformed to `LittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="13070-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="13070-114">See Also</span></span>

- [<span data-ttu-id="13070-115">ApplyLEOperationonPhaseLEA입니다.</span><span class="sxs-lookup"><span data-stu-id="13070-115">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEA)
- [<span data-ttu-id="13070-116">ApplyLEOperationonPhaseLEC입니다.</span><span class="sxs-lookup"><span data-stu-id="13070-116">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEC</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEC)
- [<span data-ttu-id="13070-117">ApplyLEOperationonPhaseLECA입니다.</span><span class="sxs-lookup"><span data-stu-id="13070-117">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA)