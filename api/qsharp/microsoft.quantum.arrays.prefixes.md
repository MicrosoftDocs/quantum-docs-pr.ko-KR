---
uid: Microsoft.Quantum.Arrays.Prefixes
title: 전위 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: a2e1721f8f59bf9aa425f04710637023d482a2ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845504"
---
# <a name="prefixes-function"></a>전위 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


배열이 지정 된 경우 모든 접두사를 반환 합니다.

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a>설명

전체 배열까지 첫 번째 요소만 포함 하는 배열부터 시작 하 여 모든 접두사의 배열을 반환 합니다.

## <a name="input"></a>입력

### <a name="array--t"></a>배열: ' t []

요소의 배열입니다.



## <a name="output--t"></a>출력: ' t [] []



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

`array`요소의 형식입니다.

## <a name="example"></a>예제

```qsharp
let prefixes = Prefixes([23, 42, 144]);
// prefixes = [[23], [23, 42], [23, 42, 144]]
```