---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRA
title: ApplyIfElseRA operation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRA
qsharp.summary: ''
ms.openlocfilehash: bcc52c6e2b4dfc6354e12c57e19739ac021d2e8f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725415"
---
# <a name="applyifelsera-operation"></a>ApplyIfElseRA operation

네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

패키지 [](https://nuget.org/packages/)




```qsharp
operation ApplyIfElseRA<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj), zeroArg : 'T), (onResultOneOp : ('U => Unit is Adj), oneArg : 'U)) : Unit
```


## <a name="input"></a>입력

### <a name="measurementresult--__invalidresult__"></a>measurementResult: __잘못 <Result> 됨__




### <a name="onresultzeroop--t--unit-adj"></a>onResultZeroOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj




### <a name="zeroarg--t"></a>zeroArg: ' '




### <a name="onresultoneop--u--unit-adj"></a>onResultOneOp: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj




### <a name="onearg--u"></a>oneArg: ' U





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다


### <a name="u"></a>' U

