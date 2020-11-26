---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: SizeAdjustedTruthTable 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: c53ac3f2c46bca955847fc7b380337e3910390ac
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202926"
---
# <a name="sizeadjustedtruthtable-function"></a>SizeAdjustedTruthTable 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


변수의 수에 따라 부울의 배열에서 참 테이블을 조정 합니다.

새 배열은 길이가 반환 되며 항목을 `2^numVars` `table` 사용 하 여 크기를 확장 `false` 하거나 요소로 자를 수 있습니다 `2^numVars` .

```qsharp
function SizeAdjustedTruthTable (table : Bool[], numVars : Int) : Bool[]
```


## <a name="input"></a>입력

### <a name="table--bool"></a>테이블: [Bool](xref:microsoft.quantum.lang-ref.bool)[]

참 테이블을 실제 값 배열로


### <a name="numvars--int"></a>numVars: [Int](xref:microsoft.quantum.lang-ref.int)

변수 수



## <a name="output--bool"></a>Output: [Bool](xref:microsoft.quantum.lang-ref.bool)[]

크기 조정 참 테이블