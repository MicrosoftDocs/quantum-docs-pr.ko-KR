---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyC
title: ApplyConditionallyC 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyC
qsharp.summary: ''
ms.openlocfilehash: 963a85e0e442592c01a2e70fa0dc02d6048d8be7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229038"
---
# <a name="applyconditionallyc-operation"></a>ApplyConditionallyC 작업

네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)




```qsharp
operation ApplyConditionallyC<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Ctl), equalArg : 'T), (onNonEqualOp : ('U => Unit is Ctl), nonEqualArg : 'U)) : Unit is Ctl
```


## <a name="input"></a>입력

### <a name="measurementresults--__invalidresult__"></a>measurementResults: __잘못 <Result> 된__[]




### <a name="resultsvalues--__invalidresult__"></a>resultsValues: __잘못 <Result> 된__[]




### <a name="onequalop--t--unit--is-ctl"></a>' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.




### <a name="equalarg--t"></a>equalArg: ' '




### <a name="onnonequalop--u--unit--is-ctl"></a>Onnonp: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.




### <a name="nonequalarg--u"></a>nonEqualArg: ' U





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다


### <a name="u"></a>' U

