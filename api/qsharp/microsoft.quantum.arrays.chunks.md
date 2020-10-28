---
uid: Microsoft.Quantum.Arrays.Chunks
title: 청크 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: fe10999d35ed05908fd59b9dad8b5c0c51233ae6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719468"
---
# <a name="chunks-function"></a>청크 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지 [](https://nuget.org/packages/)


배열을 같은 길이의 여러 요소로 분할 합니다.

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a>입력

### <a name="nelements--int"></a>nElements: [Int](xref:microsoft.quantum.lang-ref.int)

각 청크의 길이입니다.


### <a name="arr--t"></a>arr: ' t []

분할할 배열입니다.



## <a name="output--t"></a>출력: ' t [] []

원본 배열의 각 청크를 포함 하는 배열입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="remarks"></a>설명

`nElements`가로 나눌 수 없는 경우 출력의 마지막 요소는 보다 짧을 수 있습니다 `Length(arr)` `nElements` .