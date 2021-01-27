---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: TargetStateReflectionOracle 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: 4169ccf3e210e27f779311553b845ea04f2c7dc6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843901"
---
# <a name="targetstatereflectionoracle-function"></a><span data-ttu-id="41b4d-102">TargetStateReflectionOracle 함수</span><span class="sxs-lookup"><span data-stu-id="41b4d-102">TargetStateReflectionOracle function</span></span>

<span data-ttu-id="41b4d-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="41b4d-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="41b4d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="41b4d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="41b4d-105">플래그에 `ReflectionOracle` 따라 고유 하 게 표시 되는 대상 상태에 대 한를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="41b4d-105">Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.</span></span>

<span data-ttu-id="41b4d-106">대상 상태에는 1로 설정 된 단일 비트와 다른 모든 0: $ \ket {1} _f $가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41b4d-106">The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.</span></span>

```qsharp
function TargetStateReflectionOracle (idxFlagQubit : Int) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="input"></a><span data-ttu-id="41b4d-107">입력</span><span class="sxs-lookup"><span data-stu-id="41b4d-107">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="41b4d-108">Idx플래그 [](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="41b4d-108">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="41b4d-109">Oracle의 플래그를 지정 하는 $f의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="41b4d-109">Index to flag qubit $f$ of oracle.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="41b4d-110">출력: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="41b4d-110">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="41b4d-111">`ReflectionOracle`$ \Ket _f $로 표시 된 상태에 대해 반영 하는입니다 {1} .</span><span class="sxs-lookup"><span data-stu-id="41b4d-111">A `ReflectionOracle` that reflects about the state marked by $\ket{1}_f$.</span></span>

## <a name="see-also"></a><span data-ttu-id="41b4d-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="41b4d-112">See Also</span></span>

- [<span data-ttu-id="41b4d-113">ReflectionOracle입니다.</span><span class="sxs-lookup"><span data-stu-id="41b4d-113">Microsoft.Quantum.Canon.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Canon.ReflectionOracle)