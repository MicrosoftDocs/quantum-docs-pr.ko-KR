---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: ApplyBlockEncodingByLCU 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: 1575b93b6c3242e1dffafb330c44cc017a72a8b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722125"
---
# <a name="applyblockencodingbylcu-operation"></a>ApplyBlockEncodingByLCU 작업

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지 [](https://nuget.org/packages/)


`BlockEncodingByLCU`의 구현입니다.

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit
```


## <a name="input"></a>입력

### <a name="statepreparation--t--unit-adj--ctl"></a>statePreparation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl




### <a name="selector--ts--unit-adj--ctl"></a>selector: (' ' ') => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl




### <a name="auxiliary--t"></a>보조: ' '




### <a name="system--s"></a>시스템:





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다


### <a name="s"></a>큐브의

