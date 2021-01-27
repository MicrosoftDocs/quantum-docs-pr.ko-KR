---
uid: Microsoft.Quantum.Canon.ApplyToPartition
title: ApplyToPartition 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartition
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts.
ms.openlocfilehash: a0dc3453e7501816132569869e858418d5f3f4e5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850549"
---
# <a name="applytopartition-operation"></a>ApplyToPartition 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 레지스터 파티션에 작업 쌍을 두 부분으로 적용 합니다.

```qsharp
operation ApplyToPartition (op : ((Qubit[], Qubit[]) => Unit), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="op--qubitqubit--unit"></a>op: (이상[비트](xref:microsoft.quantum.lang-ref.qubit)[[], [](xref:microsoft.quantum.lang-ref.qubit)]) => [단위](xref:microsoft.quantum.lang-ref.unit) 

지정 된 파티션에 적용할 작업 쌍입니다.


### <a name="numberofqubitstofirstargument--int"></a>numberOfQubitsToFirstArgument: [Int](xref:microsoft.quantum.lang-ref.int)

파티션의 첫 번째 부분에 배치할 대상의 요소 수입니다.
나머지는 파티션의 두 번째 부분을 구성 합니다.


### <a name="target--qubit"></a>target: [](xref:microsoft.quantum.lang-ref.qubit)

지정 된 두 작업을 통해 분할 되 고 작동 하는 나머지 비트의 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [ApplyToPartitionA입니다.](xref:Microsoft.Quantum.Canon.ApplyToPartitionA)
- [ApplyToPartitionC입니다.](xref:Microsoft.Quantum.Canon.ApplyToPartitionC)
- [ApplyToPartitionCA입니다.](xref:Microsoft.Quantum.Canon.ApplyToPartitionCA)