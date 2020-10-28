---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: ApplyDeltaParity 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: bb01eb684ff1820be08a573c0ca6cfc12efeb889
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723980"
---
# <a name="applydeltaparity-operation"></a>ApplyDeltaParity 작업

네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .

패키지 [](https://nuget.org/packages/)


이전 PQRS 간 패리티 차이를 계산 합니다. 용어 및 다음 PQRS 부채. 이 차이는 보조 비트에서 계산 됩니다.

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="prevfermionicterm--int"></a>prevFermionicTerm: [Int](xref:microsoft.quantum.lang-ref.int)[]

이전 PQRS에 대 한 인덱스 목록 ... 표현을.


### <a name="nextfermionicterm--int"></a>nextFermionicTerm: [Int](xref:microsoft.quantum.lang-ref.int)[]

다음 PQRS에 대 한 인덱스 목록 ... 표현을.


### <a name="aux--qubit"></a>aux: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

패리티 계산 결과가 저장 되는 보조 비트입니다.


### <a name="qubits--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

모든 PQRS에서 처리 되는 고 비트 표현을.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

여기서는 P < Q < R < S 인덱스를 < 하는 것으로 가정 합니다. prevPQ 및 nextPQ 모두에 대해입니다.