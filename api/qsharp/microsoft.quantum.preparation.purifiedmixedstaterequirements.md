---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements
title: PurifiedMixedStateRequirements 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateRequirements
qsharp.summary: Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".
ms.openlocfilehash: 9b8861a4112c4e6c9db994339353c771a3de81a6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229990"
---
# <a name="purifiedmixedstaterequirements-function"></a><span data-ttu-id="dcbfe-102">PurifiedMixedStateRequirements 함수</span><span class="sxs-lookup"><span data-stu-id="dcbfe-102">PurifiedMixedStateRequirements function</span></span>

<span data-ttu-id="dcbfe-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="dcbfe-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="dcbfe-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dcbfe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dcbfe-105">에서 반환 하는 작업을 적용 하기 위해 할당 해야 하는 총 비트 수를 반환 합니다 @"microsoft.quantum.preparation.purifiedmixedstate" .</span><span class="sxs-lookup"><span data-stu-id="dcbfe-105">Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".</span></span>

```qsharp
function PurifiedMixedStateRequirements (targetError : Double, nCoefficients : Int) : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
```


## <a name="input"></a><span data-ttu-id="dcbfe-106">입력</span><span class="sxs-lookup"><span data-stu-id="dcbfe-106">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="dcbfe-107">targetError: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="dcbfe-107">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="dcbfe-108">$ \Epsilon $ 대상 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="dcbfe-108">The target error $\epsilon$.</span></span>


### <a name="ncoefficients--int"></a><span data-ttu-id="dcbfe-109">nCoefficients: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dcbfe-109">nCoefficients : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dcbfe-110">혼합 상태를 준비할 때 지정할 계수 수입니다.</span><span class="sxs-lookup"><span data-stu-id="dcbfe-110">The number of coefficients to be specified in preparing a mixed state.</span></span>



## <a name="output--mixedstatepreparationrequirements"></a><span data-ttu-id="dcbfe-111">출력: [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span><span class="sxs-lookup"><span data-stu-id="dcbfe-111">Output : [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span></span>

<span data-ttu-id="dcbfe-112">함수에서 사용 하는 각 인덱스 및 가비지 레지스터와 총에 필요한 수의 수에 대 한 설명입니다 @"microsoft.quantum.preparation.purifiedmixedstate" .</span><span class="sxs-lookup"><span data-stu-id="dcbfe-112">A description of how many qubits are required in total, and for each of the index and garbage registers used by the @"microsoft.quantum.preparation.purifiedmixedstate" function.</span></span>

## <a name="see-also"></a><span data-ttu-id="dcbfe-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="dcbfe-113">See Also</span></span>

- [<span data-ttu-id="dcbfe-114">PurifiedMixedState.</span><span class="sxs-lookup"><span data-stu-id="dcbfe-114">Microsoft.Quantum.Preparation.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)