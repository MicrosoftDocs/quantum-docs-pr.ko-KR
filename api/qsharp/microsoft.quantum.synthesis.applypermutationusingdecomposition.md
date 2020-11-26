---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition
title: ApplyPermutationUsingDecomposition 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecomposition
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 5b25ef3327bbca2dfdbe8fa876f3f797dddf77e8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192131"
---
# <a name="applypermutationusingdecomposition-operation"></a>ApplyPermutationUsingDecomposition 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


분해 기반 합성을 사용 하 여 순열 Permutes 퀀텀 상태에서 amplitudes를 지정 합니다.

```qsharp
operation ApplyPermutationUsingDecomposition (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Description

이 절차에서는 분해 기반 합성 방식을 구현 합니다.  입력은 $2 ^ n $ elements $ \{ 0, \pi, 2 ^ n-1 \} $이 고 $n $-변수가 해독 가능한 부울 함수를 나타내는 순열 $ \pi $입니다.
알고리즘은 각 변수 인덱스에 대해 다음 단계를 반복적으로 수행 합니다 $i $:

1. $ ((\ Pi_l, \ pi_r), \pi ') $를 계산 하 여 $ \ pi_l $ 및 $ \ pi_r $의 이미지가 $i $ 이외의 인덱스에 있는 요소에서 비트를 변경 하지 않도록 하 고 해당 요소에서 $ \pi의 이미지를 변경 하지 않습니다.
2. $ \Pi \leftarrow \pi ' $를 설정 하 고 고정 지점이 아닌 요소에 따라 $ \ pi_l $ 및 $ \ pi_r $에서 valtables를 파생 시킵니다.

모든 변수 인덱스에 대해 이러한 단계를 적용 한 후 나머지 순열 $ \pi $는 id가 되며 수집 된 진위 테이블 및 인덱스에 따라 작업을 사용 하 여 sttable 제어 된 작업을 적용할 수 있습니다 @"microsoft.quantum.intrinsic.x" @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" .

변수 순서는 $0, \ 점, n-$1입니다.  작업에서 사용자 지정 변수 순서를 지정할 수 있습니다 @"microsoft.quantum.synthesis.applypermutationusingdecompositionwithvariableorder" .

## <a name="input"></a>입력

### <a name="perm--int"></a>perm: [Int](xref:microsoft.quantum.lang-ref.int)[]

0부터 시작 하는 $2 ^ n $ 요소의 순열입니다.


### <a name="qubits--littleendian"></a>작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

순열이 적용 되는 $ 이상 비트 $n 목록입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>참조 항목

- [*Alexis De Vos*, *Yvan Van rentergem*, 고급 (2), 2008, pp. 183--200](http://www.aimsciences.org/article/doi/10.3934/amc.2008.2.183)
- [*Mathias Soeken*, *김 Tague*, *Gerhard* Dueck, *Rolf Drechsler*, 기호화 된 계산 73 (2016), pp. 1--26의 저널](https://www.sciencedirect.com/science/article/pii/S0747717115000188?via%3Dihub)

## <a name="see-also"></a>참고 항목

- [ApplyPermutationUsingDecompositionWithVariableOrder.](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder)
- [ApplyPermutationUsingTransformation.](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)