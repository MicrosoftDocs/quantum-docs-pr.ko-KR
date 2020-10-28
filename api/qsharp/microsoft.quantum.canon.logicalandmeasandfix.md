---
uid: Microsoft.Quantum.Canon.LogicalANDMeasAndFix
title: LogicalANDMeasAndFix 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: LogicalANDMeasAndFix
qsharp.summary: Computes the logical AND of multiple qubits.
ms.openlocfilehash: 86e4b9a8c6ed5f4f56db0ceefc8051d34e911c4c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715926"
---
# <a name="logicalandmeasandfix-operation"></a>LogicalANDMeasAndFix 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


여러 비트의 논리적 AND를 계산 합니다.

```qsharp
operation LogicalANDMeasAndFix (ctrlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a>입력

### <a name="ctrlregister--qubit"></a>ctrlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

다중 입력 및 게이트에 대 한 비트 입력입니다.


### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

및의 출력이에 기록 되는 데 사용할입니다. 이는 항상 $ \ket $ 상태에서 시작 하는 것으로 간주 됩니다 {0} .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

`ctrlRegister`에 정확히 $2 $ stbits가 있는 경우이는 작업과 동일 `CCNOT` 하지만 $ \ket {001} $ 및 $ \ket {101} $ 및 $ \ket $의 $-e ^ {i \ pi/2} $에 $e ^ {i \ pi/2} $의 {011} 단계가 있습니다.
또한 Adjoint는 특수 한 경우에만 원래 작업의 역함수 인 측정 및 수정 방법입니다 (참조 참조). 단 더 작은 게이트 게이트를 사용 합니다.

## <a name="references"></a>참조

- [*Craig Gidney* , 1709.06648](https://arxiv.org/abs/1709.06648)