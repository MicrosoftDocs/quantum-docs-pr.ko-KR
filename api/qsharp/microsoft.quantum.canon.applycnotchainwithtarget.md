---
uid: Microsoft.Quantum.Canon.ApplyCNOTChainWithTarget
title: ApplyCNOTChainWithTarget 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChainWithTarget
qsharp.summary: Computes the parity of an array of qubits into a target qubit.
ms.openlocfilehash: fd0a0f3e1db89946aec2c63f3cde7a021608eea5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718364"
---
# <a name="applycnotchainwithtarget-operation"></a>ApplyCNOTChainWithTarget 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


대상 비트의 배열에 대 한 패리티를 계산 합니다.

```qsharp
operation ApplyCNOTChainWithTarget (qubits : Qubit[], targetQubit : Qubit) : Unit
```


## <a name="description"></a>Description

배열이 처음에 $ \ket{q_0} \ket{q_1} \cdots q_ {\text{target}}} $ 상태에 있는 경우, 최종 상태는 $ \ket{q_0} \ket{q_1 \cdots q_0} \cdots \text{target}}} q_ {n-1} \cdots \co\o q_0 \cdots {$로 지정 됩니다.

## <a name="input"></a>입력

### <a name="qubits--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

패리티를 계산 하는 데 사용할 비트의 배열입니다.


### <a name="targetqubit--qubit"></a>Targetbit [:](xref:microsoft.quantum.lang-ref.qubit)

'가 중 비트 '의 패리티가 XORed 하는 마지막입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

다음은 동일 합니다.

```qsharp
ApplyCNOTChainWithTarget(Most(qs), Last(qs));
```

및

```qsharp
ApplyCNOTChain(qs);
```