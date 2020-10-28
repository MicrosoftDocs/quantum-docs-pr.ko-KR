---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: MeasureStabilizerGenerators 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: a3f48ff24a39d13a57f7a144e21d4e41bb8a8b49
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712265"
---
# <a name="measurestabilizergenerators-operation"></a>MeasureStabilizerGenerators 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지 [](https://nuget.org/packages/)


안정기 그룹의 지정 된 생성기 집합을 측정 합니다.

```qsharp
operation MeasureStabilizerGenerators (stabilizerGroup : Pauli[][], logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister, gadget : ((Pauli[], Qubit[]) => Result)) : Microsoft.Quantum.ErrorCorrection.Syndrome
```


## <a name="input"></a>입력

### <a name="stabilizergroup--pauli"></a>stabilizerGroup: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Multiqubit Pauli 연산자의 배열입니다.
예를 들어 `stabilizerGroup[0]` 는 안정기 생성기 인 텐서 곱 인 단일 수준 비트 Pauli 행렬의 목록입니다.


### <a name="logicalregister--logicalregister"></a>logicalRegister: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

안정기 코드가 정의 된 요소의 배열입니다.


### <a name="gadget--pauliqubit--__invalidresult__"></a>가젯: ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[[], [](xref:microsoft.quantum.lang-ref.qubit)]) => __잘못 되었습니다 <Result>__ . 

Multiqubit Pauli 연산자를 측정 하는 방법을 지정 하는 작업입니다.



## <a name="output--syndrome"></a>출력: [증후군](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)

측정값의 결과입니다.

## <a name="remarks"></a>설명

이는 지정 된 생성기 집합이 통근 이나 출장 여부를 확인 하지 않습니다.
통근 이나 출장 않는 경우에는 측정값의 결과가 임의로 다를 수 있습니다.