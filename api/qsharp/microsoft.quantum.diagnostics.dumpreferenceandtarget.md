---
uid: Microsoft.Quantum.Diagnostics.DumpReferenceAndTarget
title: DumpReferenceAndTarget 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpReferenceAndTarget
qsharp.summary: Uses DumpRegister to provide diagnostics on the state of a reference and target register. Written as separate operation to allow overriding and interpreting as separate registers, rather than as a single combined register.
ms.openlocfilehash: 7f66af8a1f6f9ab83740fbf5dcfaf55776d74eb9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853401"
---
# <a name="dumpreferenceandtarget-operation"></a>DumpReferenceAndTarget 작업

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


DumpRegister를 사용 하 여 참조 및 대상 레지스터의 상태에 대 한 진단을 제공 합니다. 결합 된 단일 레지스터가 아닌 별도의 레지스터를 재정의 하 고 해석할 수 있도록 별도의 작업으로 작성 됩니다.

```qsharp
operation DumpReferenceAndTarget (reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="reference--qubit"></a>참조:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="target--qubit"></a>target: [](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

