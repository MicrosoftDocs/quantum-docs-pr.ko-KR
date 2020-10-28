---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns
title: SteaneCodeRecoveryFns 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryFns
qsharp.summary: Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: b1dd1c2e9a71e58bd8a86d1759a8b6af13a49614
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712139"
---
# <a name="steanecoderecoveryfns-function"></a>SteaneCodeRecoveryFns 함수

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지 [](https://nuget.org/packages/)


⟦ 7, 1, 3 ⟧ Steane 퀀텀 코드의 안정기 그룹에 결합 된 X 및 Z 부분을 위한 디코더입니다.

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a>출력: ([recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))

`RecoveryFn`증후군 측정값을 사용 하 `Result[]` 고 `Pauli[]` 검색 된 오류를 수정 하는 작업을 반환 하는 형식의 함수 튜플입니다.

## <a name="see-also"></a>참고 항목

- [SteaneCodeRecoveryX를 수정 합니다.](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [SteaneCodeRecoveryZ를 수정 합니다.](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)