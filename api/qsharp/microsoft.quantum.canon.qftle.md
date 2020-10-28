---
uid: Microsoft.Quantum.Canon.QFTLE
title: QFTLE 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFTLE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: f28f74d34fb4688739646da3dc12ae6734eb4ad4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715639"
---
# <a name="qftle-operation"></a><span data-ttu-id="a50a5-102">QFTLE 작업</span><span class="sxs-lookup"><span data-stu-id="a50a5-102">QFTLE operation</span></span>

<span data-ttu-id="a50a5-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a50a5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a50a5-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a50a5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a50a5-105">작은 endian 표현의 정수를 포함 하는 퀀텀 레지스터에서 퀀텀 푸리에 변환을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50a5-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation QFTLE (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="a50a5-106">입력</span><span class="sxs-lookup"><span data-stu-id="a50a5-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="a50a5-107">qs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a50a5-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a50a5-108">퀀텀 푸리에 변환이 적용 되는 퀀텀 레지스터</span><span class="sxs-lookup"><span data-stu-id="a50a5-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="a50a5-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a50a5-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a50a5-110">설명</span><span class="sxs-lookup"><span data-stu-id="a50a5-110">Remarks</span></span>

<span data-ttu-id="a50a5-111">입력 및 출력은 little endian 인코딩에 있는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a50a5-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="a50a5-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a50a5-112">See Also</span></span>

- [<span data-ttu-id="a50a5-113">Microsoft. 양자. QFT</span><span class="sxs-lookup"><span data-stu-id="a50a5-113">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)