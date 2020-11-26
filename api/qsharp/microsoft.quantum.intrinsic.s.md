---
uid: Microsoft.Quantum.Intrinsic.S
title: S 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: S
qsharp.summary: Applies the S gate to a single qubit.
ms.openlocfilehash: c697408c4efe1963787b5aee8f0d3bb6b9e64dd5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198455"
---
# <a name="s-operation"></a>S 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


단일의 단일 비트에 게이트를 적용 합니다.

```qsharp
operation S (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Description

단일 행렬 \begin{align} S \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ 0 & i \end{bmatrix}.에서이 작업을 시뮬레이션할 수 있습니다.
\end{align}

## <a name="input"></a>입력

### <a name="qubit--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

게이트가 적용 되어야 하는의 비트입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

