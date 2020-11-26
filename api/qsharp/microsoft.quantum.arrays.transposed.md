---
uid: Microsoft.Quantum.Arrays.Transposed
title: 전치 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: f293399d8e3a2cb32b2929e8d1591ac5eaefd277
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219994"
---
# <a name="transposed-function"></a>전치 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열의 배열로 표시 되는 매트릭스의 바꾸기를 반환 합니다.

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a>Description

$R $ rows 및 $c $ columns를 사용 하 여 $r \times c $ matrix로 입력 합니다.  행렬은 행 기반입니다. 즉, `matrix[i][j]` 행 $i $ 및 열 $j $의 요소에 액세스 합니다.

이 함수는 입력 행렬의 전치 인 $c \times r $ matrix를 반환 합니다.

## <a name="input"></a>입력

### <a name="matrix--t"></a>matrix: ' t [] []

행 기반 $r \times c $ 행렬



## <a name="output--t"></a>출력: ' t [] []

$C \times r $ matrix로 바뀜

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

에 있는 각 요소의 형식입니다 `matrix` .