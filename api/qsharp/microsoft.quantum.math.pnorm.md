---
uid: Microsoft.Quantum.Math.PNorm
title: PNorm 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: cea85715e448305486f6d8a6c10e11da56edf3ee
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722300"
---
# <a name="pnorm-function"></a>PNorm 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지 [](https://nuget.org/packages/)


`L(p)`S 벡터의 표준을 반환 합니다 `Double` .

즉, 형식의 $x $ 배열을 지정 하면 `Double[]` $-ad$ \| x \| \_ p = (\ sum_ {j} | x_j | ^ {p}) ^ {1/p} $ $p 반환 됩니다.

```qsharp
function PNorm (p : Double, array : Double[]) : Double
```


## <a name="input"></a>입력

### <a name="p--double"></a>p: [Double](xref:microsoft.quantum.lang-ref.double)

$P $-일반의 지 수 $p입니다.


### <a name="array--double"></a>array: [Double](xref:microsoft.quantum.lang-ref.double)[]





## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

$P $-일반 $ \| x \| _p $입니다.