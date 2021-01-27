---
uid: Microsoft.Quantum.Canon.MultiplexOperations
title: MultiplexOperations 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperations
qsharp.summary: >-
  Applies an array of operations controlled by an array of number states.

  That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 1cf483bb0d3b7cc43d271b65a2363fab95ff0f3b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852540"
---
# <a name="multiplexoperations-operation"></a>MultiplexOperations 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


숫자 상태의 배열에 의해 제어 되는 작업 배열을 적용 합니다.

즉, $n $-\ket{j} $로 제어 될 때 단일 $V _j $를 적용 하는 곱하기 제어 된 단일 $U 작업을 적용 합니다.

$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.

```qsharp
operation MultiplexOperations<'T> (unitaries : ('T => Unit is Adj + Ctl)[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="unitaries--t--unit--is-adj--ctl"></a>unitaries: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl []

최대 $2 ^ n $ 단일 작업의 배열입니다. $J $ th 연산은 작은 endian 형식으로 인코딩된 숫자 상태 $ \ket{j} $로 인덱싱됩니다.


### <a name="index--littleendian"></a>인덱스: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

숫자 상태 $ \ket{j} $를 거의 endian 형식으로 인코딩하는 $-# 컨트롤 레지스터를 $n 합니다.


### <a name="target--t"></a>대상: ' '

$V _j $가 작동 하는 일반 고 비트 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="remarks"></a>설명

`coefficients` $2 ^ n $ 미만으로 지정 된 경우는 id 요소로 채워집니다. 이 구현에서는 $n-$1 보조 비트를 사용 합니다.

## <a name="references"></a>참조

- 퀀텀 속도 향상 Andrew Childs, Dmitri Maslov, Yunseong 베트남, Neil Ross, 위안 Su를 사용 하 여 첫 번째 퀀텀 시뮬레이션을 지향 합니다. https://arxiv.org/abs/1711.10980