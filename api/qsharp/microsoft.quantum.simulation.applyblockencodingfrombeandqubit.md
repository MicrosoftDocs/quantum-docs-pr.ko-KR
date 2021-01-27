---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingFromBEandQubit
title: ApplyBlockEncodingFromBEandQubit 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingFromBEandQubit
qsharp.summary: Conversion of ((LittleEndian, Qubit[]) => () is Adj + Ctl) to BlockEncoding
ms.openlocfilehash: 616ca9a78918199057e203a825cdcde7aeb75de2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852807"
---
# <a name="applyblockencodingfrombeandqubit-operation"></a>ApplyBlockEncodingFromBEandQubit 작업

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


((LittleEndian, Adj []) => ()를 BlockEncoding으로 변환 ()

```qsharp
operation ApplyBlockEncodingFromBEandQubit (op : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl), auxiliary : Qubit[], system : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="op--littleendianqubit--unit--is-adj--ctl"></a>op: ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Adj](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is + Ctl




### <a name="auxiliary--qubit"></a>보조: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="system--qubit"></a>시스템: [](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

