---
uid: Microsoft.Quantum.Arrays.Diagonal
title: 대각선 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: 180b7185c94d712fa02100cb97abfbb6c464d12a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719384"
---
# <a name="diagonal-function"></a>대각선 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지 [](https://nuget.org/packages/)


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