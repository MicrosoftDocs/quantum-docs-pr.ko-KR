---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: TargetStateReflectionOracle 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: 65ad316a6ac986ebd0dc28b25859026a60aa3239
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191111"
---
# <a name="targetstatereflectionoracle-function"></a><span data-ttu-id="df9b7-102">TargetStateReflectionOracle 함수</span><span class="sxs-lookup"><span data-stu-id="df9b7-102">TargetStateReflectionOracle function</span></span>

<span data-ttu-id="df9b7-103">네임 스페이스: [AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="df9b7-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="df9b7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="df9b7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="df9b7-105">플래그에 `ReflectionOracle` 따라 고유 하 게 표시 되는 대상 상태에 대 한를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="df9b7-105">Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.</span></span>

<span data-ttu-id="df9b7-106">대상 상태에는 1로 설정 된 단일 비트와 다른 모든 0: $ \ket {1} _f $가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df9b7-106">The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.</span></span>

```qsharp
function TargetStateReflectionOracle (idxFlagQubit : Int) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="input"></a><span data-ttu-id="df9b7-107">입력</span><span class="sxs-lookup"><span data-stu-id="df9b7-107">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="df9b7-108">Idx플래그 [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="df9b7-108">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="df9b7-109">Oracle의 플래그를 지정 하는 $f의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="df9b7-109">Index to flag qubit $f$ of oracle.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="df9b7-110">출력: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="df9b7-110">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="df9b7-111">`ReflectionOracle`$ \Ket _f $로 표시 된 상태에 대해 반영 하는입니다 {1} .</span><span class="sxs-lookup"><span data-stu-id="df9b7-111">A `ReflectionOracle` that reflects about the state marked by $\ket{1}_f$.</span></span>

## <a name="see-also"></a><span data-ttu-id="df9b7-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="df9b7-112">See Also</span></span>

- [<span data-ttu-id="df9b7-113">ReflectionOracle입니다.</span><span class="sxs-lookup"><span data-stu-id="df9b7-113">Microsoft.Quantum.Canon.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Canon.ReflectionOracle)