---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorL
title: ExtendedGreatestCommonDivisorL 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorL
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 1445f1c3d2a5852459a492fa5e6bfd2a685786d9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857525"
---
# <a name="extendedgreatestcommondivisorl-function"></a>ExtendedGreatestCommonDivisorL 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


$U \cdot a + v \cdot b = \operatorname{GCD} (a, b) $와 같이 튜플을 $ (u, v) $로 계산 합니다. 여기서 $ \operatorname{GCD} $은 $a $ $a $ 및 $b $의 최대 공약수입니다. GCD는 항상 양수입니다.

```qsharp
function ExtendedGreatestCommonDivisorL (a : BigInt, b : BigInt) : (BigInt, BigInt)
```


## <a name="input"></a>입력

### <a name="a--bigint"></a>a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

확장 된 최대 공약수를 계산 하는 첫 번째 숫자입니다.


### <a name="b--bigint"></a>b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

확장 된 최대 공약수를 계산 하는 두 번째 숫자입니다.



## <a name="output--bigintbigint"></a>출력: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))

튜플을 $ (u, v) $로, 속성 $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $입니다.

## <a name="references"></a>참조

- 이 구현은 다음에 따라 구현 됩니다. https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm