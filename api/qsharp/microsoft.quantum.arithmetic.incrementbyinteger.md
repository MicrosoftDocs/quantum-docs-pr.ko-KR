---
uid: Microsoft.Quantum.Arithmetic.IncrementByInteger
title: IncrementByInteger 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: fa5e75e91206aa5f33233c8a54d6e9e7ac2950e3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222969"
---
# <a name="incrementbyinteger-operation"></a>IncrementByInteger 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


단계 회전을 사용 하 여, 부호 없는 퀀텀 레지스터를 고전 정수로 늘립니다.

```qsharp
operation IncrementByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Description

가 `target` $x 부호 없는 정수를 작은 endian 인코딩으로 인코딩하고 $a $와 같은 경우를 가정 `increment` 합니다.
그런 다음이 작업을 수행 하면 단일 $ \ket{x} \maps\ket{x + a} $이 구현 됩니다. 여기서 더하기는 모듈로 $2 ^ n $, 여기서 $n = \texttt{Length (target!)}입니다. $.

## <a name="input"></a>입력

### <a name="increment--int"></a>증가값: [Int](xref:microsoft.quantum.lang-ref.int)

가 증가 하는 정수 `target` 입니다.


### <a name="target--littleendian"></a>대상: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

퀀텀 레지스터는 작은 endian 인코딩을 사용 하 여 부호 없는 정수를 인코딩합니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

