---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: SyndromeMeasOp 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 1314e16d26c7310bab21caa91cb398d4b6f09b29
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712118"
---
# <a name="syndromemeasop-user-defined-type"></a>SyndromeMeasOp 사용자 정의 형식

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지 [](https://nuget.org/packages/)


오류 수정 코드 블록의 증후군을 측정 하는 데 사용 되는 작업을 나타냅니다.

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="remarks"></a>설명

시그니처는 `(LogicalRegister => Syndrome)` 의 이상 값에 대해 공동으로 작동 하는 작업을 나타내며 일부 보조의 경우에는 보조 비트를 측정 하 여 `LogicalRegister` `Syndrome` 이러한 측정의을 나타내는 값을 추출 합니다 `Result[]` .

## <a name="see-also"></a>참고 항목

- [Microsoft 양자를 수정 합니다. LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [증후군를 수정 합니다.](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)