---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromSteaneCode
title: DecodeFromSteaneCode 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromSteaneCode
qsharp.summary: An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 50fc6fb22e8b65ce10aba41e18362ad96236a907
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201141"
---
# <a name="decodefromsteanecode-operation"></a>DecodeFromSteaneCode 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


⟦ 7, 1, 3 ⟧ Steane 퀀텀 코드 아래의 인코딩된 퀀텀 레지스터에 인코딩되지 않은 퀀텀 레지스터를 매핑하는 역 인코딩 작업입니다.

```qsharp
operation DecodeFromSteaneCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a>입력

### <a name="logicalregister--logicalregister"></a>logicalRegister: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

인코딩된 5-고 비트 코드 논리 상태를 나타내는 정수 배열입니다.



## <a name="output--qubitqubit"></a>Output[: ((),](xref:microsoft.quantum.lang-ref.qubit)[[], [](xref:microsoft.quantum.lang-ref.qubit)])

첫 번째 매개 변수에서 인코딩되지 않은 상태를 나타내고 두 번째 매개 변수에서 보조 비트를 사용 하 여 길이가 1 인의 비트 배열입니다.

## <a name="remarks"></a>설명

선택한 디코더는 ⟦ 7, 1, 3 ⟧ Steane 코드의 CSS 코드 속성을 사용 합니다. 즉, X 오류 및 Z 오류를 별도로 수정 합니다. 코드의 속성은 각각 정수로 간주 되는 경우 z 증후군 각각 x의 3 비트 인코딩입니다 (각각 z)을 적용 해야 합니다.

## <a name="references"></a>참조

- D. Gottesman, "안정기 코드 및 퀀텀 오류 수정", "Ph.D Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052

## <a name="see-also"></a>참고 항목

- [SteaneCodeEncoder를 수정 합니다.](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder)
- [SteaneCodeDecoder를 수정 합니다.](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)
- [Microsoft 양자를 수정 합니다. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)