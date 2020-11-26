---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation
title: ApplyPermutationUsingTransformation 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingTransformation
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using transformation-based synthesis.
ms.openlocfilehash: a05b433eae2612bbf5c87522c4ef251976184aa8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192063"
---
# <a name="applypermutationusingtransformation-operation"></a>ApplyPermutationUsingTransformation 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


변형 기반 합성을 사용 하 여 순열 Permutes 퀀텀 상태에서 amplitudes를 지정 합니다.

```qsharp
operation ApplyPermutationUsingTransformation (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Description

이 절차에서는 단방향 변환 기반 합성 방식을 구현 합니다.  입력은 $2 ^ n $ elements $ \{ 0, \pi, 2 ^ n-1 $을 통한 순열 $ \pi $ \} 로, $n $-변수가 해독 가능한 부울 함수를 나타냅니다.
알고리즘은 다음 단계를 반복적으로 수행 합니다.

1. $X \ne \ pi (x) = y $와 같은 가장 작은 $x $를 찾습니다.
2. 출력에 적용 되는 여러 제어 된 Toffoli 작업을 찾습니다. $ \pi (x) = x $를 사용 하 고 모든 $x ' < x $에 대해 $ \pi (x ') $를 변경 하지 않습니다.

## <a name="input"></a>입력

### <a name="perm--int"></a>perm: [Int](xref:microsoft.quantum.lang-ref.int)[]

0부터 시작 하는 $2 ^ n $ 요소의 순열입니다.


### <a name="qubits--littleendian"></a>작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

순열이 적용 되는 $ 이상 비트 $n 목록입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>참조 항목

- [*D. Michael*, *Dmitri Maslov*, *Gerhard Dueck* 318-323 2003,,,, 2003](https://doi.org/10.1145/775832.775915)
- [*Mathias Soeken*, *Gerhard, Dueck*, *dmichael*, Proc .rc 2016, Springer, pp. 307-321, 2016](https://doi.org/10.1007/978-3-319-40578-0_22)

## <a name="see-also"></a>참고 항목

- [ApplyPermutationUsingDecomposition.](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)