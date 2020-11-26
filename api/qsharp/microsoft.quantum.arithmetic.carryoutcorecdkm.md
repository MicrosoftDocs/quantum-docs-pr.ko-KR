---
uid: Microsoft.Quantum.Arithmetic.CarryOutCoreCDKM
title: CarryOutCoreCDKM 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CarryOutCoreCDKM
qsharp.summary: The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM. This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.
ms.openlocfilehash: 19a692a3b54a413f25a474c361e773ab6c65579e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223547"
---
# <a name="carryoutcorecdkm-operation"></a>CarryOutCoreCDKM 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


위의 ApplyOuterCDKMAdder 작업과 함께 사용 되는 RippleCarryAdderCDKM의 핵심 작업입니다. 즉, RippleCarryAdderCDKM의 내부 작업을 가져오기 위해이 작업을 conjugated 합니다. 이 작업을 수행 하면 작업을 계산 하 여 입력의 일부에 대 한 게이트 없는 시퀀스를 적용 합니다 `ys` .

```qsharp
operation CarryOutCoreCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="xs--littleendian"></a>xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

첫 번째 비트율 비트 레지스터입니다.


### <a name="ys--littleendian"></a>작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

두 번째 비트율 비트 레지스터입니다.


### <a name="ancilla--qubit"></a>ancilla: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

이 작업에 전달 된 RippleCarryAdderCDKM에서 사용 되는 ancilla 이상 비트입니다.


### <a name="carry--qubit"></a>운반: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

RippleCarryAdderCDKM 작업에서 이상 비트를 수행 합니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>참조 항목

- Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new 퀀텀 ripple and A new, 2004.
  https://arxiv.org/abs/quant-ph/0410184v1