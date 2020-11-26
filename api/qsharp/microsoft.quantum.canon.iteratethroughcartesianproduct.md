---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: IterateThroughCartesianProduct 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: 6340c7a972253e6f583a3856df93a7066ced3139
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206445"
---
# <a name="iteratethroughcartesianproduct-operation"></a>IterateThroughCartesianProduct 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


여러 범위의 데카르트 곱에서 각 인덱스에 대 한 작업을 적용 합니다.

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a>Description

`0..(bounds[0] - 1)`, `0..(bounds[1] - 1)` , ...,,, ...,의 데카르트 곱의 각 요소에 대 한 작업을 반복적으로 적용 합니다.`0..(bounds[Length(bounds) - 1] - 1)`

## <a name="input"></a>입력

### <a name="bounds--int"></a>범위: [Int](xref:microsoft.quantum.lang-ref.int)[]

반복할 범위를 지정 하 고 각 범위를 정수 길이로 지정 하는 배열입니다.


### <a name="op--int--unit"></a>op: [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) 

지정 된 데카르트 곱의 각 요소에 대해 호출 되는 작업입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [IterateThroughCartesianPower입니다.](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)