---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByInteger
title: IncrementPhaseByInteger 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: cc7922b2940cb979394958d5eb4e9933144eb062
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843158"
---
# <a name="incrementphasebyinteger-operation"></a>IncrementPhaseByInteger 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


단계 회전을 사용 하 여, 부호 없는 퀀텀 레지스터를 고전 정수로 늘립니다.

```qsharp
operation IncrementPhaseByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>설명

가 `target` $x 부호 없는 정수를 작은 endian 인코딩으로 인코딩하고 $a $와 같은 경우를 가정 `increment` 합니다.
그런 다음이 작업을 수행 하면 단일 $ \ket{x} \maps\ket{x + a} $이 구현 됩니다. 여기서 더하기는 모듈로 $2 ^ n $, 여기서 $n = \texttt{Length (target!)}입니다. $.

## <a name="input"></a>입력

### <a name="increment--int"></a>증가값: [Int](xref:microsoft.quantum.lang-ref.int)

가 증가 하는 정수 `target` 입니다.


### <a name="target--phaselittleendian"></a>대상: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

퀀텀 레지스터는 이중 (QFT) 기반의 작은 endian 인코딩을 사용 하 여 부호 없는 정수를 인코딩합니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

증분은 퀀텀 레지스터가 아닌 기존 상수 이므로 회로가 간소화 되었습니다.

회로 다이어그램 및 설명은 [ arXiv: 10-ant-ph/0008033v1의 6 페이지 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) 에 있는 그림을 참조 하세요.

## <a name="references"></a>참조

- [*Thomas G. Draper*, arxiv: mant-ph/0008033](https://arxiv.org/pdf/quant-ph/0008033v1.pdf)

## <a name="see-also"></a>참고 항목

- [IncrementByInteger.](xref:Microsoft.Quantum.Arithmetic.IncrementByInteger)