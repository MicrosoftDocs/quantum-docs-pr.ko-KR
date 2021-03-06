---
uid: Microsoft.Quantum.ErrorCorrection.Recover
title: 복구 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: Recover
qsharp.summary: Performs a single round of error correction by a quantum code described by a `QECC` type.
ms.openlocfilehash: 3e2ce404ae3a6b4097897b859388fea3f915232c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825516"
---
# <a name="recover-operation"></a>복구 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


형식으로 설명 되는 퀀텀 코드에의 한 오류 수정 사항을 한 번 수행 합니다 `QECC` .

```qsharp
operation Recover (code : Microsoft.Quantum.ErrorCorrection.QECC, fn : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a>입력

### <a name="code--qecc"></a>코드: [Qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)

퀀텀 오류-형식으로 패키지 된 코드를 수정 하면 `QECC` 퀀텀 데이터의 인코딩과 디코딩을 설명 하 고 오류 syndromes을 측정 하는 방법을 설명 합니다.


### <a name="fn--recoveryfn"></a>fn: [Recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

`RecoveryFn`검색 된 오류를 수정 하는 작업에 증후군 각 오류를 매핑하는입니다 `Pauli[]` .


### <a name="logicalregister--logicalregister"></a>logicalRegister: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

안정기 코드가 정의 된 요소의 배열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [Microsoft 양자 수정. QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)
- [Microsoft 양자를 수정 합니다. RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [Microsoft 양자를 수정 합니다. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)