---
uid: Microsoft.Quantum.Synthesis.TruthTablesFromPermutationFolder
title: TruthTablesFromPermutationFolder 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: TruthTablesFromPermutationFolder
qsharp.summary: Decomposition logic for a single variable index
ms.openlocfilehash: 6b00c9e880ed7b7b3bf446dcb17dab3bab7a83a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724456"
---
# <a name="truthtablesfrompermutationfolder-function"></a>TruthTablesFromPermutationFolder 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지 [](https://nuget.org/packages/)


단일 변수 인덱스의 분해 논리

```qsharp
function TruthTablesFromPermutationFolder (numVars : Int, state : Microsoft.Quantum.Synthesis.DecompositionState, index : Int) : Microsoft.Quantum.Synthesis.DecompositionState
```


## <a name="description"></a>Description

현재 상태를 사용 하 여 업데이트 된 순열을 생성 하 고 제어 되는 게이트에서 새 함수를 추가할 수 있습니다.

## <a name="input"></a>입력

### <a name="numvars--int"></a>numVars: [Int](xref:microsoft.quantum.lang-ref.int)




### <a name="state--decompositionstate"></a>상태: [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)




### <a name="index--int"></a>인덱스: [Int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--decompositionstate"></a>출력: [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)

