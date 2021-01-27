---
uid: Microsoft.Quantum.Arithmetic.ApplyXorInPlace
title: ApplyXorInPlace 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyXorInPlace
qsharp.summary: Applies a bitwise-XOR operation between a classical integer and an integer represented by a register of qubits.
ms.openlocfilehash: 8f338d6638d554f3ead1f3c0e7b6605c7937abd8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843469"
---
# <a name="applyxorinplace-operation"></a>ApplyXorInPlace 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


는 고전적인 정수와, 비트의 레지스터가 나타내는 정수 사이에 비트 XOR 연산을 적용 합니다.

```qsharp
operation ApplyXorInPlace (value : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>설명

`X`정수에서 1 비트를 기반으로 하는 작은 endian 레지스터에 작업을 적용 합니다.

에 의해 표시 되 `value` 고 y가에서 인코딩된 부호 없는 정수 인 `target` 경우 $ `InPlaceXorLE` \ket{y}\rightarrow \ket{y\oplus a} $로 지정 된 작업을 수행 합니다. 여기서 $ \oplus $는 배타적 비트 or 연산자입니다.

## <a name="input"></a>입력

### <a name="value--int"></a>값: [Int](xref:microsoft.quantum.lang-ref.int)

음수가 아닌 것으로 간주 되는 정수입니다.


### <a name="target--littleendian"></a>대상: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

작은 endian 인코딩으로 저장 하는 데 사용 되는 퀀텀 레지스터 `value` 입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

