---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQTermToPauliMajIdx_
title: _PQTermToPauliMajIdx_ 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: edb9302e04de2abc6dfa9da0da27504f776e721f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839299"
---
# <a name="_pqtermtopaulimajidx_-function"></a>_PQTermToPauliMajIdx_ 함수

네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


PQ 용어를 설명 하는 GeneratorIndex을 Paulis의 식 ' GeneratorIndex [] '로 변환 합니다.

```qsharp
function _PQTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a>입력

### <a name="term--generatorindex"></a>용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` PQ 용어를 나타내는입니다.



## <a name="output--optimizedbetermindex"></a>출력: [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)

PQ term을 Pauli 용어로 표현 하는 ' GeneratorIndex [] '