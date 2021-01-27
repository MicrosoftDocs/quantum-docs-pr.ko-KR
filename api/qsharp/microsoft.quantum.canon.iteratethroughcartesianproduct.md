---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: IterateThroughCartesianProduct 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: a0aaa8ef6aa6798d31c810254c92820f8136800c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840272"
---
# <a name="iteratethroughcartesianproduct-operation"></a>IterateThroughCartesianProduct 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


여러 범위의 데카르트 곱에서 각 인덱스에 대 한 작업을 적용 합니다.

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a>설명

`0..(bounds[0] - 1)`, `0..(bounds[1] - 1)` , ...,,, ...,의 데카르트 곱의 각 요소에 대 한 작업을 반복적으로 적용 합니다.`0..(bounds[Length(bounds) - 1] - 1)`

## <a name="input"></a>입력

### <a name="bounds--int"></a>범위: [Int](xref:microsoft.quantum.lang-ref.int)[]

반복할 범위를 지정 하 고 각 범위를 정수 길이로 지정 하는 배열입니다.


### <a name="op--int--unit"></a>op: [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) 

지정 된 데카르트 곱의 각 요소에 대해 호출 되는 작업입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>예

작업을 지정 하는 경우 `op` 다음 두 코드 조각이 동일 합니다.

```qsharp
IterateThroughCartesianProduct([3, 4, 5], op);
```

```qsharp
op([0, 0, 0]);
op([1, 0, 0]);
op([2, 0, 0]);
op([0, 1, 0]);
// ...
op([0, 3, 0]);
op([0, 0, 1]);
//
op([2, 3, 4]);
```

## <a name="see-also"></a>참고 항목

- [IterateThroughCartesianPower입니다.](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)