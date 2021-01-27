---
uid: Microsoft.Quantum.Core.RangeReverse
title: RangeReverse 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: f3b94d3c6fa6350a2c337f8bc8d889d24d87a85b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853654"
---
# <a name="rangereverse-function"></a>RangeReverse 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Core)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


입력 범위의 역순 인 새 범위를 반환 합니다.

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a>입력

### <a name="r--range"></a>r: [범위](xref:microsoft.quantum.lang-ref.range)

입력 범위.



## <a name="output--range"></a>출력: [범위](xref:microsoft.quantum.lang-ref.range)

지정 된 범위의 역순 인 새 범위입니다.

## <a name="remarks"></a>설명

범위의 `end` `-step` `start` 마지막 요소는와 같을 수 없기 때문에 범위를 반대로 하는 것은 간단 합니다. `end`