---
uid: Microsoft.Quantum.Math.SquaredNorm
title: SquaredNorm 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: 72ae8266492bef64eaec34cd70c5fe725ee1e8c9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848206"
---
# <a name="squarednorm-function"></a>SquaredNorm 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


벡터의 2 차 제곱을 반환 합니다.

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a>설명

벡터의 2 차 제곱을 반환 합니다. 즉, 입력 $ \vec{x} $가 지정 된 경우 $ \ sum_i x_i ^ 2 $를 반환 합니다.

## <a name="input"></a>입력

### <a name="array--double"></a>array: [Double](xref:microsoft.quantum.lang-ref.double)[]

제곱 2-표준을 반환 하는 벡터입니다.



## <a name="output--double"></a>출력: [Double](xref:microsoft.quantum.lang-ref.double)

의 2 차 제곱입니다 `array` .