---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: EncodeIntoFiveQubitCode 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: c9df4c5c98a78cae8b3af4597020d35469454153
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712398"
---
# <a name="encodeintofivequbitcode-operation"></a>EncodeIntoFiveQubitCode 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지 [](https://nuget.org/packages/)


⟦ 5, 1, 3 ⟧ 퀀텀 코드로 인코딩합니다.

```qsharp
operation EncodeIntoFiveQubitCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>입력

### <a name="physregister--qubit"></a>physRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

인코딩되지 않은 상태를 나타내는의 비트입니다. 이 배열의 `Qubit[]` 길이는 1입니다.


### <a name="auxqubits--qubit"></a>auxQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

인코딩된 상태를 나타내는 데 사용 되는 보조 비트의 레지스터입니다.



## <a name="output--logicalregister"></a>출력: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

`LogicalRegister`인코딩된 상태를 저장 하는 형식의 실제 요소의 배열입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft 양자를 수정 합니다. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)