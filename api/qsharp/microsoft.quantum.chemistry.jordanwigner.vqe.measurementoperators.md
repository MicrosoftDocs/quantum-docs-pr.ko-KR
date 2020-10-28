---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.MeasurementOperators
title: MeasurementOperators 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: MeasurementOperators
qsharp.summary: Computes all the measurement operators required to compute the expectation of a Jordan-Wigner term.
ms.openlocfilehash: 24d752c4f198764b6e7c6ea6c49669c020c1a502
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713679"
---
# <a name="measurementoperators-function"></a>MeasurementOperators 함수

네임 스페이스: [JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

패키지 [](https://nuget.org/packages/)


Jordan-Wigner 용어의 예상 값을 계산 하는 데 필요한 모든 측정 연산자를 계산 합니다.

```qsharp
function MeasurementOperators (nQubits : Int, indices : Int[], termType : Int) : Pauli[][]
```


## <a name="input"></a>입력

### <a name="nqubits--int"></a>N Bits: [Int](xref:microsoft.quantum.lang-ref.int)

분자 시스템을 시뮬레이트하는 데 필요한 비트 수입니다.


### <a name="indices--int"></a>인덱스: [Int](xref:microsoft.quantum.lang-ref.int)[]

각 Pauli 연산자가 적용 되는의 인덱스를 포함 하는 배열입니다.


### <a name="termtype--int"></a>termType: [Int](xref:microsoft.quantum.lang-ref.int)

Jordan-Wigner 용어의 유형입니다.



## <a name="output--pauli"></a>출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

측정 연산자의 배열 (각각 Pauli의 배열)입니다.