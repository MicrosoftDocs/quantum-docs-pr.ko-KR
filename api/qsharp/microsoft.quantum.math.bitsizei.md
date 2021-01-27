---
uid: Microsoft.Quantum.Math.BitSizeI
title: BitSizeI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeI
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: e7edf37a81571dfa1d4cb755493e1863a44c694e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857694"
---
# <a name="bitsizei-function"></a>BitSizeI 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


음수가 아닌 정수의 경우 `a` 를 나타내는 데 필요한 비트 수를 반환 `a` 합니다.

즉, $a < 2 ^ n $와 같은 가장 작은 $n $를 반환 합니다.

```qsharp
function BitSizeI (a : Int) : Int
```


## <a name="input"></a>입력

### <a name="a--int"></a>a: [Int](xref:microsoft.quantum.lang-ref.int)

비트 크기를 계산할 정수입니다.



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

의 비트 크기 `a` 입니다.