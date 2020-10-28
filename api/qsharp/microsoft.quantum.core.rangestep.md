---
uid: Microsoft.Quantum.Core.RangeStep
title: RangeStep 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: f8e4c42330f2d6afdc1c0a9bdde36081ccab2f94
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713161"
---
# <a name="rangestep-function"></a>RangeStep 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Core)

패키지 [](https://nuget.org/packages/)


범위의 다음 값이 계산 되는 방법을 지정 하는 정수를 반환 합니다.

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a>입력

### <a name="range--range"></a>범위: [범위](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

지정 된 범위의 정의 된 단계 값입니다.

## <a name="remarks"></a>설명

범위 식의 첫 번째 요소는이 `start` `start+step` `start+step+step` 전달 될 때까지, 두 번째 요소는, 세 번째 요소는 등입니다. `end`