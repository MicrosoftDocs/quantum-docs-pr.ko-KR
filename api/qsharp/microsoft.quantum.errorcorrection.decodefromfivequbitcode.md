---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromFiveQubitCode
title: DecodeFromFiveQubitCode 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromFiveQubitCode
qsharp.summary: Decodes the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 9b4580cb88f03a16e3c9c55511d0ec5968cc636f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853163"
---
# <a name="decodefromfivequbitcode-operation"></a>DecodeFromFiveQubitCode 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


⟦ 5, 1, 3 ⟧ 퀀텀 코드를 디코딩합니다.

```qsharp
operation DecodeFromFiveQubitCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a>입력

### <a name="logicalregister--logicalregister"></a>logicalRegister: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

인코딩된 5-고 비트 코드 논리 상태를 나타내는 정수 배열입니다.



## <a name="output--qubitqubit"></a>Output[: ((),](xref:microsoft.quantum.lang-ref.qubit)[[], [](xref:microsoft.quantum.lang-ref.qubit)])

첫 번째 매개 변수에서 인코딩되지 않은 상태를 나타내고 두 번째 매개 변수에서 보조 비트를 사용 하 여 길이가 1 인의 비트 배열입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft 양자 수정. FiveQubitCodeEncoder](xref:Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoder)
- [Microsoft 양자를 수정 합니다. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)