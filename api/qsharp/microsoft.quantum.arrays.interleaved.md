---
uid: Microsoft.Quantum.Arrays.Interleaved
title: 인터리브 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 1ff5999cc19f47e3dcae601b960446923b613d90
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220963"
---
# <a name="interleaved-function"></a>인터리브 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


인터리브 하며는 거의 동일한 크기의 두 배열을 가집니다.

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a>Description

이 함수는 첫 번째 배열에서 첫 번째 요소부터 시작 하 여 두 배열의 인터리빙을 반환 합니다.

첫 번째 배열의 길이는 두 번째 배열의 길이와 동일 하거나 하나 이상의 요소를 가질 수 있어야 합니다.

## <a name="input"></a>입력

### <a name="first--t"></a>first: ' t []

인터리브 될 첫 번째 배열입니다.


### <a name="second--t"></a>second: ' t []

인터리브 될 두 번째 배열입니다.



## <a name="output--t"></a>출력: ' t []

인터리브 배열

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

및의 각 요소 형식입니다 `first` `second` .