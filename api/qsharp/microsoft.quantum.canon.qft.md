---
uid: Microsoft.Quantum.Canon.QFT
title: QFT 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFT
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: 8f1aa8c3680a068e500503ca25afa9a49e4ef5bf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205541"
---
# <a name="qft-operation"></a><span data-ttu-id="ff7a9-102">QFT 작업</span><span class="sxs-lookup"><span data-stu-id="ff7a9-102">QFT operation</span></span>

<span data-ttu-id="ff7a9-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ff7a9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ff7a9-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ff7a9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ff7a9-105">빅 endian 표현의 정수를 포함 하는 퀀텀 레지스터에서 퀀텀 푸리에 변환을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7a9-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation QFT (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ff7a9-106">입력</span><span class="sxs-lookup"><span data-stu-id="ff7a9-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="ff7a9-107">qs:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="ff7a9-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="ff7a9-108">퀀텀 푸리에 변환이 적용 되는 퀀텀 레지스터</span><span class="sxs-lookup"><span data-stu-id="ff7a9-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="ff7a9-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ff7a9-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ff7a9-110">설명</span><span class="sxs-lookup"><span data-stu-id="ff7a9-110">Remarks</span></span>

<span data-ttu-id="ff7a9-111">입력 및 출력은 big endian 인코딩에 있는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff7a9-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff7a9-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ff7a9-112">See Also</span></span>

- [<span data-ttu-id="ff7a9-113">ApplyQuantumFourierTransformBE입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7a9-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)