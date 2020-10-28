---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: DecomposedOn 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: b033723a50fb85e77c9d4baec1f94231327e9b25
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725219"
---
# <a name="decomposedon-function"></a>DecomposedOn 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지 [](https://nuget.org/packages/)


변수에서 순열 분해

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a>Description

순열 $ \pi $ ( `perm` ) 및 인덱스 $i $ ( `index` )이 지정 된 경우이 메서드는 세 개의 순열 $ ((\ pi_l, \ pi_r), \pi ') $를 반환 하 여 $ \ pi_l $ 및 $ \ pi_r $의 이미지가 $i $ 이외의 인덱스에 있는 요소의 비트를 변경 하지 않도록 하 고 해당 요소에서 $ \pi의 이미지를 변경할 수 없습니다.

## <a name="input"></a>입력

### <a name="perm--int"></a>perm: [Int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="index--int"></a>인덱스: [Int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--intintint"></a>Output: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])

