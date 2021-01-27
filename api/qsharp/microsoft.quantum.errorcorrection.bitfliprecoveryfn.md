---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipRecoveryFn
title: BitFlipRecoveryFn 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipRecoveryFn
qsharp.summary: Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.
ms.openlocfilehash: 1cf2bd944b4dcaadeeca96fa0f576250590962e0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827589"
---
# <a name="bitfliprecoveryfn-function"></a>BitFlipRecoveryFn 함수

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


⟦ 3, 1, 1 ⟧ 비트 대칭 코드에 대 한 테이블 조회에 지정 된 증후군 측정에 대 한 복구 Pauli 작업에 대 한 함수입니다.

```qsharp
function BitFlipRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a>출력: [Recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

`RecoveryFn`증후군 측정값을 사용 하 `Result[]` 고 `Pauli[]` 검색 된 오류를 수정 하는 작업을 반환 하는 형식의 함수입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft 양자를 수정 합니다. RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)