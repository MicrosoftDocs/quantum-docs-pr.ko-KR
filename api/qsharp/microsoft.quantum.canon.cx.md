---
uid: Microsoft.Quantum.Canon.CX
title: CX 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CX
qsharp.summary: >-
  Applies the controlled-X (CX) gate to a pair of qubits.

  $$ \begin{align} \left(\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{matrix}\right) \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: e27b30a6b4609daaac2cc5eda68120115777af0c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840748"
---
# <a name="cx-operation"></a>CX 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


제어 된 X (CX) 게이트를 한 쌍의 비트에 적용 합니다.

$ $ \begin{align} \left (\begin{matrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 0 & 0 & 0 & 1 0 & 0 & 1 \\ \\ \\ \\ & 0 \end{matrix}\right) \end{align}, $ $ 여기서 행과 열은 퀀텀 개념 가이드에서와 같이 구성 됩니다.

```qsharp
operation CX (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="control--qubit"></a>제어: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

CX gate의 비트를 제어 합니다.


### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

CX gate의 대상입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

다음에 해당 합니다.

```qsharp
Controlled X([control], target);
```

그리고 다음을 수행 합니다.

```qsharp
CNOT(control, target);
```