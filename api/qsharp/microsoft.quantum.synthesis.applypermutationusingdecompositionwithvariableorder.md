---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: ApplyPermutationUsingDecompositionWithVariableOrder 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: a5ca9b366f7ff477070e21fea047ff04b425439c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203436"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a>ApplyPermutationUsingDecompositionWithVariableOrder 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


분해 기반 합성을 사용 하 여 순열 Permutes 퀀텀 상태에서 amplitudes를 지정 합니다.

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>설명

이 작업은 @"microsoft.quantum.synthesis.applypermutationusingdecomposition" 변수 순서를 지정할 수 있는 보다 일반적인 버전의입니다. 다른 변수 순서는 제어 되는 게이트에 사용 되는 분해 시퀀스와 진위 테이블을 변경 합니다 @"microsoft.quantum.intrinsic.x" .  따라서 변수 순서를 변경 하면 순열 실현에 사용 되는 전체 게이트 수가 변경 됩니다.

## <a name="input"></a>입력

### <a name="perm--int"></a>perm: [Int](xref:microsoft.quantum.lang-ref.int)[]

0부터 시작 하는 $2 ^ n $ 요소의 순열입니다.


### <a name="variableorder--int"></a>variableOrder: [Int](xref:microsoft.quantum.lang-ref.int)[]

0부터 시작 하는 $n $ 요소의 순열입니다.


### <a name="qubits--littleendian"></a>작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

순열이 적용 되는 $ 이상 비트 $n 목록입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [ApplyPermutationUsingDecomposition.](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [ApplyPermutationUsingTransformation.](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)