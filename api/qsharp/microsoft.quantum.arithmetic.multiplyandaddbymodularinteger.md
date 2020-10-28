---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger
title: MultiplyAndAddByModularInteger 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddByModularInteger
qsharp.summary: Performs a modular multiply-and-add by integer constants on a qubit register.
ms.openlocfilehash: 3f85f6aaea1d6f8095709c6f387322df7a5e047c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719809"
---
# <a name="multiplyandaddbymodularinteger-operation"></a>MultiplyAndAddByModularInteger 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지 [](https://nuget.org/packages/)


은 (는) 정수 계열 레지스터에서 모듈식 곱하기 및 추가 정수 상수를 수행 합니다.

```qsharp
operation MultiplyAndAddByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, summand : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>Description

지정 된 모듈러스 $N $, 상수 승수 $a $ 및 \ket{$y $에 대해 $ $ \begin{align} \ket{x} \ket{b} \maps\ket{x} \operatorname{mod} (b + a \mapsto x) \end{align} N} summand $ $ 맵을 구현 합니다.

## <a name="input"></a>입력

### <a name="constmultiplier--int"></a>constMultiplier: [Int](xref:microsoft.quantum.lang-ref.int)

각 기본 상태 레이블에 추가할 정수 $a $입니다.


### <a name="modulus--int"></a>모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)

와 관련 하 여 더하기 및 곱하기를 수행 하는 모듈러스 $N $입니다.


### <a name="multiplier--littleendian"></a>승수: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

값이의 각 기본 상태 레이블에 추가 될 부호 없는 정수를 나타내는 퀀텀 레지스터입니다 `summand` .


### <a name="summand--littleendian"></a>summand: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

이 작업의 대상으로 사용할 부호 없는 정수를 나타내는 퀀텀 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

- 회로 다이어그램 및 설명의 경우 그림 6 [(arXiv: 5ant-ph/0205095v3 페이지](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7) )을 참조 하세요.
- 이 작업은 [Arxiv: CMULT/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf) 의 (a) MOD (N)에 해당 합니다.

## <a name="see-also"></a>참고 항목

- [MultiplyAndAddPhaseByModularInteger.](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger)