---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: ColumnAt 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: ad09ada1a2253a54e70dddd6dba8aa243d2cd5a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719456"
---
# <a name="columnat-function"></a>ColumnAt 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지 [](https://nuget.org/packages/)


행렬에서 열을 추출 합니다.

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a>Description

이 함수는 행 단위 순서로 행렬의 열을 추출 합니다.
Corrsponds 행을 추출 하면 첫 번째 인덱스의 요소에 액세스할 수 있으므로 추가 처리가 필요 하지 않습니다.

## <a name="input"></a>입력

### <a name="column--int"></a>열: [Int](xref:microsoft.quantum.lang-ref.int)

행렬의 열


### <a name="matrix--t"></a>matrix: ' t [] []

2 차원 행렬 (행 단위 순서)



## <a name="output--t"></a>출력: ' t []



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

에 있는 각 요소의 형식입니다 `matrix` .

## <a name="see-also"></a>참고 항목

- [Microsoft 양자 배열](xref:Microsoft.Quantum.Arrays.Transposed)
- [Microsoft 양자. 배열 대각선](xref:Microsoft.Quantum.Arrays.Diagonal)