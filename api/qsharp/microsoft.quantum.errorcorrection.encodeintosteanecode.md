---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoSteaneCode
title: EncodeIntoSteaneCode 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoSteaneCode
qsharp.summary: An encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 2f65423a17dafadd1f9f10a07335150dfc8bf886
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826201"
---
# <a name="encodeintosteanecode-operation"></a>EncodeIntoSteaneCode 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


⟦ 7, 1, 3 ⟧ Steane 퀀텀 코드 아래의 인코딩된 퀀텀 레지스터에 인코딩되지 않은 퀀텀 레지스터를 매핑하는 인코딩 작업입니다.

```qsharp
operation EncodeIntoSteaneCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>입력

### <a name="physregister--qubit"></a>physRegister: [](xref:microsoft.quantum.lang-ref.qubit)[]

인코딩되지 않은 퀀텀 상태를 포함 하는 ubit 레지스터


### <a name="auxqubits--qubit"></a>auxQubits: [](xref:microsoft.quantum.lang-ref.qubit)[]

처음에는 0이 고, 인코딩 작업을 수행할 수 있도록 퀀텀 시스템에 추가 되는 추가 비트 레지스터입니다.



## <a name="output--logicalregister"></a>출력: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Steane 인코더가 적용 된 후 상태를 포함 하는 퀀텀 레지스터

## <a name="see-also"></a>참고 항목

- [Microsoft 양자를 수정 합니다. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [SteaneCodeDecoder를 수정 합니다.](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)