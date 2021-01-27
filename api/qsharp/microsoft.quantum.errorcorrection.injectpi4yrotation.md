---
uid: Microsoft.Quantum.ErrorCorrection.InjectPi4YRotation
title: InjectPi4YRotation 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: InjectPi4YRotation
qsharp.summary: Rotates a single qubit by π/4 about the Y-axis.
ms.openlocfilehash: 249c347c9e9729e719eda69e4e9a21847d9a46eb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825954"
---
# <a name="injectpi4yrotation-operation"></a>InjectPi4YRotation 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Y 축에 대해 π/4를 기준으로 단일의 비트를 회전 합니다.

```qsharp
operation InjectPi4YRotation (data : Qubit, magic : Qubit) : Unit is Adj
```


## <a name="description"></a>설명

에 대해 π/4 회전을 수행 `Y` 합니다.

회전은 매직 상태를 사용 하 여 수행 됩니다. 즉, $ $ \begin{align} \cos\frac{\pi} {8} \ket {0} + \sin \frac{\pi} \ket 상태를 복사 합니다 {8} {1} .
\end{align} $ $

## <a name="input"></a>입력

### <a name="data--qubit"></a>데이터: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

$ \Pi/$4에 대 한 $Y $에 대해 회전 하는 데 사용할 비트입니다.


### <a name="magic--qubit"></a>마법: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

초기 상태의 초기 상태에 있는 놀라운 비트입니다. 이 작업의 다음 응용 프로그램이 `magic` $ \ket $ 상태로 반환 됩니다 {0} .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

다음은 동일 합니다.

```qsharp
Ry(PI() / 4.0, data);
```

및

```qsharp
using (magic = Qubit()) {
    Ry(PI() / 4.0, magic);
    InjectPi4YRotation(data, magic);
    Reset(magic);
}
```

이 작업은 동작을 지원 합니다 .이 `Adjoint` 경우 동일한 매직 상태를 사용 하지만 데이터의 효과는 $-\ pi/4 $ $Y $-회전입니다.