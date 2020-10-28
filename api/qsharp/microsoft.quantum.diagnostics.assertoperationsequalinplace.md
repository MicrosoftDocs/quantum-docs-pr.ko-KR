---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace
title: AssertOperationsEqualInPlace 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).

  This assertion uses $n$ qubits and requires multiple calls of the operations being compared.
ms.openlocfilehash: 407a139da816281346eb06849f81e91b83202653
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712972"
---
# <a name="assertoperationsequalinplace-operation"></a>AssertOperationsEqualInPlace 작업

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지 [](https://nuget.org/packages/)


두 작업이 지정 된 경우는 모든 입력 상태에 대해 동일 하 게 작동 한다는 것을 어설션 합니다.

이 어설션은 \ket $V의 모든 상태에 대 한 작업의 동작을 확인 하 여 구현 됩니다 .이 경우에는 _0\otime ... \otimes V_ {n-1} $로 설정 합니다. 여기서 $V _k $은 $ {0} $, $ \ket {1} $, $ \ket{+} $ 및 $ \ket{i} $ (+ 1 Eigenstate)의 상태입니다.

이 어설션은 $ opbits $n를 사용 하 고 비교 되는 작업을 여러 번 호출 해야 합니다.

```qsharp
operation AssertOperationsEqualInPlace (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>입력

### <a name="nqubits--int"></a>N Bits: [Int](xref:microsoft.quantum.lang-ref.int)

작업이 수행 하 고 작동 하는 $n $의 수입니다 `givenU` `expectedU` .


### <a name="givenu--qubit--unit"></a>givenU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) 

검사 될 $ 이상 비트 $n에 대 한 작업입니다.


### <a name="expectedu--qubit--unit-adj"></a>Adj Unit [()](xref:microsoft.quantum.lang-ref.qubit)=> [Unit](xref:microsoft.quantum.lang-ref.unit)

비교할 $로 비트 $n에 대 한 참조 연산 `givenU` 입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>참조

$ \Ket {0} $, $ \ket {1} $, $ \ket{+} $ 및 $ \ket{i} $ 상태의 기준은 [ *Chuang,*](https://arxiv.org/abs/quant-ph/9610001)Nielsen에 설명 된 Chuang-Nielsen 기준입니다.

## <a name="see-also"></a>참고 항목

- [AssertOperationsEqualReferenced.](xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced)