---
uid: Microsoft.Quantum.ErrorCorrection.ApplyBitFlipEncoder
title: ApplyBitFlipEncoder 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: ApplyBitFlipEncoder
qsharp.summary: >-
  Private operation used to implement both the bit flip encoder and decoder.

  Note that this encoder can make use of in-place coherent recovery, in which case it will "cause" the error described by the initial state of `auxQubits`. In particular, if `auxQubits` are initially in the state $\ket{10}$, this will cause an $X_1$ error on the encoded qubit.
ms.openlocfilehash: e56e84effa001f104bbd5e28e7181dbd39a4cf5e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201294"
---
# <a name="applybitflipencoder-operation"></a>ApplyBitFlipEncoder 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


비트 플립 인코더와 디코더를 모두 구현 하는 데 사용 되는 개인 작업입니다.

이 인코더는 현재 위치의 일관 된 복구를 사용할 수 있으며,이 경우의 초기 상태에 설명 된 오류를 "발생" 시킵니다 `auxQubits` .
특히 `auxQubits` 이 $ \ket $ 상태에 있는 경우에는 {10} 인코딩된 비트의 $X _1 $ 오류가 발생 합니다.

```qsharp
operation ApplyBitFlipEncoder (coherentRecovery : Bool, data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a>입력

### <a name="coherentrecovery--bool"></a>coherentRecovery: [Bool](xref:microsoft.quantum.lang-ref.bool)




### <a name="data--qubit"></a>data: [bit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="scratch--qubit"></a>스크래치: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>참조

- doi: 10.1103/PhysRevA 85.044302