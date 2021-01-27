---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns
title: SteaneCodeRecoveryFns 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryFns
qsharp.summary: Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 8dc715042f98b90b8cea7e2d6ecb5d02a78d297f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853020"
---
# <a name="steanecoderecoveryfns-function"></a>SteaneCodeRecoveryFns 함수

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


⟦ 7, 1, 3 ⟧ Steane 퀀텀 코드의 안정기 그룹에 결합 된 X 및 Z 부분을 위한 디코더입니다.

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a>출력: ([recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))

`RecoveryFn`증후군 측정값을 사용 하 `Result[]` 고 `Pauli[]` 검색 된 오류를 수정 하는 작업을 반환 하는 형식의 함수 튜플입니다.

## <a name="see-also"></a>참고 항목

- [SteaneCodeRecoveryX를 수정 합니다.](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [SteaneCodeRecoveryZ를 수정 합니다.](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)