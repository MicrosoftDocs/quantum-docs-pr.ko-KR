---
uid: Microsoft.Quantum.Arrays.LookupFunction
title: LookupFunction 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: LookupFunction
qsharp.summary: Given an array, returns a function which returns elements of that array.
ms.openlocfilehash: 22b56bb7e9f03ebc5b2225efb2e6450d56022664
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845692"
---
# <a name="lookupfunction-function"></a>LookupFunction 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


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