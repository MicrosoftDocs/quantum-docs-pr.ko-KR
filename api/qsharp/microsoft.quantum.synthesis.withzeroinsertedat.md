---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: WithZeroInsertedAt 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 414b703151b9152aa69709d9c28e68e5ae63506f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228868"
---
# <a name="withzeroinsertedat-function"></a>WithZeroInsertedAt 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


0 비트를 정수에 삽입 합니다.

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a>Description

이 작업은 정수를 사용 하 고 0을 비트 `position` 단위로 삽입 한 다음 업데이트 된 값을 정수로 반환 합니다.  예를 들어 10 ($10 _ = 1010_ $)의 위치 2에 0을 삽입 하면 {10} {2} 숫자 18 ($18 _ {10} = 10010_ {2} $)이 반환 됩니다.

## <a name="input"></a>입력

### <a name="position--int"></a>position: [Int](xref:microsoft.quantum.lang-ref.int)

0이 삽입 되는 위치입니다.


### <a name="value--int"></a>값: [Int](xref:microsoft.quantum.lang-ref.int)

수정 된 값



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

수정 된 값