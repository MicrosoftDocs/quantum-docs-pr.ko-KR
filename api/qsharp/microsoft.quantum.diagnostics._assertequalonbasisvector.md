---
uid: Microsoft.Quantum.Diagnostics._assertEqualOnBasisVector
title: _assertEqualOnBasisVector 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _assertEqualOnBasisVector
qsharp.summary: Checks if the result of applying two operations `givenU` and `expectedU` to a basis state is the same. The basis state is described by `basis` parameter. See <xref:microsoft.quantum.extensions.fliptobasis> function for more details on this description.
ms.openlocfilehash: 01b6d5aede102e47df86ea70d071d81eba1ade6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713154"
---
# <a name="_assertequalonbasisvector-operation"></a>_assertEqualOnBasisVector 작업

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지 [](https://nuget.org/packages/)


두 작업과 `givenU` 기반 상태를 적용 한 결과가 동일한 지 확인 합니다 `expectedU` . 기본 상태는 매개 변수를 통해 설명 됩니다 `basis` .
<xref:microsoft.quantum.extensions.fliptobasis>이 설명에 대 한 자세한 내용은 함수를 참조 하세요.

```qsharp
operation _assertEqualOnBasisVector (basis : Int[], givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>입력

### <a name="basis--int"></a>기본: [Int](xref:microsoft.quantum.lang-ref.int)[]

각 $n $ 이상 비트에 대해 단일가 지정 하는 기준 상태 (0 <= id <= 3)입니다.


### <a name="givenu--qubit--unit"></a>givenU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) 

검사 될 $ 이상 비트 $n에 대 한 작업입니다.


### <a name="expectedu--qubit--unit-adj"></a>Adj Unit [()](xref:microsoft.quantum.lang-ref.qubit)=> [Unit](xref:microsoft.quantum.lang-ref.unit)

GivenU $n에 대 한 참조 작업을 비교 합니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

