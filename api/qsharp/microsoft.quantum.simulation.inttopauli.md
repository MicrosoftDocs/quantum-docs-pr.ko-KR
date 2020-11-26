---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: IntToPauli 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: 18edb600f7b5b33c7ad98e78e32903c570082225
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229208"
---
# <a name="inttopauli-function"></a>IntToPauli 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


정수를 단일 값 비트 Pauli 연산자로 변환 합니다.

```qsharp
function IntToPauli (idx : Int) : Pauli
```


## <a name="input"></a>입력

### <a name="idx--int"></a>idx: [Int](xref:microsoft.quantum.lang-ref.int)

`0..3`Pauli 연산자로 변환할 범위의 정수입니다.



## <a name="output--pauli"></a>출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

`Pauli`에서 제공 하는 연산자 `[PauliI, PauliX, PauliY, PauliZ][idx]` 입니다.