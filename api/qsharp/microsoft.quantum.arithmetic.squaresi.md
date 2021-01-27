---
uid: Microsoft.Quantum.Arithmetic.SquareSI
title: SquareSI 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareSI
qsharp.summary: Square signed integer `xs` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 161b45766c6f4d500d25def24aa509ee7fdc8628
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842937"
---
# <a name="squaresi-operation"></a>SquareSI 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)


부호 있는 사각형 `xs` 의 정수 이며 처음에 0 이어야 하는에 결과를 저장 합니다 `result` .

```qsharp
operation SquareSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="xs--signedlittleendian"></a>xs: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

n 비트 정수-제곱 (SignedLittleEndian)


### <a name="result--signedlittleendian"></a>결과: [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)

2n-bit result (SignedLittleEndian)는 $ \ket $ 상태 여야 합니다 {0} .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

구현은 IntegerSquare에 의존 합니다.