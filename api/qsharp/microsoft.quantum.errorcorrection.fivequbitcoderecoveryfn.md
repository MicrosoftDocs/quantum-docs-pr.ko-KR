---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeRecoveryFn
title: Fivkebitcoderec과잉 Yfn 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeRecoveryFn
qsharp.summary: Returns function that maps error syndrome measurements to the appropriate error-correcting Pauli operators by table lookup for the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 5b8afe222d197eb7d342ac45f027f2de9130b61a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712328"
---
# <a name="fivequbitcoderecoveryfn-function"></a>Fivkebitcoderec과잉 Yfn 함수

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지 [](https://nuget.org/packages/)


⟦ 5, 1, 3 ⟧ 퀀텀 코드에 대 한 테이블 조회에 따라 오류 증후군 측정값을 적절 한 오류 수정으로 매핑하는 함수를 반환 합니다.

```qsharp
function FiveQubitCodeRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a>출력: [Recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

`RecoveryFn`증후군 측정값을 사용 하 `Result[]` 고 `Pauli[]` 검색 된 오류를 수정 하는 연산자를 반환 하는 형식의 함수입니다.

## <a name="remarks"></a>설명

가중치 $1 $의 모든 오류를 반복 하 여 총 $3 \ 시간 5 = 15 $ 가능한 사소한 syndromes을 얻습니다.
Id와 함께 오류 테이블과 해당 증후군이 작성 됩니다. 5 비트 코드의 경우이 테이블은 $X \_ 1: (0, 0, 0, 1)로 지정 됩니다. X \_ 2: (1, 0, 0, 0); X \_ 3: (1, 1, 0, 0); X \_ 4: (0, 1, 1, 0); X \_ 5: (0, 0, 1, 1) $, $Z \_ 1: (1, 0, 1, 0); Z \_ 2: (0, 1, 0, 1); Z \_ 3: (0, 0, 1, 0); Z \_ 4: (1, 0, 0, 1); Z \_ 5: (0, 1, 0, 0) $ $X _i $ 및 $Z _i $ syndromes를 추가 하 여 _i $를 가져온 $Y. 테이블 조회 복구의 순서는 bitvectors를 정수로 변환 하 여 제공 됩니다 (little endian 사용).

## <a name="see-also"></a>참고 항목

- [Microsoft 양자를 수정 합니다. RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)