---
uid: Microsoft.Quantum.Arithmetic.ApplyLEOperationOnPhaseLEC
title: ApplyLEOperationOnPhaseLEC 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyLEOperationOnPhaseLEC
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.
ms.openlocfilehash: dafe27f66f967fb641a8898672e124c0a51fe687
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190839"
---
# <a name="applyleoperationonphaselec-operation"></a><span data-ttu-id="735c6-102">ApplyLEOperationOnPhaseLEC 작업</span><span class="sxs-lookup"><span data-stu-id="735c6-102">ApplyLEOperationOnPhaseLEC operation</span></span>

<span data-ttu-id="735c6-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="735c6-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="735c6-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="735c6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="735c6-105"><xref:microsoft.quantum.arithmetic.phaselittleendian>형식의 대상 레지스터에서 등록을 입력으로 사용 하는 작업을 적용 <xref:microsoft.quantum.arithmetic.littleendian> 합니다.</span><span class="sxs-lookup"><span data-stu-id="735c6-105">Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.</span></span>

```qsharp
operation ApplyLEOperationOnPhaseLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl), target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="735c6-106">입력</span><span class="sxs-lookup"><span data-stu-id="735c6-106">Input</span></span>

### <a name="op--littleendian--unit--is-ctl"></a><span data-ttu-id="735c6-107">op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="735c6-107">op : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="735c6-108">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="735c6-108">The operation to be applied.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="735c6-109">대상: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="735c6-109">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="735c6-110">작업이 적용 되는 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="735c6-110">The register to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="735c6-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="735c6-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="735c6-112">설명</span><span class="sxs-lookup"><span data-stu-id="735c6-112">Remarks</span></span>

<span data-ttu-id="735c6-113">레지스터는를 사용 하 `LittleEndian` 여로 변환 된 <xref:microsoft.quantum.canon.qftle> 다음의 응용 프로그램 후 원래 표현으로 반환 됩니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="735c6-113">The register is transformed to `LittleEndian` by the use of <xref:microsoft.quantum.canon.qftle> and is then returned to its original representation after application of `op`.</span></span>

## <a name="see-also"></a><span data-ttu-id="735c6-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="735c6-114">See Also</span></span>

- [<span data-ttu-id="735c6-115">ApplyLEOperationonPhaseLE입니다.</span><span class="sxs-lookup"><span data-stu-id="735c6-115">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE)
- [<span data-ttu-id="735c6-116">ApplyLEOperationonPhaseLEA입니다.</span><span class="sxs-lookup"><span data-stu-id="735c6-116">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEA</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEA)
- [<span data-ttu-id="735c6-117">ApplyLEOperationonPhaseLECA입니다.</span><span class="sxs-lookup"><span data-stu-id="735c6-117">Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA</span></span>](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLECA)