---
uid: Microsoft.Quantum.Arithmetic.CompareUsingRippleCarry
title: CompareUsingRippleCarry 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareUsingRippleCarry
qsharp.summary: This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.
ms.openlocfilehash: e2d6e5a663f8c4e101c7e2ab1346d10cade3f4e0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223462"
---
# <a name="compareusingripplecarry-operation"></a>CompareUsingRippleCarry 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


이 연산은 값의 XOR를 출력의 비트에 적용 하 여, 값의 레지스터가 나타내는 정수가 다른 정수 보다 큰지 테스트 합니다.

```qsharp
operation CompareUsingRippleCarry (x : Microsoft.Quantum.Arithmetic.LittleEndian, y : Microsoft.Quantum.Arithmetic.LittleEndian, output : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>설명

두 개의 정수가 지정 되 `x` 고 `y` 동일한 크기의 비트 레지스터에 저장 된 경우이 작업은 충족 되는지 확인 `x > y` 합니다. True 이면 1이 XORed 출력으로 변환 됩니다. 그렇지 않으면 0이 출력의 XORed 됩니다.
즉,이 작업은 단일 $ $ \begin{align} U\ket {x} \ k {y} \ k {z} = \ket{x}\ket{y}\ket{z\oplus (x>y)}로 나타낼 수 있습니다.
\end{align} $ $

## <a name="input"></a>입력

### <a name="x--littleendian"></a>x: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

지정 된 형식으로 저장 되는 첫 번째 숫자 `LittleEndian` 는 이상 비트 레지스터입니다.


### <a name="y--littleendian"></a>y: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

지정 된 형식에 저장 된 두 번째 숫자 `LittleEndian` 입니다.


### <a name="output--qubit"></a>출력: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

비교 결과를 저장 하 $x y $>입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>참조 항목

- 새 퀀텀 ripple-A. Cuccaro, Thomas G. Draper, Samuel, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184