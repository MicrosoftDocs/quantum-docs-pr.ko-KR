---
uid: Microsoft.Quantum.Synthesis.FlipMasks
title: FlipMasks 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FlipMasks
qsharp.summary: For every 2-level unitary calculates "flip mask", which denotes qubits which should be inverted before and after applying corresponding 1-qubit gate. For convenience prepends result with 0.
ms.openlocfilehash: ca0ce69b3353379a42cc109cebb32efe4e364825
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859204"
---
# <a name="flipmasks-function"></a>FlipMasks 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


모든 2 단계에 대해 "대칭 마스크"가 계산 됩니다 .이는 해당 하는 1-고 비트 게이트를 적용 하기 전후에 반전 되어야 하는 비트를 나타냅니다.
편의를 위해 앞에 0을 사용 합니다.

```qsharp
function FlipMasks (decomposition : (Microsoft.Quantum.Math.Complex[][], Int, Int)[], allQubitsMask : Int) : Int[]
```


## <a name="input"></a>입력

### <a name="decomposition--complexintint"></a>분해: ([복합](xref:Microsoft.Quantum.Math.Complex)[] [],[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []




### <a name="allqubitsmask--int"></a>All Bitsmask: [Int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Output: [Int](xref:microsoft.quantum.lang-ref.int)[]

