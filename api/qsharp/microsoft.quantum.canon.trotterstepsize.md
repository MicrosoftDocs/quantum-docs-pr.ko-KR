---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: TrotterStepSize 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: fabfbff74572b3c96c701de5443e4265a0468d78
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715226"
---
# <a name="trotterstepsize-function"></a>TrotterStepSize 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


Trotter 시뮬레이션 알고리즘의 재귀적 구현에서 Trotter step 크기를 계산 합니다.

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a>입력

### <a name="order--int"></a>순서: [Int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>설명

이 [작업은 다른](https://arxiv.org/abs/quant-ph/0508139)인덱싱 규칙을 사용 합니다. 특히 `DecomposedIntoTimeStepsCA(_, 4)` 은 _2/0508139의 스칼라 $p (\lambda) $에 해당 합니다.