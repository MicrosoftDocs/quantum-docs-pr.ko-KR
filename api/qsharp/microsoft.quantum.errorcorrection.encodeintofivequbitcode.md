---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: EncodeIntoFiveQubitCode 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 1bccf46453ad34199dcebc5bcff693359fe2254c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826314"
---
# <a name="encodeintofivequbitcode-operation"></a>EncodeIntoFiveQubitCode 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


⟦ 5, 1, 3 ⟧ 퀀텀 코드로 인코딩합니다.

```qsharp
operation EncodeIntoFiveQubitCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>입력

### <a name="physregister--qubit"></a>physRegister: [](xref:microsoft.quantum.lang-ref.qubit)[]

인코딩되지 않은 상태를 나타내는의 비트입니다. 이 배열의 `Qubit[]` 길이는 1입니다.


### <a name="auxqubits--qubit"></a>auxQubits: [](xref:microsoft.quantum.lang-ref.qubit)[]

인코딩된 상태를 나타내는 데 사용 되는 보조 비트의 레지스터입니다.



## <a name="output--logicalregister"></a>출력: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

`LogicalRegister`인코딩된 상태를 저장 하는 형식의 실제 요소의 배열입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft 양자를 수정 합니다. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)