---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: IntegerBits 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: 3352c1b3003ee387fb03b72461fedb400e29046d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855413"
---
# <a name="integerbits-function"></a>IntegerBits 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


정수의 비트가 설정 된 모든 위치를 반환 합니다.

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a>입력

### <a name="value--int"></a>값: [Int](xref:microsoft.quantum.lang-ref.int)

음수가 아닌 숫자입니다.


### <a name="length--int"></a>길이: [Int](xref:microsoft.quantum.lang-ref.int)

의 이진 확장의 비트 수입니다 `value` .



## <a name="output--int"></a>Output: [Int](xref:microsoft.quantum.lang-ref.int)[]

모든 비트의 `value` 위치를 고려 하는 이진 확장의 1 인 모든 비트 위치 (0부터 시작)를 포함 하는 배열입니다 `length - 1` .  모든 위치는 배열에서 오름차순으로 정렬 됩니다.

## <a name="example"></a>예제

```qsharp
IntegerBits(23, 5); // [0, 1, 2, 4]
IntegerBits(10, 4); // [1, 3]
```