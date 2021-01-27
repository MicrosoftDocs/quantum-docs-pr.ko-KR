---
uid: Microsoft.Quantum.Arithmetic.MultiplyByModularInteger
title: MultiplyByModularInteger 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyByModularInteger
qsharp.summary: Performs modular multiplication by an integer constant on a qubit register.
ms.openlocfilehash: bd4e0ad6c5bad779d9a31139690021fd9fcda210
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846500"
---
# <a name="multiplybymodularinteger-operation"></a>MultiplyByModularInteger 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


이상 비트 레지스터에서 정수 상수로 모듈식 곱하기를 수행 합니다.

```qsharp
operation MultiplyByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>설명

`modulus`$N $ 및 $a $를 사용 하 여 나타냅니다 `constMultiplier` .
그런 다음이 작업은 계산 단위로 정의 된 단일 작업을 구현 합니다. $ $ \begin{align} \ket{y} \maps\ket{(a \mapsto y) \operatorname{mod} N} \end{align} $ $ (모든 $y $ between $0 $N $-$1)

## <a name="input"></a>입력

### <a name="constmultiplier--int"></a>constMultiplier: [Int](xref:microsoft.quantum.lang-ref.int)

승수를 곱할 때 기준이 되는 상수입니다. 모듈러스 여야 합니다.


### <a name="modulus--int"></a>모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)

곱하기 연산은 모듈로 수행 됩니다 `modulus` .


### <a name="multiplier--littleendian"></a>승수: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

상수로 곱할 숫자입니다.
이는 작은 endian 형식의 정수를 인코딩 하는 배열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

- 회로 다이어그램 및 설명의 경우 [8 페이지의 arXiv: daant-ph/0205095v3 페이지](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8) 에서 그림 7을 참조 하세요.
- 이 작업은 [Arxiv: ₐ/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf) 의 u에 해당 합니다.