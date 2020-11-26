---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsC
title: ApplySeriesOfOpsC 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsC
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Controlled)
ms.openlocfilehash: eaa0ea3e33cce708af5879cfbe875397fbb82a8a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217937"
---
# <a name="applyseriesofopsc-operation"></a>ApplySeriesOfOpsC 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Ops 및 해당 대상의 목록을 배열에 순차적으로 적용 합니다. 제어

```qsharp
operation ApplySeriesOfOpsC<'T> (listOfOps : ('T[] => Unit is Ctl)[], targets : Int[][], register : 'T[]) : Unit is Ctl
```


## <a name="input"></a>입력

### <a name="listofops--t--unit--is-ctl"></a>listOfOps: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl []입니다.

각각의 배열을 적용 하는 작업의 목록입니다. 가장 낮은 인덱스 순으로 순차적으로 적용 됩니다.
각에는 제어 되는 함수를 포함 해야 합니다.


### <a name="targets--int"></a>대상: [Int](xref:microsoft.quantum.lang-ref.int)[] []

Op의 대상을 설명 하는 중첩 된 배열입니다. 각 배열에는 사용할 인덱스를 설명 하는 정수 목록이 포함 되어야 합니다.


### <a name="register--t"></a>등록: ' t []

작업할의 비트 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyOpRepeatedlyOver](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)