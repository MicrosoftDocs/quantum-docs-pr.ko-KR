---
uid: Microsoft.Quantum.Chemistry.JordanWigner._V0123TermToPauliGenIdx_
title: _V0123TermToPauliGenIdx_ 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _V0123TermToPauliGenIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQRS term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 8893d7c5479409a0ff98aa0b9e58f34fd3d274f7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839186"
---
# <a name="_v0123termtopauligenidx_-function"></a>_V0123TermToPauliGenIdx_ 함수

네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


PQRS 용어를 설명 하는 GeneratorIndex을 Paulis의 식 ' GeneratorIndex [] '로 변환 합니다.

```qsharp
function _V0123TermToPauliGenIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a>입력

### <a name="term--generatorindex"></a>용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` PQRS 용어를 나타내는입니다.



## <a name="output--generatorindex"></a>출력: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]

PQRS term을 Pauli 용어로 표현 하는 ' GeneratorIndex [] '