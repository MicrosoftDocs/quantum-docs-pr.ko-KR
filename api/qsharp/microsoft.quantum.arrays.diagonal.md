---
uid: Microsoft.Quantum.Arrays.Diagonal
title: 대각선 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: fe6bac0acfa07b14620c7c35ae5e1cec2287d13d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221541"
---
# <a name="diagonal-function"></a>대각선 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


2 차원 배열의 대각선 요소 배열을 반환 합니다.

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a>Description

2 차원 배열에 정사각형이 아닌 도형이 있으면 행 및 열 수에 대 한 최소의 대각선이 반환 됩니다.

## <a name="input"></a>입력

### <a name="matrix--t"></a>matrix: ' t [] []

2 차원 행렬 (행 단위 순서)



## <a name="output--t"></a>출력: ' t []



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

에 있는 각 요소의 형식입니다 `matrix` .

## <a name="see-also"></a>참고 항목

- [Microsoft 양자 배열](xref:Microsoft.Quantum.Arrays.Transposed)