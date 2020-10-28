---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromBitFlipCode
title: DecodeFromBitFlipCode 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromBitFlipCode
qsharp.summary: Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: be6ad5fce9eeb3eea031ff301b78dbb3680b66f0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712482"
---
# <a name="decodefrombitflipcode-operation"></a>DecodeFromBitFlipCode 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지 [](https://nuget.org/packages/)


[3, 1, 3]/⟦ 3, 1, 1 ⟧ 비트 대칭 코드에서 디코딩합니다.

```qsharp
operation DecodeFromBitFlipCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a>입력

### <a name="logicalregister--logicalregister"></a>logicalRegister: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

비트 대칭 코드의 코드 블록입니다.



## <a name="output--qubitqubit"></a>Output[: ((),](xref:microsoft.quantum.lang-ref.qubit)[[], [](xref:microsoft.quantum.lang-ref.qubit)])

논리적 레지스터로 인코딩된 데이터의 튜플 및 증후군를 나타내는 데 사용 되는 보조 비트입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft 양자를 수정 합니다. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [EncodeIntoBitFlipCode를 수정 합니다.](xref:Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode)