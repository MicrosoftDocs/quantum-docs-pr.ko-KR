---
uid: Microsoft.Quantum.Characterization.MeasureIdentity
title: MeasureIdentity 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: MeasureIdentity
qsharp.summary: Measures the identity operator on a register of qubits.
ms.openlocfilehash: 71a103fddb3a27703318975bea94bc7a22a9ce81
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714967"
---
# <a name="measureidentity-operation"></a>MeasureIdentity 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)

패키지 [](https://nuget.org/packages/)


은 (는) 다양 한 비트의 레지스터에서 identity 연산자를 측정 합니다.

```qsharp
operation MeasureIdentity (register : Qubit[]) : Result
```


## <a name="input"></a>입력

### <a name="register--qubit"></a>register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

측정할 레지스터입니다.



## <a name="output--__invalidresult__"></a>출력: __잘못 <Result> 됨__

결과 값 `Zero` 입니다.

## <a name="remarks"></a>설명

$ \Boldone $에는 eigenvalue $1 $만 있고 음수 eigenvalue이 없기 때문에이 작업은 항상를 반환 하며 `Zero` ,이는 eigenvalue $ + 1 = (-1) ^ 0 $에 해당 하며, 상태를 축소 하지 않습니다 `register` .

자체적으로이 작업은 유용 하지 않지만 프로세스 tomography의 컨텍스트에서는 퀀텀 프로세스의 추적 유지에 대 한 정보를 제공 하므로 유용 합니다.
특히 손실 측정이 있는 대상 컴퓨터는 $ \boldone $의 실제 측정을 통해이 작업을 대체 해야 합니다.