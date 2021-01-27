---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: TrotterStepSize 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: c7b6432645dcad2bd47c62b91e04e0b42cd04ca9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840066"
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