---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: DecomposedOn 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: fb7aa5af8f3eb07399e0d2dd2d50723f4e6b169a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855520"
---
# <a name="decomposedon-function"></a>DecomposedOn 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


변수에서 순열 분해

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a>설명

순열 $ \pi $ ( `perm` ) 및 인덱스 $i $ ( `index` )이 지정 된 경우이 메서드는 세 개의 순열 $ ((\ pi_l, \ pi_r), \pi ') $를 반환 하 여 $ \ pi_l $ 및 $ \ pi_r $의 이미지가 $i $ 이외의 인덱스에 있는 요소의 비트를 변경 하지 않도록 하 고 해당 요소에서 $ \pi의 이미지를 변경할 수 없습니다.

## <a name="input"></a>입력

### <a name="perm--int"></a>perm: [Int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="index--int"></a>인덱스: [Int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--intintint"></a>Output: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])



## <a name="example"></a>예

입력이 perm = [0, 2, 3, 5, 7, 1, 4, 6] 및 인덱스 = 0 인 것으로 가정 합니다 .이 함수는 다음 표를 기준으로 세 개의 순열 ( `perm` 그룹 A의 요소와 그룹 D의 이미지)을 포함 하는 이진 표기법의 순열 목록을 계산 합니다.  열에는 비트 인덱스가 나열 됩니다.

|   A |   B |   C |   D |
| 2 1 0 | 2 1 0 | 2 1 0 | 2 1 0 |
|-------|-------|-------|-------|
| 0 0 0 |       |       | 0 0 0 | 0
| 0 0 1 |       |       | 0 1 0 | 2
| 0 1 0 |       |       | 0 1 1 | 3
| 0 1 1 |       |       | 1 0 1 | 5
| 1 0 0 |       |       | 1 1 1 | 7
| 1 0 1 |       |       | 0 0 1 | 1
| 1 1 0 |       |       | 1 0 0 | 4
| 1 1 1 |       |       | 1 1 0 | 6

인덱스의 모든 값이 0 (= 인덱스)이 아닌 경우 A에서 B로, D에서 C로 복사 됩니다.

|   A |   B |   C |   D |
| 2 1 0 | 2 1 0 | 2 1 0 | 2 1 0 |
|-------|-------|-------|-------|
| 0 0 0 | 0 0   | 0 0   | 0 0 0 |
| 0 0 1 | 0 0   | 0 1   | 0 1 0 |
| 0 1 0 | 0 1   | 0 1   | 0 1 1 |
| 0 1 1 | 0 1   | 1 0   | 1 0 1 |
| 1 0 0 | 1 0   | 1 1   | 1 1 1 |
| 1 0 1 | 1 0   | 0 0   | 0 0 1 |
| 1 1 0 | 1 1   | 1 0   | 1 0 0 |
| 1 1 1 | 1 1   | 1 1   | 1 1 0 |

다음은 블록 B의 열 0에 빈 인덱스가 있는 첫 번째 요소에 대해 0이 배치 된 다음 1이 B에 배치 되 고 (첫 번째 경우에는 인덱스가 0 0 인 다른 행) B에 배치 됩니다.
그런 다음 블록 C의 동일한 행에 1이 추가 된 다음 블록 C의 해당 접두사에 대해 0이 추가 됩니다.  이 프로세스는 모든 인덱스가 B 및 C 블록의 0 열에 배치 될 때까지 반복 됩니다.

|   A |   B |   C |   D |
| 2 1 0 | 2 1 0 | 2 1 0 | 2 1 0 |
|-------|-------|-------|-------|
| 0 0 0 | 0 0 0 | 0 0 0 | 0 0 0 |
| 0 0 1 | 0 0 1 | 0 1 1 | 0 1 0 |
| 0 1 0 | 0 1 0 | 0 1 0 | 0 1 1 |
| 0 1 1 | 0 1 1 | 1 0 1 | 1 0 1 |
| 1 0 0 | 1 0 0 | 1 1 0 | 1 1 1 |
| 1 0 1 | 1 0 1 | 0 0 1 | 0 0 1 |
| 1 1 0 | 1 1 0 | 1 0 0 | 1 0 0 |
| 1 1 1 | 1 1 1 | 1 1 1 | 1 1 0 |

테이블에서 다음과 같은 세 가지 새 순열을 읽을 수 있습니다.

- $ \ pi_l $ (요소 포함), B의 이미지 (왼쪽)
- D의 요소가 포함 된 $ \ pi_r $, C (오른쪽)의 이미지
- $ \pi ' $ (B의 요소 포함), C의 이미지 (나머지)

인덱스 1과 2에 대 한 $ \ pi_l $ 및 $ \ pi_r $에서 디자인 비트 값은 변경 되지 않으며 인덱스 0의 경우 $ \ pi_ ' $의 비트 값은 변경 되지 않습니다.  또한 $ \ pi_l $ 및 $ \ pi_r $은 (는) 자체 역 이어야 합니다.

파생 된 순열 및 반환 된 순열: left = [0, 1, 2, 3, 4, 5, 6, 7] right = [0, 1, 3, 2, 4, 5, 7, 6] 나머지가 = [0, 3, 2, 5, 6, 1, 4, 7]