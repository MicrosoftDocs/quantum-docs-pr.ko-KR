---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZTermToPauliMajIdx_
title: _ZTermToPauliMajIdx_ 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: 56de7b7b425b7d7c5830c15d7119fc1d0291d061
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839095"
---
# <a name="_ztermtopaulimajidx_-function"></a>_ZTermToPauliMajIdx_ 함수

네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Z 용어를 설명 하는 GeneratorIndex을 Paulis의 ' GeneratorIndex [] ' 식으로 변환 합니다.

```qsharp
function _ZTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a>입력

### <a name="term--generatorindex"></a>용어: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` Z 용어를 나타내는입니다.



## <a name="output--optimizedbetermindex"></a>출력: [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)

' GeneratorIndex [] ' Z 용어를 Pauli 용어로 표현 합니다.