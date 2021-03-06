---
uid: Microsoft.Quantum.Arithmetic.SquareI
title: SquareI 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareI
qsharp.summary: Computes the square of the integer `xs` into `result`, which must be zero initially.
ms.openlocfilehash: 6813c8144b0ac98bae404b5e9b97e08b06c6bb3a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846308"
---
# <a name="squarei-operation"></a>SquareI 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)


에서 정수의 제곱을 계산 하 `xs` 여 `result` 처음에 0 이어야 합니다.

```qsharp
operation SquareI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="xs--littleendian"></a>xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $ bit number to square (LittleEndian)


### <a name="result--littleendian"></a>결과: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$2n $-bit result (LittleEndian)는 $ \ket $ 상태 여야 합니다 {0} .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

표준 시프트 및 추가 방법을 사용 하 여 사각형을 계산 합니다. 일반 승수를 적용 하기 전에 먼저 xs를 복사 하 고 복사 작업을 실행 취소 하는 단순 전방 솔루션과 비교 하 여 $n-$1의 비트를 저장 합니다.