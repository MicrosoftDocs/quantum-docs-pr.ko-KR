---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOps
title: ApplySeriesOfOps 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOps
qsharp.summary: Applies a list of ops and their targets sequentially on an array.
ms.openlocfilehash: b086b01b0be86bd25a6d6cdef26bfbb53e484cb2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841507"
---
# <a name="applyseriesofops-operation"></a>ApplySeriesOfOps 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Ops 및 해당 대상의 목록을 배열에 순차적으로 적용 합니다.

```qsharp
operation ApplySeriesOfOps<'T> (listOfOps : ('T[] => Unit)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a>입력

### <a name="listofops--t--unit-"></a>listOfOps: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit) []

각각의 배열을 적용 하는 작업의 목록입니다. 가장 낮은 인덱스 순으로 순차적으로 적용 됩니다.


### <a name="targets--int"></a>대상: [Int](xref:microsoft.quantum.lang-ref.int)[] []

Op의 대상을 설명 하는 중첩 된 배열입니다. 각 배열에는 사용할 인덱스를 설명 하는 정수 목록이 포함 되어야 합니다.


### <a name="register--t"></a>등록: ' t []

작업할의 비트 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="example"></a>예

다음은 Exp ([PauliX, PauliY], 0.5)를 PauliY에 적용 하 고, 1//then X to ybit 2 let ops = [Exp ([PauliX,], 0.5, _), Applytofirst Bit (X, _)];를 적용 합니다. let 인덱스 = [[0, 1], [2]]; ApplySeriesOfOps (ops, 인덱스, 및 Bitbitarray);

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyOpRepeatedlyOver](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)