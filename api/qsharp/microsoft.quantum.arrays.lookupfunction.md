---
uid: Microsoft.Quantum.Arrays.LookupFunction
title: LookupFunction 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: LookupFunction
qsharp.summary: Given an array, returns a function which returns elements of that array.
ms.openlocfilehash: c929054b96ee499db896cacf0e3ae4da6f6c4b98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719072"
---
# <a name="lookupfunction-function"></a>LookupFunction 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지 [](https://nuget.org/packages/)


배열이 지정 된 경우 해당 배열의 요소를 반환 하는 함수를 반환 합니다.

```qsharp
function LookupFunction<'T> (array : 'T[]) : (Int -> 'T)
```


## <a name="input"></a>입력

### <a name="array--t"></a>배열: ' t []

조회 함수로 나타낼 배열입니다.



## <a name="output--int---t"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int) > ' t '

이에 `f` 해당 하는 함수 `f(idx) == f[idx]` 입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

조회 함수로 표시 되는 배열의 요소 형식입니다.

## <a name="remarks"></a>설명

이 함수는 함수 및 함수를 인수로 사용 하는 작업과의 상호 운용을 위해 주로 유용 `Int -> 'T` 합니다. 예를 들어, 함수를 사용 하 여 전체 배열을 메모리에 기록할 필요가 없도록 하는 생성기 표현 라이브러리에서 일반적입니다.