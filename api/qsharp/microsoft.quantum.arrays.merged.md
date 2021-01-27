---
uid: Microsoft.Quantum.Arrays.Merged
title: 병합 된 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: 262e7450188370212a7e2a57bf15e9f8ab162814
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845621"
---
# <a name="merged-function"></a>병합 된 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


정렬 된 두 배열이 지정 된 경우 정렬 된 순서에서 두 요소가 모두 포함 된 단일 배열을 반환 합니다. Merge sort에 의해 내부적으로 사용 됩니다.

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a>입력

### <a name="comparison--tt---bool"></a>비교: (' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)




### <a name="left--t"></a>left: ' t []




### <a name="right--t"></a>right: ' t []





## <a name="output--t"></a>출력: ' t []



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

