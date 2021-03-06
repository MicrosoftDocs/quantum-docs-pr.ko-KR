---
uid: Microsoft.Quantum.Arithmetic.DivideI
title: DivideI 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: DivideI
qsharp.summary: Divides two quantum integers.
ms.openlocfilehash: 73c4e394ca38b8089b2990f8a8b6a3ee50f644d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846676"
---
# <a name="dividei-operation"></a>DivideI 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)


두 퀀텀 정수를 나눕니다.

```qsharp
operation DivideI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>설명

`xs` 는 나머지를 보유 `xs - floor(xs/ys) * ys` 하 고는를 `result` 보유 `floor(xs/ys)` 합니다.

## <a name="input"></a>입력

### <a name="xs--littleendian"></a>xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $ 비트 피제수는 나머지로 바뀝니다.


### <a name="ys--littleendian"></a>작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $ 비트 제 들


### <a name="result--littleendian"></a>결과: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$ 비트 결과 $n $ \ket $ 상태 여야 하며 {0} 정수 나누기의 결과로 대체 됩니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

는 표준 시프트 및 빼기 방법을 사용 하 여 나누기를 구현 합니다.
제어 되는 버전은 빼기로 추가 컨트롤이 필요 하지 않습니다.