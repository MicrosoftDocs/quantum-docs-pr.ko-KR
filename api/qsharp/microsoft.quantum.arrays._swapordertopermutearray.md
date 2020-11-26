---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: _SwapOrderToPermuteArray 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: 9df2ec00d91c1124fae960efd15d576b15b0223c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221711"
---
# <a name="_swapordertopermutearray-function"></a>_SwapOrderToPermuteArray 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열에서 정렬 된 배열을 생성 하기 위해 교환 해야 하는 순서 요소를 반환 합니다.
에서 교체가 발생 한다고 가정 합니다.

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a>입력

### <a name="neworder--int"></a>newOrder: [Int](xref:microsoft.quantum.lang-ref.int)[]

새 배열의 인덱스 순열이 포함 된 배열입니다. $ Elements $n 해야 하며, 각각 $0 $에서 $n-$1 사이의 고유한 정수 여야 합니다.



## <a name="output--intint"></a>Output: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []

튜플은 교환 될 두 인덱스를 나타냅니다. 교체는 가장 낮은 인덱스에서 시작 됩니다.

## <a name="remarks"></a>설명

## <a name="psuedocode"></a>Psuedocode

의 경우 (인덱스는 0 ..1 (newOrder)-1) {newOrder [index]! = index {Switch newOrder [index] with newOrder [newOrder [인덱스]]}}