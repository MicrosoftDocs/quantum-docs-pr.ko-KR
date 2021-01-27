---
uid: Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator
title: MultiplexOperationsFromGenerator 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsFromGenerator
qsharp.summary: >-
  Applies a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 59afa9d9a34fe74206118680940d243ed8b2496e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852504"
---
# <a name="multiplexoperationsfromgenerator-operation"></a>MultiplexOperationsFromGenerator 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


N-\ket{j} $로 제어 될 때 단일 $V _j $를 적용 하는 곱하기 제어 된 단일 $U 작업을 적용 합니다.

$U = \sum ^ {N-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $입니다.

```qsharp
operation MultiplexOperationsFromGenerator<'T> (unitaryGenerator : (Int, (Int -> ('T => Unit is Adj + Ctl))), index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="unitarygenerator--intint---t--unit--is-adj--ctl"></a>Unit Arygenerator: ([int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)

첫 번째 요소가 `Int` unitaries $N $의 수이 고 두 번째 요소는 $ `(Int -> ('T => () is Adj + Ctl))` [0, N-1] $의 정수 $j $를 사용 하는 함수 이며 _j $ $V 단일 작업을 출력 합니다.


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

- [*Andrew Childs, Dmitri Maslov, Yunseong 베트남, Neil Ross, 위안 Su*, arxiv: 1711.10980](https://arxiv.org/abs/1711.10980)