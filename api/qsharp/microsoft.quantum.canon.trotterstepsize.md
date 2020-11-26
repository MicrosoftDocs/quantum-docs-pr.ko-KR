---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: TrotterStepSize 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: aa5b63e058e1ea726b0d4c6eca73078831daaf3b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204694"
---
# <a name="trotterstepsize-function"></a>TrotterStepSize 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Trotter 시뮬레이션 알고리즘의 재귀적 구현에서 Trotter step 크기를 계산 합니다.

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a>입력

### <a name="order--int"></a>순서: [Int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>설명

이 [작업은 다른](https://arxiv.org/abs/quant-ph/0508139)인덱싱 규칙을 사용 합니다. 특히 `DecomposedIntoTimeStepsCA(_, 4)` 은 _2/0508139의 스칼라 $p (\lambda) $에 해당 합니다.