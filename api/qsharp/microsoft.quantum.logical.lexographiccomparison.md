---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: LexographicComparison 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: de8179ab6e835d08e7f41287f31a876b7ecc91c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814395"
---
# <a name="lexographiccomparison-function"></a>LexographicComparison 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


비교 함수가 지정 된 경우 lexographically는 두 배열을 비교 하는 새 함수를 반환 합니다.

```qsharp
function LexographicComparison<'T> (elementComparison : (('T, 'T) -> Bool)) : (('T[], 'T[]) -> Bool)
```


## <a name="input"></a>입력

### <a name="elementcomparison--tt---bool"></a>elementComparison: (' ' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)

두 요소를 비교 하 고 `x` `y` `x` 가 보다 작거나 같은 경우을 반환 하는 함수입니다 `y` .



## <a name="output--tt---bool"></a>Output: (' ' ' ' ' t [])-> [Bool](xref:microsoft.quantum.lang-ref.bool)

두 배열을 비교 하 고 `xs` `ys` `xs` lexographical 정렬에서 이전 또는 같은 경우을 반환 하는 함수입니다 `ys` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

비교할 배열의 요소 형식입니다.

## <a name="remarks"></a>설명

두 배열과 lexographic 비교는 `xs` `ys` 다음 절차에 따라 정의 됩니다. `x` `y` `elementComparison(x, y)` 및가 모두 true 인 경우 두 개의 요소 및가 동일 하다는 것을 알 수 `elementComparison(y, x)` 있습니다.

- 두 배열 모두 동일 하지 않은 요소의 첫 번째 쌍까지 요소 별로 비교 됩니다. 에 따라 먼저 발생 하는 요소를 포함 하는 배열을 `elementComparison` 먼저 lexographical 정렬에서 발생 한다고 합니다.
- Inequivalent 요소가 없고 한 배열이 다른 배열 보다 길면 짧은 배열이 먼저 발생 하는 것으로 간주 됩니다.

## <a name="see-also"></a>참고 항목

- [Microsoft 양자 배열 정렬](xref:Microsoft.Quantum.Arrays.Sorted)