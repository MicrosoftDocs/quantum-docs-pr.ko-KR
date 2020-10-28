---
uid: Microsoft.Quantum.Arrays.Unique
title: Unique 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: c5d40bb82f2de640e9c78eef0c27e4766b477826
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718784"
---
# <a name="unique-function"></a>Unique 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지 [](https://nuget.org/packages/)


인접 한 요소가 없는 새 배열을 반환 합니다.

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a>Description

일부 요소 배열 및 테스트 같음을 지정 하는 경우이 함수는 요소의 상대 순서가 유지 되는 새 배열을 반환 하지만 동일한 모든 인접 요소가 단일 요소로만 필터링 됩니다.

## <a name="input"></a>입력

### <a name="equal--tt---bool"></a>같음: (' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)

`a`가 인 경우와 동일한 것으로 간주 되는 두 요소를 비교 하는 함수입니다 `b` `equal(a, b)` `true` .


### <a name="array--t"></a>배열: ' t []

고유 요소에 대해 필터링 할 배열입니다.



## <a name="output--t"></a>출력: ' t []

인접 한 요소가 없는 배열입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

에 있는 각 요소의 형식입니다 `array` .

## <a name="remarks"></a>설명

동일 하지만 서로 다른 여러 요소가 있는 경우 출력 배열에 여러 요소가 발생 합니다.  과 함께이 함수 `Sorted` 를 사용 하 여 전체 고유 요소가 포함 된 배열을 가져옵니다.