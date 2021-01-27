---
uid: Microsoft.Quantum.Diagnostics._iterateThroughCartesianPower
title: _iterateThroughCartesianPower 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _iterateThroughCartesianPower
qsharp.summary: Iterates a variable through a Cartesian product [ 0, bounds[0]-1 ] × [ 0, bounds[1]-1 ] × [ 0, bounds[Length(bounds)-1]-1 ] and calls op(arr) for every element of the Cartesian product
ms.openlocfilehash: a27302be75ee701b0629310700b56d222aaef7db
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853570"
---
# <a name="_iteratethroughcartesianpower-operation"></a>_iterateThroughCartesianPower 작업

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


데카르트 product [0, 경계 [0]-1] × [0, 경계 [1]-1] × [0, 경계 [길이 (범위)-1]-1]를 통해 변수를 반복 하 고 데카르트 제품의 모든 요소에 대해 op (arr)를 호출 합니다.

```qsharp
operation _iterateThroughCartesianPower (length : Int, value : Int, op : (Int[] => Unit)) : Unit
```


## <a name="input"></a>입력

### <a name="length--int"></a>길이: [Int](xref:microsoft.quantum.lang-ref.int)




### <a name="value--int"></a>값: [Int](xref:microsoft.quantum.lang-ref.int)




### <a name="op--int--unit"></a>op: [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) 





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

