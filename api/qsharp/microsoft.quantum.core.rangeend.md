---
uid: Microsoft.Quantum.Core.RangeEnd
title: 범위 종료 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 90a9e31bf5c4a5e92a35998ddaec8c9e9de9888e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224040"
---
# <a name="rangeend-function"></a>범위 종료 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Core)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


시퀀스의 마지막 요소가 아닐 수 있는 지정 된 범위의 정의 된 끝 값을 반환 합니다.

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a>입력

### <a name="range--range"></a>범위: [범위](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

지정 된 범위의 정의 된 끝 값입니다.

## <a name="remarks"></a>설명

범위 식의 첫 번째 요소는이 `start` `start+step` `start+step+step` 전달 될 때까지, 두 번째 요소는, 세 번째 요소는 등입니다. `end`

범위의 정의 된 끝 값은 범위에 지정 된 시퀀스의 마지막 요소와 다를 수 있습니다. 예를 들어, 범위는 0 .입니다. 2.. 5 마지막 요소는 4 이지만 끝 값은 5입니다.