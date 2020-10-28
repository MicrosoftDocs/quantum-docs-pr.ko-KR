---
uid: Microsoft.Quantum.Math.PNormalized
title: PNormalized 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: 6f9dfebe83f52cbf486cd8e6874d3699f5e6b8ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722286"
---
# <a name="pnormalized-function"></a>PNormalized 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지 [](https://nuget.org/packages/)


일반에서의 벡터를 정규화 `Double` `L(p)` 합니다.

즉, 형식의 $x $ 배열이 지정 된 경우 `Double[]` 모든 요소가 $-일반 $ x _p $ $p으로 나뉘는 배열을 반환 \| \| 합니다.

```qsharp
function PNormalized (p : Double, array : Double[]) : Double[]
```


## <a name="input"></a>입력

### <a name="p--double"></a>p: [Double](xref:microsoft.quantum.lang-ref.double)

$P $-일반의 지 수 $p입니다.


### <a name="array--double"></a>array: [Double](xref:microsoft.quantum.lang-ref.double)[]





## <a name="output--double"></a>Output: [Double](xref:microsoft.quantum.lang-ref.double)[]

$P $-일반 $ x _p $로 정규화 된 $ $x 배열 \| \| 입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft 양자.](xref:Microsoft.Quantum.Math.PNorm)