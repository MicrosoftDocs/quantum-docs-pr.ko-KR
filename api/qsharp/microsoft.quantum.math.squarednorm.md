---
uid: Microsoft.Quantum.Math.SquaredNorm
title: SquaredNorm 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: 4165a761753f336cb7b94ad36b11ac324ad4e5c6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725023"
---
# <a name="squarednorm-function"></a>SquaredNorm 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지 [](https://nuget.org/packages/)


벡터의 2 차 제곱을 반환 합니다.

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a>Description

벡터의 2 차 제곱을 반환 합니다. 즉, 입력 $ \vec{x} $가 지정 된 경우 $ \ sum_i x_i ^ 2 $를 반환 합니다.

## <a name="input"></a>입력

### <a name="array--double"></a>array: [Double](xref:microsoft.quantum.lang-ref.double)[]

제곱 2-표준을 반환 하는 벡터입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

의 2 차 제곱입니다 `array` .