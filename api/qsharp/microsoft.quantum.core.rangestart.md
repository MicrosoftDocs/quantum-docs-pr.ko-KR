---
uid: Microsoft.Quantum.Core.RangeStart
title: 범위 시작 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 44683b204ecd469f5f5412a7ec06e98ec8a4f37e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224006"
---
# <a name="rangestart-function"></a>범위 시작 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Core)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


지정 된 범위의 정의 된 시작 값을 반환 합니다.

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a>입력

### <a name="range--range"></a>범위: [범위](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

지정 된 범위의 정의 된 시작 값입니다.

## <a name="remarks"></a>설명

범위 식의 첫 번째 요소는이 `start` `start+step` `start+step+step` 전달 될 때까지, 두 번째 요소는, 세 번째 요소는 등입니다. `end`

범위에서 정의 된 시작 값은 범위에서 빈 시퀀스 (예: 2.)를 지정 하는 경우를 제외 하 고는 시퀀스의 첫 번째 요소와 동일 합니다. 1).