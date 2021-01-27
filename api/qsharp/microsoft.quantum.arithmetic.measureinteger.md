---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: MeasureInteger 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: 288aee24e0ae6425db35312b560630a6bb9bfc80
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843117"
---
# <a name="measureinteger-operation"></a><span data-ttu-id="b4ccf-102">MeasureInteger 작업</span><span class="sxs-lookup"><span data-stu-id="b4ccf-102">MeasureInteger operation</span></span>

<span data-ttu-id="b4ccf-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b4ccf-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b4ccf-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b4ccf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b4ccf-105">퀀텀 레지스터의 콘텐츠를 측정 하 고 정수로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ccf-105">Measures the content of a quantum register and converts it to an integer.</span></span> <span data-ttu-id="b4ccf-106">측정은 표준 계산 기준, 즉의 eigenbasis을 기준으로 수행 `PauliZ` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4ccf-106">The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.</span></span>

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a><span data-ttu-id="b4ccf-107">입력</span><span class="sxs-lookup"><span data-stu-id="b4ccf-107">Input</span></span>

### <a name="target--littleendian"></a><span data-ttu-id="b4ccf-108">대상: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b4ccf-108">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b4ccf-109">작은 endian 인코딩의 퀀텀 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ccf-109">A quantum register in the little-endian encoding.</span></span>



## <a name="output--int"></a><span data-ttu-id="b4ccf-110">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b4ccf-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b4ccf-111">측정 된 값을 포함 하는 부호 없는 정수입니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="b4ccf-111">An unsigned integer that contains the measured value of `target`.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4ccf-112">설명</span><span class="sxs-lookup"><span data-stu-id="b4ccf-112">Remarks</span></span>

<span data-ttu-id="b4ccf-113">이 작업을 수행 하면 해당 입력 레지스터가 $ \ket{00\cdots 0} $ 상태로 다시 설정 되며 대상 컴퓨터에 다시 배포 하는 데 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ccf-113">This operation resets its input register to the $\ket{00\cdots 0}$ state, suitable for releasing back to a target machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4ccf-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b4ccf-114">See Also</span></span>

- [<span data-ttu-id="b4ccf-115">MeasureIntegerBE입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ccf-115">Microsoft.Quantum.Canon.MeasureIntegerBE</span></span>](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)