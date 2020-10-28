---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger
title: IncrementPhaseByModularInteger 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 52309c056a3eae25ffdfbfa848f94bf744c71132
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721057"
---
# <a name="incrementphasebymodularinteger-operation"></a>IncrementPhaseByModularInteger 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지 [](https://nuget.org/packages/)


정수 상수를 기준으로 하는 이상 비트 레지스터의 모듈식 증분을 수행 합니다.

```qsharp
operation IncrementPhaseByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="description"></a>Description

`increment`$A $, `modulus` $N $ 및 $y $로 인코딩된 정수를 사용 하 여 나타냅니다 `target` .
그런 다음이 작업은 다음 변환을 수행 합니다. \begin{align} \ket{y} \maps\ket{(y + a) \operatorname{mod} N} \end{align} 정수는 QFT로 거의 endian 형식으로 인코딩됩니다.

## <a name="input"></a>입력

### <a name="increment--int"></a>증가값: [Int](xref:microsoft.quantum.lang-ref.int)

$Y $에 더할 정수 증가값 $a $입니다.


### <a name="modulus--int"></a>모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)

Mods $y + a $의 정수 $N $입니다.


### <a name="target--phaselittleendian"></a>대상: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

$A $가에 추가 되는 단계 인코딩된 작은 endian 형식의 정수 $y $입니다 `increment` .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

에 `target` 가장 높은 비트가 0으로 설정 된 것으로 가정 합니다.
또한은 대상의 값이 $ $N 미만 이라고 가정 합니다.

회로 다이어그램 및 설명은 [arXiv: vant-ph/0205095v3의 5 페이지](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5)에서 그림 5를 참조 하세요.

## <a name="see-also"></a>참고 항목

- [IncrementByModularInteger.](xref:Microsoft.Quantum.Arithmetic.IncrementByModularInteger)