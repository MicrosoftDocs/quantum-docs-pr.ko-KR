---
uid: Microsoft.Quantum.Characterization.ApplyHadamardTestOnSingleRegister
title: ApplyHadamardTestOnSingleRegister 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ApplyHadamardTestOnSingleRegister
qsharp.summary: ''
ms.openlocfilehash: 2b6592cb837115f143931f6bc084bec66eaa84fe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840013"
---
# <a name="applyhadamardtestonsingleregister-operation"></a>ApplyHadamardTestOnSingleRegister 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)




```qsharp
operation ApplyHadamardTestOnSingleRegister (phaseShift : Bool, commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a>입력

### <a name="phaseshift--bool"></a>phaseShift: [Bool](xref:microsoft.quantum.lang-ref.bool)




### <a name="commonpreparation--qubit--unit--is-adj"></a>commonPreparation: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is




### <a name="preparation1--qubit--unit--is-adj--ctl"></a>preparation1: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl + Ctl




### <a name="preparation2--qubit--unit--is-adj--ctl"></a>preparation2: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl + Ctl




### <a name="register--qubit"></a>register: [](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

