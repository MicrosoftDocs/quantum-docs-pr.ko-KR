---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: IterateThroughCartesianPower 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 526d28cbf3cd356b4f48eec02b3f032f70a868d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716024"
---
# <a name="iteratethroughcartesianpower-operation"></a>IterateThroughCartesianPower 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


정수 범위의 데카르트 제곱에 있는 각 인덱스에 대해 작업을 적용 합니다.

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a>Description

범위에서 데카르트 제곱의 각 요소에 대 한 작업을 반복적으로 적용 `0..(bound - 1)` 합니다.

## <a name="input"></a>입력

### <a name="power--int"></a>power: [Int](xref:microsoft.quantum.lang-ref.int)

범위가 발생 해야 하는 데카르트 제곱입니다 `0..(bound - 1)` .


### <a name="bound--int"></a>바인딩: [Int](xref:microsoft.quantum.lang-ref.int)

범위 길이로 지정 된 반복 될 범위에 대 한 사양입니다.


### <a name="op--int--unit"></a>op: [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) 

지정 된 데카르트 거듭제곱의 각 요소에 대해 호출 되는 작업입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [IterateThroughCartesianProduct입니다.](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)