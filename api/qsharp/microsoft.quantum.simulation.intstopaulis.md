---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: IntsToPaulis 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 605257aa7ca39e457127e3c3459b5891145b1863
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709451"
---
# <a name="intstopaulis-function"></a>IntsToPaulis 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지 [](https://nuget.org/packages/)


정수 배열을 단일가 나 비트 Pauli 연산자의 배열로 변환 합니다.

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a>입력

### <a name="ints--int"></a>정수: [Int](xref:microsoft.quantum.lang-ref.int)[]

`0..3`Pauli 연산자로 변환할 범위의 정수 배열입니다.



## <a name="output--pauli"></a>출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

`paulis`Pauli 연산자의 배열에는에 `Pauli[]` 지정 된 `ints` 의 요소와 동일한 길이가 `paulis[idxPauli]` `[PauliI, PauliX, PauliY, PauliZ]` `ints[idxPauli]` 있습니다.