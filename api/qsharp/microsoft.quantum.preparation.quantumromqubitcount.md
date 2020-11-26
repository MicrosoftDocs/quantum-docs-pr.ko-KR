---
uid: Microsoft.Quantum.Preparation.QuantumROMQubitCount
title: QuantumROMQubitCount 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROMQubitCount
qsharp.summary: >-
  > [!WARNING]

  > QuantumROMQubitCount has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements> instead.


  Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.
ms.openlocfilehash: 0ec1e042b9f675505f73bfcdcc6706d0bc0367df
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210406"
---
# <a name="quantumromqubitcount-function"></a>QuantumROMQubitCount 함수

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> QuantumROMQubitCount는 더 이상 사용 되지 않습니다. 대신 <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements>를 사용하십시오.

에서 반환 하는 작업에 할당 해야 하는 총 작업 수를 반환 합니다 `QuantumROM` .

```qsharp
function QuantumROMQubitCount (targetError : Double, nCoeffs : Int) : (Int, (Int, Int))
```


## <a name="input"></a>입력

### <a name="targeterror--double"></a>targetError: [Double](xref:microsoft.quantum.lang-ref.double)

$ \Epsilon $ 대상 오류입니다.


### <a name="ncoeffs--int"></a>nCoeffs: [Int](xref:microsoft.quantum.lang-ref.int)

에 지정 된 계수 수 `QuantumROM` 입니다.



## <a name="output--intintint"></a>Output[: (int,](xref:microsoft.quantum.lang-ref.int)([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)))

## <a name="first-parameter"></a>첫 번째 매개 변수

`(x,(y,z))`는 할당 된 총 수 인 튜플을,는 레지스터의 값이 고,은 `x = y + z` `y` 가비지 비트 수입니다 `LittleEndian` `z` .