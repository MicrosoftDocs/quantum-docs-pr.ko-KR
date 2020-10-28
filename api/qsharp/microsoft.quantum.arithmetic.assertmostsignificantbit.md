---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: AssertMostSignificantBit 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 408e50ed9f2e6c8ba35db20855608d2bd1f24eea
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721381"
---
# <a name="assertmostsignificantbit-operation"></a><span data-ttu-id="2bed6-102">AssertMostSignificantBit 작업</span><span class="sxs-lookup"><span data-stu-id="2bed6-102">AssertMostSignificantBit operation</span></span>

<span data-ttu-id="2bed6-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2bed6-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2bed6-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2bed6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2bed6-105">부호 없는 정수를 나타내는 고 비트 레지스터의 가장 중요 한 것이 특정 상태에 있음을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bed6-105">Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.</span></span>

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="2bed6-106">입력</span><span class="sxs-lookup"><span data-stu-id="2bed6-106">Input</span></span>

### <a name="value--__invalidresult__"></a><span data-ttu-id="2bed6-107">값: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="2bed6-107">value : __invalid<Result>__</span></span>

<span data-ttu-id="2bed6-108">어설션된 상위 비트의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2bed6-108">The value of the highest bit being asserted.</span></span>


### <a name="number--littleendian"></a><span data-ttu-id="2bed6-109">number: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2bed6-109">number : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="2bed6-110">가장 높은 비트를 확인 하는 부호 없는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="2bed6-110">Unsigned integer of which the highest bit is checked.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2bed6-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2bed6-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2bed6-112">설명</span><span class="sxs-lookup"><span data-stu-id="2bed6-112">Remarks</span></span>

<span data-ttu-id="2bed6-113">이 작업의 제어 된 버전은 컨트롤을 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bed6-113">The controlled version of this operation ignores controls.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bed6-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2bed6-114">See Also</span></span>

- [<span data-ttu-id="2bed6-115">Microsoft 양자. Assert</span><span class="sxs-lookup"><span data-stu-id="2bed6-115">Microsoft.Quantum.Intrinsic.Assert</span></span>](xref:Microsoft.Quantum.Intrinsic.Assert)