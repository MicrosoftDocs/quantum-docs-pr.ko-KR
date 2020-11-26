---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX
title: SteaneCodeRecoveryX 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryX
qsharp.summary: Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 5fac832ef5b7d7be2d85675a32f45e66312f66c8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200373"
---
# <a name="steanecoderecoveryx-function"></a>SteaneCodeRecoveryX 함수

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


⟦ 7, 1, 3 ⟧ Steane 퀀텀 코드의 안정기 그룹에 있는 X 부분에 대 한 디코더입니다.

```qsharp
function SteaneCodeRecoveryX (syndrome : Microsoft.Quantum.ErrorCorrection.Syndrome) : Pauli[]
```


## <a name="input"></a>입력

### <a name="syndrome--syndrome"></a>증후군: [증후군](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)

안정기의 X 부분을 측정 하 여 가져온 증후군 배열입니다.



## <a name="output--pauli"></a>출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

인코딩된 퀀텀 시스템에 적용 될 때에 해당 하는 오류를 수정 하는 Pauli 작업의 배열입니다 `syndrome` .

## <a name="remarks"></a>설명

선택한 디코더는 ⟦ 7, 1, 3 ⟧ Steane 코드의 CSS 코드 속성을 사용 합니다. 즉, X 오류 및 Z 오류를 별도로 수정 합니다. 코드의 속성은 각각 정수로 간주 되는 경우 z 증후군 각각 x의 3 비트 인코딩입니다 (각각 z)을 적용 해야 합니다.

## <a name="references"></a>참조 항목

- D. Gottesman, "안정기 코드 및 퀀텀 오류 수정", "Ph.D Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052

## <a name="see-also"></a>참고 항목

- [SteaneCodeRecoveryX를 수정 합니다.](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [SteaneCodeRecoveryFns를 수정 합니다.](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns)