---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: MeasureInteger 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: 7cd2d93332eb168c7c2be92a3b910033ca8c10ae
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720968"
---
# <a name="measureinteger-operation"></a><span data-ttu-id="8fef7-102">MeasureInteger 작업</span><span class="sxs-lookup"><span data-stu-id="8fef7-102">MeasureInteger operation</span></span>

<span data-ttu-id="8fef7-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8fef7-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8fef7-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8fef7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8fef7-105">퀀텀 레지스터의 콘텐츠를 측정 하 고 정수로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fef7-105">Measures the content of a quantum register and converts it to an integer.</span></span> <span data-ttu-id="8fef7-106">측정은 표준 계산 기준, 즉의 eigenbasis을 기준으로 수행 `PauliZ` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fef7-106">The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.</span></span>

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a><span data-ttu-id="8fef7-107">입력</span><span class="sxs-lookup"><span data-stu-id="8fef7-107">Input</span></span>

### <a name="target--littleendian"></a><span data-ttu-id="8fef7-108">대상: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8fef7-108">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="8fef7-109">작은 endian 인코딩의 퀀텀 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="8fef7-109">A quantum register in the little-endian encoding.</span></span>



## <a name="output--int"></a><span data-ttu-id="8fef7-110">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8fef7-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8fef7-111">측정 된 값을 포함 하는 부호 없는 정수입니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="8fef7-111">An unsigned integer that contains the measured value of `target`.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fef7-112">설명</span><span class="sxs-lookup"><span data-stu-id="8fef7-112">Remarks</span></span>

<span data-ttu-id="8fef7-113">이 작업을 수행 하면 해당 입력 레지스터가 $ \ket{00\cdots 0} $ 상태로 다시 설정 되며 대상 컴퓨터에 다시 배포 하는 데 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fef7-113">This operation resets its input register to the $\ket{00\cdots 0}$ state, suitable for releasing back to a target machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="8fef7-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8fef7-114">See Also</span></span>

- [<span data-ttu-id="8fef7-115">MeasureIntegerBE입니다.</span><span class="sxs-lookup"><span data-stu-id="8fef7-115">Microsoft.Quantum.Canon.MeasureIntegerBE</span></span>](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)