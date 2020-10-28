---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: SizeAdjustedTruthTable 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: 3480f022df7a289594b003f201d16d8bf7c29d7e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725471"
---
# <a name="sizeadjustedtruthtable-function"></a>SizeAdjustedTruthTable 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지 [](https://nuget.org/packages/)


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