---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseIntrinsicCA
title: ApplyIfElseIntrinsicCA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseIntrinsicCA
qsharp.summary: ''
ms.openlocfilehash: 6ba83f7344c77b95f2e7397cd42f39884556547a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855690"
---
# <a name="applyifelseintrinsicca-operation"></a>ApplyIfElseIntrinsicCA 작업

네임 스페이스: [QuantumProcessor. 확장명](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)




```qsharp
operation ApplyIfElseIntrinsicCA (measurementResult : Result, onResultZeroOp : (Unit => Unit is Ctl + Adj), onResultOneOp : (Unit => Unit is Ctl + Adj)) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="measurementresult--__invalidresult__"></a>measurementResult: __잘못 <Result> 됨__




### <a name="onresultzeroop--unit--unit--is-adj--ctl"></a>onResultZeroOp: [unit](xref:microsoft.quantum.lang-ref.unit) => [unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl




### <a name="onresultoneop--unit--unit--is-adj--ctl"></a>onresultoneop: [unit](xref:microsoft.quantum.lang-ref.unit) => [unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

