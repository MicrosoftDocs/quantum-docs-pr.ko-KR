---
uid: Microsoft.Quantum.Convert.PauliArrayAsInt
title: PauliArrayAsInt 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: PauliArrayAsInt
qsharp.summary: Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.
ms.openlocfilehash: 6077110cc07c8626b22eb404c1de096ed43efcc3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224244"
---
# <a name="pauliarrayasint-function"></a>PauliArrayAsInt 함수

네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


단일가 나 비트 Pauli 연산자의 배열로 표현 되는 다중 기능 비트 Pauli 연산자를 정수로 인코딩합니다.

```qsharp
function PauliArrayAsInt (paulis : Pauli[]) : Int
```


## <a name="input"></a>입력

### <a name="paulis--pauli"></a>paulis: [Paulis](xref:microsoft.quantum.lang-ref.pauli)[]

최대 31 개의 단일 수준 Pauli 연산자의 배열입니다.



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

아래에서 설명 하는 고유 하 게 식별 하는 정수 `paulis` 입니다.

## <a name="remarks"></a>설명

각 Pauli 연산자는 두 비트를 사용 하 여 인코딩할 수 있습니다. $ $ \begin{align} \boldone \maps00, \쿼드 X \maps01, \쿼드 Y \maps11, \쿼드 Z \maps10.
\end{align} $ $

Pauli 연산자의 배열이 지정 된 `[P0, ..., Pn]` 경우이 함수는 각 Pauli 연산자의 매핑을 빅 endian 순서로 연결 하 여 이진 확장이 형성 된 정수를 반환 `bits(Pn) ... bits(P0)` 합니다.