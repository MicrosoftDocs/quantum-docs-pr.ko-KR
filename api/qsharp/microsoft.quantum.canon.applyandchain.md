---
uid: Microsoft.Quantum.Canon.ApplyAndChain
title: ApplyAndChain 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAndChain
qsharp.summary: Computes a chain of AND gates
ms.openlocfilehash: 3991ded1a9c70bf4b58d19b0304a1df3b31896d0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842011"
---
# <a name="applyandchain-operation"></a>ApplyAndChain 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


및 게이트 체인을 계산 합니다.

```qsharp
operation ApplyAndChain (auxRegister : Qubit[], ctrlRegister : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="description"></a>설명

임시 결과를 계산 하는 보조 비트를 명시적으로 지정 해야 합니다.
해당 레지스터의 길이는 `Length(ctrlRegister) - 2` 두 개 이상의 컨트롤이 있는 경우이 고, 그렇지 않으면 길이가 0입니다.

## <a name="input"></a>입력

### <a name="auxregister--qubit"></a>auxRegister: [](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="ctrlregister--qubit"></a>ctrlRegister: [](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

