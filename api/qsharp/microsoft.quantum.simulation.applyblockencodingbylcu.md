---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: ApplyBlockEncodingByLCU 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: a9a9e3bbd598453719f49f78392f3a92c9401b36
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852820"
---
# <a name="applyblockencodingbylcu-operation"></a>ApplyBlockEncodingByLCU 작업

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


`BlockEncodingByLCU`의 구현입니다.

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="statepreparation--t--unit--is-adj--ctl"></a>statePreparation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl




### <a name="selector--ts--unit--is-adj--ctl"></a>selector: (' ' ') => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl




### <a name="auxiliary--t"></a>보조: ' '




### <a name="system--s"></a>시스템:





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다


### <a name="s"></a>큐브의

