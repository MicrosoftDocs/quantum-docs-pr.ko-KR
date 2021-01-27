---
uid: Microsoft.Quantum.Preparation.BlochSphereCoordinates
title: BlochSphereCoordinates 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: BlochSphereCoordinates
qsharp.summary: >-
  Computes the Bloch sphere coordinates for a single-qubit state.

  Given two complex numbers $a0, a1$ that represent the qubit state, computes coordinates on the Bloch sphere such that $a0 \ket{0} + a1 \ket{1} = r e^{it}(e^{-i \phi /2}\cos{(\theta/2)}\ket{0}+e^{i \phi /2}\sin{(\theta/2)}\ket{1})$.
ms.openlocfilehash: 62643f64a6b829949fa708e300d9d262527dbb29
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855896"
---
# <a name="blochspherecoordinates-function"></a>BlochSphereCoordinates 함수

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


단일가 나 비트 상태에 대 한 Bloch 구 좌표를 계산 합니다.

지정 된 두 복소수 $a 0, a1 $는 Bloch 구의 좌표를 계산 하는 구의 좌표를 계산 하는 구의 좌표를 계산 합니다. 예를 들어, $a 0 \ket {0} + a1 \ket {1} = r e ^ {it} (e ^ {-i \emlb = r e ^ {(\ 테타/2)} \ket {0} + e ^ {i \emlc\sin{(\ 테타 {1}

```qsharp
function BlochSphereCoordinates (a0 : Microsoft.Quantum.Math.ComplexPolar, a1 : Microsoft.Quantum.Math.ComplexPolar) : (Microsoft.Quantum.Math.ComplexPolar, Double, Double)
```


## <a name="input"></a>입력

### <a name="a0--complexpolar"></a>a0: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)

상태 $ \ket $의 복합 계수입니다 {0} .


### <a name="a1--complexpolar"></a>a1: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)

상태 $ \ket $의 복합 계수입니다 {1} .



## <a name="output--complexpolardoubledouble"></a>출력: ([Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar),[double](xref:microsoft.quantum.lang-ref.double),[double](xref:microsoft.quantum.lang-ref.double))

을 포함 하는 튜플입니다 `(ComplexPolar(r, t), phi, theta)` .