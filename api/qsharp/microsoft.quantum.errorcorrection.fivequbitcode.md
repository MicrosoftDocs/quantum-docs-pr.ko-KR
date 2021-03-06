---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: FiveQubitCode 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 540dcf1eafa7449f386676a9a3c9562a4d4bf29c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853151"
---
# <a name="fivequbitcode-function"></a>FiveQubitCode 함수

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


내부 증후군 측정을 포함 하는 ⟦ 5, 1, 3 ⟧ 코드 인코더 및 디코더를 나타내는 QECC 값을 반환 합니다.

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a>출력: [Qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)

형식을 지정 하 여 퀀텀 오류 수정 코드의 구현을 반환 합니다 `QECC` .

## <a name="remarks"></a>설명

이 코드는 다음 두 가지 문서에 독립적으로 있습니다.

- C. H. DiVincenzo, J. A. Smolin 및 W. K입니다. Wootters, "Mixed state 되거나 얽 히 및 퀀텀 오류 수정", "Phys, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 및
- 18. Laflamme, c. Miquel, J. P. 합니다. Zurek, "완전 한 퀀텀 오류 수정 코드", "Phys. Lett. 77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019