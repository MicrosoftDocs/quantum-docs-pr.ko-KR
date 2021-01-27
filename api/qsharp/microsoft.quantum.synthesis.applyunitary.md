---
uid: Microsoft.Quantum.Synthesis.ApplyUnitary
title: ApplyUnitary 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyUnitary
qsharp.summary: >-
  Applies gate defined by 2^n x 2^n unitary matrix.

  Fails if matrix is not unitary, or has wrong size.
ms.openlocfilehash: 58215d3b05b8c6974e979d21a13869f27b436310
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859218"
---
# <a name="applyunitary-operation"></a>ApplyUnitary 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


2 ^ n x 2 ^ n 단일 행렬로 정의 된 게이트를 적용 합니다.

Matrix가 단일 요소가 아니거나 크기가 잘못 된 경우 실패 합니다.

```qsharp
operation ApplyUnitary (unitary : Microsoft.Quantum.Math.Complex[][], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="unitary--complex"></a>단일: [복합](xref:Microsoft.Quantum.Math.Complex)[] []

2 ^ n x 2 ^ n 단일 행렬 작업을 설명 합니다.
Matrix가 단일 크기가 아니거나 적절 한 크기가 아닌 경우는 예외를 throw 합니다.


### <a name="qubits--littleendian"></a>작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

작업 (길이 n의 레지스터)을 적용 하는 이상 비트입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

