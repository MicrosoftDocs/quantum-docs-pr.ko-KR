---
uid: Microsoft.Quantum.Arrays.Swapped
title: 교환 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Swapped
qsharp.summary: Applies a swap of two elements in an array.
ms.openlocfilehash: 575d6b76e52f198d91ab5557ada8032df491cfa3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850946"
---
# <a name="swapped-function"></a>교환 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열에 두 요소의 교환을 적용 합니다.

```qsharp
function Swapped<'T> (firstIndex : Int, secondIndex : Int, arr : 'T[]) : 'T[]
```


## <a name="input"></a>입력

### <a name="firstindex--int"></a>firstIndex: [Int](xref:microsoft.quantum.lang-ref.int)

교환할 첫 번째 요소의 인덱스입니다.


### <a name="secondindex--int"></a>secondIndex: [Int](xref:microsoft.quantum.lang-ref.int)

스왑할 두 번째 요소의 인덱스입니다.


### <a name="arr--t"></a>arr: ' t []

스왑할 요소가 포함 된 배열입니다.



## <a name="output--t"></a>출력: ' t []

내부 교환이 적용 된 배열입니다.

## <a name="example"></a>예

```qsharp
// The following returns [0, 3, 2, 1, 4]
Swapped(1, 3, [0, 1, 2, 3, 4]);
```

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

