---
uid: Microsoft.Quantum.Arithmetic.AssertPhaseLessThan
title: AssertPhaseLessThan 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertPhaseLessThan
qsharp.summary: Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.
ms.openlocfilehash: 7b7a4fea8973727da4dcab6f739c6db8da835a2f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843443"
---
# <a name="assertphaselessthan-operation"></a><span data-ttu-id="b776c-102">AssertPhaseLessThan 작업</span><span class="sxs-lookup"><span data-stu-id="b776c-102">AssertPhaseLessThan operation</span></span>

<span data-ttu-id="b776c-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b776c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b776c-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b776c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b776c-105">`number`PhaseLittleEndian에서 인코딩된가 보다 작음을 어설션 합니다 `value` .</span><span class="sxs-lookup"><span data-stu-id="b776c-105">Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.</span></span>

```qsharp
operation AssertPhaseLessThan (value : Int, number : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b776c-106">입력</span><span class="sxs-lookup"><span data-stu-id="b776c-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="b776c-107">값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b776c-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b776c-108">`number` 이 보다 작아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b776c-108">`number` must be less than this.</span></span>


### <a name="number--phaselittleendian"></a><span data-ttu-id="b776c-109">number: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b776c-109">number : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="b776c-110">와 비교 되는 부호 없는 정수 `value` 입니다.</span><span class="sxs-lookup"><span data-stu-id="b776c-110">Unsigned integer which is compared to `value`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b776c-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b776c-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b776c-112">설명</span><span class="sxs-lookup"><span data-stu-id="b776c-112">Remarks</span></span>

<span data-ttu-id="b776c-113">이 작업의 제어 된 버전은 컨트롤을 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b776c-113">The controlled version of this operation ignores controls.</span></span>