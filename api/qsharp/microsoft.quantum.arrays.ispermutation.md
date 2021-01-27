---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: IsPermutation 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 7e563650f33b0292e1e41f629829a2d3b9e5fd28
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848088"
---
# <a name="ispermutation-function"></a>IsPermutation 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 배열이 순열을 나타내는 경우에만 true를 출력 합니다.

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a>설명

길이가 인 배열이 지정 된 경우에는의 `array` `n` 각 정수가에서 정확히 한 번 표시 되는 경우에만 true를 반환 합니다 `0` `n - 1` . 예를 들어 `array` `array` 요소에 대 한 순열으로 해석 될 수 있습니다 `n` .

## <a name="input"></a>입력

### <a name="permuation--int"></a>permuation: [Int](xref:microsoft.quantum.lang-ref.int)[]

순열을 나타낼 수 있거나 나타내지 않을 수 있는 배열입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)



## <a name="example"></a>예

다음 Q # 코드는 "모든 진단이 성공적으로 완료 되었습니다." 라는 메시지를 출력 합니다.

```qsharp
Fact(IsPermutation([2, 0, 1], "");
Contradiction(IsPermutation([5, 0, 1], "[5, 0, 1] isn't a permutation");
Message("All diagnostics completed successfully.");
```

## <a name="remarks"></a>설명

길이가 0 인 배열은 순열 일반적으로 됩니다.