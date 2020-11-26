---
uid: Microsoft.Quantum.Preparation.PrepareChoiStateC
title: PrepareChoiStateC 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiStateC
qsharp.summary: Prepares the Choi–Jamiołkowski state for a given operation with a controlled variant onto given reference and target registers.
ms.openlocfilehash: 7d9e53b1dd8ec08c0d0b200cc51562ca6330b06e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210542"
---
# <a name="preparechoistatec-operation"></a>PrepareChoiStateC 작업

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 참조 및 대상 레지스터에 대해 제어 된 variant를 사용 하 여 지정 된 작업에 대 한 Choi – Jamiołkowski 상태를 준비 합니다.

```qsharp
operation PrepareChoiStateC (op : (Qubit[] => Unit is Ctl), reference : Qubit[], target : Qubit[]) : Unit is Ctl
```


## <a name="input"></a>입력

### <a name="op--qubit--unit--is-ctl"></a>op: [이상](xref:microsoft.quantum.lang-ref.qubit)[] => [단위가](xref:microsoft.quantum.lang-ref.unit)  Ctl입니다.




### <a name="reference--qubit"></a>참조:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="target--qubit"></a>target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [PrepareChoiState.](xref:Microsoft.Quantum.Preparation.PrepareChoiState)