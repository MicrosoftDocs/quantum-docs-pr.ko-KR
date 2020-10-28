---
uid: Microsoft.Quantum.Preparation.PrepareChoiStateA
title: PrepareChoiStateA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiStateA
qsharp.summary: Prepares the Choi–Jamiłkowski state for a given operation with an adjoint variant onto given reference and target registers.
ms.openlocfilehash: c679f9a02aa15f9a582257770b8dc57d798d1b29
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710984"
---
# <a name="preparechoistatea-operation"></a>PrepareChoiStateA 작업

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지 [](https://nuget.org/packages/)


지정 된 참조 및 대상 레지스터에 대해 adjoint variant를 사용 하 여 지정 된 작업에 대 한 Choi – Jamiłkowski 상태를 준비 합니다.

```qsharp
operation PrepareChoiStateA (op : (Qubit[] => Unit is Adj), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="op--qubit--unit-adj"></a>op: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)




### <a name="reference--qubit"></a>참조:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="target--qubit"></a>target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [PrepareChoiState.](xref:Microsoft.Quantum.Preparation.PrepareChoiState)