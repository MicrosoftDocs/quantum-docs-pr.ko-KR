---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyCA
title: ApplyConditionallyCA 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyCA
qsharp.summary: ''
ms.openlocfilehash: e456ed5d8f7f17a914401473948c89c020174903
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720176"
---
# <a name="applyconditionallyca-operation"></a>ApplyConditionallyCA 작업

네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

패키지 [](https://nuget.org/packages/)




```qsharp
operation ApplyConditionallyCA<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Ctl + Adj), equalArg : 'T), (onNonEqualOp : ('U => Unit is Ctl + Adj), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a>입력

### <a name="measurementresults--__invalidresult__"></a>measurementResults: __잘못 <Result> 된__ []




### <a name="resultsvalues--__invalidresult__"></a>resultsValues: __잘못 <Result> 된__ []




### <a name="onequalop--t--unit-ctl--adj"></a>OnAdj p: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl +




### <a name="equalarg--t"></a>equalArg: ' '




### <a name="onnonequalop--u--unit-ctl--adj"></a>Onnonp: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj




### <a name="nonequalarg--u"></a>nonEqualArg: ' U





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다


### <a name="u"></a>' U

