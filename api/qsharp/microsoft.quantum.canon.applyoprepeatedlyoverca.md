---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverCA
title: Applyoprepeatedly과잉 Ca 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverCA
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: b7d401f323d7affc27697744bb659c687e252682
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209112"
---
# <a name="applyoprepeatedlyoverca-operation"></a>Applyoprepeatedly과잉 Ca 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


단일 비트 레지스터에 대해 동일한 op를 여러 번 적용 합니다.

```qsharp
operation ApplyOpRepeatedlyOverCA (op : (Qubit[] => Unit is Adj + Ctl), targets : Int[][], register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="op--qubit--unit--is-adj--ctl"></a>op: [이상](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Adj + Ctl입니다.

이 작업을 수행 합니다.


### <a name="targets--int"></a>대상: [Int](xref:microsoft.quantum.lang-ref.int)[] []

Op의 대상을 설명 하는 중첩 된 배열입니다. 각 배열에는 사용할 비트를 설명 하는 정수 목록이 포함 되어야 합니다.


### <a name="register--qubit"></a>register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

작업할의 비트 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [ApplySeriesOfOps입니다.](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)