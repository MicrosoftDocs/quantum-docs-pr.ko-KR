---
uid: Microsoft.Quantum.Canon.ApplyToPartitionC
title: ApplyToPartitionC 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionC
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 840c93c653d71af1a82fb0dc51d9e056176ba88b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717116"
---
# <a name="applytopartitionc-operation"></a>ApplyToPartitionC 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


지정 된 레지스터 파티션에 작업 쌍을 두 부분으로 적용 합니다.
한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.

```qsharp
operation ApplyToPartitionC (op : ((Qubit[], Qubit[]) => Unit is Ctl), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="op--qubitqubit--unit-ctl"></a>op[: ((), [](xref:microsoft.quantum.lang-ref.qubit)][, [](xref:microsoft.quantum.lang-ref.qubit)]) => [단위](xref:microsoft.quantum.lang-ref.unit) Ctl

지정 된 파티션에 적용할 작업 쌍입니다.


### <a name="numberofqubitstofirstargument--int"></a>numberOfQubitsToFirstArgument: [Int](xref:microsoft.quantum.lang-ref.int)

파티션의 첫 번째 부분에 배치할 대상의 요소 수입니다.
나머지는 파티션의 두 번째 부분을 구성 합니다.


### <a name="target--qubit"></a>target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

지정 된 두 작업을 통해 분할 되 고 작동 하는 나머지 비트의 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [ApplyToPartition입니다.](xref:Microsoft.Quantum.Canon.ApplyToPartition)