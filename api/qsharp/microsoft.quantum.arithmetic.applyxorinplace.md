---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: ApplyXorInPlace 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: b7fc20ac421d5cff9baa3fe05450c1564f123505
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210116"
---
# <a name="applyxorinplace-operation"></a>ApplyXorInPlace 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


는 고전적인 정수와, 비트의 레지스터가 나타내는 정수 사이에 비트 XOR 연산을 적용 합니다.

```qsharp
operation ApplyXorInPlace (value : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Description

`X`정수에서 1 비트를 기반으로 하는 작은 endian 레지스터에 작업을 적용 합니다.

에 의해 표시 되 `value` 고 y가에서 인코딩된 부호 없는 정수 인 `target` 경우 $ `InPlaceXorLE` \ket{y}\rightarrow \ket{y\oplus a} $로 지정 된 작업을 수행 합니다. 여기서 $ \oplus $는 배타적 비트 or 연산자입니다.

## <a name="input"></a>입력

### <a name="value--int"></a>값: [Int](xref:microsoft.quantum.lang-ref.int)

음수가 아닌 것으로 간주 되는 정수입니다.


### <a name="target--littleendian"></a>대상: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

작은 endian 인코딩으로 저장 하는 데 사용 되는 퀀텀 레지스터 `value` 입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

