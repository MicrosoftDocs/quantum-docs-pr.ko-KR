---
uid: Microsoft.Quantum.Preparation.MixedStatePreparation
title: MixedStatePreparation 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: MixedStatePreparation
qsharp.summary: Represents a particular mixed state that can be prepared on an index and a garbage register.
ms.openlocfilehash: 94d6483914b5d21bb51a5469c7123f834e9eb5da
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193576"
---
# <a name="mixedstatepreparation-user-defined-type"></a><span data-ttu-id="0892b-102">MixedStatePreparation 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="0892b-102">MixedStatePreparation user defined type</span></span>

<span data-ttu-id="0892b-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="0892b-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="0892b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0892b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0892b-105">인덱스 및 가비지 레지스터에 대해 준비할 수 있는 특정 혼합 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0892b-105">Represents a particular mixed state that can be prepared on an index and a garbage register.</span></span>

```qsharp

newtype MixedStatePreparation = (Requirements : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements, Norm : Double, Prepare : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="0892b-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="0892b-106">Named Items</span></span>

### <a name="requirements--mixedstatepreparationrequirements"></a><span data-ttu-id="0892b-107">요구 사항: [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span><span class="sxs-lookup"><span data-stu-id="0892b-107">Requirements : [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span></span>


### <a name="norm--double"></a><span data-ttu-id="0892b-108">일반: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0892b-108">Norm : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>


### <a name="prepare--littleendianqubitqubit--unit--is-adj--ctl"></a><span data-ttu-id="0892b-109">Prepare: ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian), Adj[[],](xref:microsoft.quantum.lang-ref.qubit)[[]](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit) is Ctl + Ctl</span><span class="sxs-lookup"><span data-stu-id="0892b-109">Prepare : ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="0892b-110">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0892b-110">See Also</span></span>

- [<span data-ttu-id="0892b-111">PurifiedMixedState</span><span class="sxs-lookup"><span data-stu-id="0892b-111">Microsoft.Quantum.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.PurifiedMixedState)