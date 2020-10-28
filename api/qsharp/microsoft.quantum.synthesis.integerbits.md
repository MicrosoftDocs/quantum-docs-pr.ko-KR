---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: IntegerBits 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: ab459cd841cdac116cf0e98c094834f628b6a2d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719845"
---
# <a name="integerbits-function"></a>IntegerBits 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지 [](https://nuget.org/packages/)


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