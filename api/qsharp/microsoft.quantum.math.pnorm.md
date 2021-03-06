---
uid: Microsoft.Quantum.Math.PNorm
title: PNorm 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: 6207cca6cda5f9030facd31c327e58bdb9ecbf14
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847646"
---
# <a name="pnorm-function"></a>PNorm 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


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