---
uid: Microsoft.Quantum.Math.PNormalized
title: PNormalized 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: 196bdab67528aa8672a010ac3830459e27276ce9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227525"
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