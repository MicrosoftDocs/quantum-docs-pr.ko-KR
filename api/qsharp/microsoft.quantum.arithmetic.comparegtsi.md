---
uid: Microsoft.Quantum.Arithmetic.CompareGTSI
title: CompareGTSI 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGTSI
qsharp.summary: 'Wrapper for signed integer comparison: `result = xs > ys`.'
ms.openlocfilehash: a0e8ef66f1e1a62d4f6a78364135376810507534
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223496"
---
# <a name="comparegtsi-operation"></a>CompareGTSI 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)


부호 있는 정수 비교를 위한 `result = xs > ys` 래퍼입니다.

```qsharp
operation CompareGTSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="xs--signedlittleendian"></a>xs: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

첫 번째 $n $ 비트 숫자


### <a name="ys--signedlittleendian"></a>작업: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

두 번째 $n $ 비트 숫자


### <a name="result--qubit"></a>결과: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

$Xs > 되 면 대칭 이동 됩니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

