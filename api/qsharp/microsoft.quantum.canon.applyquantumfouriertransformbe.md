---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE
title: ApplyQuantumFourierTransformBE 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransformBE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: d15310298dc138bdffb612895bbf20ca1371db6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717788"
---
# <a name="applyquantumfouriertransformbe-operation"></a><span data-ttu-id="037a8-102">ApplyQuantumFourierTransformBE 작업</span><span class="sxs-lookup"><span data-stu-id="037a8-102">ApplyQuantumFourierTransformBE operation</span></span>

<span data-ttu-id="037a8-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="037a8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="037a8-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="037a8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="037a8-105">빅 endian 표현의 정수를 포함 하는 퀀텀 레지스터에서 퀀텀 푸리에 변환을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="037a8-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransformBE (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="037a8-106">입력</span><span class="sxs-lookup"><span data-stu-id="037a8-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="037a8-107">qs:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="037a8-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="037a8-108">퀀텀 푸리에 변환이 적용 되는 퀀텀 레지스터</span><span class="sxs-lookup"><span data-stu-id="037a8-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="037a8-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="037a8-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="037a8-110">설명</span><span class="sxs-lookup"><span data-stu-id="037a8-110">Remarks</span></span>

<span data-ttu-id="037a8-111">입력 및 출력은 big endian 인코딩에 있는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="037a8-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="037a8-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="037a8-112">See Also</span></span>

- [<span data-ttu-id="037a8-113">ApproximateQFT입니다.</span><span class="sxs-lookup"><span data-stu-id="037a8-113">Microsoft.Quantum.Canon.ApproximateQFT</span></span>](xref:Microsoft.Quantum.Canon.ApproximateQFT)
- [<span data-ttu-id="037a8-114">QFTLE입니다.</span><span class="sxs-lookup"><span data-stu-id="037a8-114">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)