---
uid: Microsoft.Quantum.Math.PNormalized
title: PNormalized 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: ea6a88d07d3b246f666b793f0b10ab6598ea4ff6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854844"
---
# <a name="pnormalized-function"></a>PNormalized 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


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