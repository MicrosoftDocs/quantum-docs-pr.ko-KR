---
uid: Microsoft.Quantum.Canon.MultiplexerFromGenerator
title: MultiplexerFromGenerator 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexerFromGenerator
qsharp.summary: >-
  Returns a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: b86238debe66747ba23c3b41164813594f80b27c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852541"
---
# <a name="multiplexerfromgenerator-function"></a>MultiplexerFromGenerator 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


N-\ket{j} $로 제어 될 때 단일 $V _j $를 적용 하는 곱하기 제어 된 단일 $U 작업을 반환 합니다.

$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.

```qsharp
function MultiplexerFromGenerator (unitaryGenerator : (Int, (Int -> (Qubit[] => Unit is Adj + Ctl)))) : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a>입력

### <a name="unitarygenerator--intint---qubit--unit--is-adj--ctl"></a>unit arygenerator: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [arybit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)

첫 번째 요소가 `Int` unitaries $N $의 수이 고 두 번째 요소는 $ `(Int -> ('T => () is Adj + Ctl))` [0, N-1] $의 정수 $j $를 사용 하는 함수 이며 _j $ $V 단일 작업을 출력 합니다.



## <a name="output--littleendianqubit--unit--is-adj--ctl"></a>출력: ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Adj](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is + Ctl

에 설명 된 unitaries을 적용 하는 곱하기 제어 되는 단일 연산 $U $입니다 `unitaryGenerator` .

## <a name="see-also"></a>참고 항목

- [MultiplexOperationsFromGenerator입니다.](xref:Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator)