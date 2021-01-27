---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: ApplySeriesOfOpsCA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 9a1f6189428b086c38b1d0f289afb18c2cf1be40
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850858"
---
# <a name="applyseriesofopsca-operation"></a>ApplySeriesOfOpsCA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Ops 및 해당 대상의 목록을 배열에 순차적으로 적용 합니다. (Adjoint + 제어 됨)

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="listofops--t--unit--is-adj--ctl"></a>listOfOps: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl []

각각의 배열을 적용 하는 작업의 목록입니다. 가장 낮은 인덱스 순으로 순차적으로 적용 됩니다.
각에는 Adjoint 및 제어 된 함수를 모두 포함 해야 합니다.


### <a name="targets--int"></a>대상: [Int](xref:microsoft.quantum.lang-ref.int)[] []

Op의 대상을 설명 하는 중첩 된 배열입니다. 각 배열에는 사용할 인덱스를 설명 하는 정수 목록이 포함 되어야 합니다.


### <a name="register--t"></a>등록: ' t []

작업할의 비트 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="example"></a>예

다음은 Exp ([PauliX, PauliY], 0.5)를 ybits 0에 적용 하 고, 1//then X to abit 2 let ops = [Exp ([PauliX, PauliY], 0.5, _), ApplyToFirstQubitCA (X, _)];를 적용 합니다. let 인덱스 = [[0, 1], [2]]; ApplySeriesOfOpsCA (ops, 인덱스, 및 Bitbitarray);

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyOpRepeatedlyOver](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)