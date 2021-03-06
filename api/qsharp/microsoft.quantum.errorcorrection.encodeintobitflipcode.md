---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode
title: EncodeIntoBitFlipCode 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoBitFlipCode
qsharp.summary: Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: 44034a864c946a7d3dbb21bad5ee500660709f1a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826671"
---
# <a name="encodeintobitflipcode-operation"></a>EncodeIntoBitFlipCode 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


[3, 1, 3]/⟦ 3, 1, 1 ⟧ 비트 대칭 코드를 인코딩합니다.

```qsharp
operation EncodeIntoBitFlipCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>입력

### <a name="physregister--qubit"></a>physRegister: [](xref:microsoft.quantum.lang-ref.qubit)[]

보호할 데이터를 나타내는 실제 및 비트의 레지스터입니다.


### <a name="auxqubits--qubit"></a>auxQubits: [](xref:microsoft.quantum.lang-ref.qubit)[]

{00}보호할 데이터를 인코딩하는 데 사용 되는 처음에 $ \ket $ 상태에 있는 보조 비트의 레지스터입니다.



## <a name="output--logicalregister"></a>출력: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

인코딩에 사용 되는 실제 및 보조 비트 (논리적 레지스터로 나타냄)입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft 양자를 수정 합니다. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)