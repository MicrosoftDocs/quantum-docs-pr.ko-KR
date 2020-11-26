---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: _DeltaParityCNOTbitstring 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 0c0da60e3c389f8208f9f7d5c84a09893f3c1bda
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226080"
---
# <a name="_deltaparitycnotbitstring-function"></a>_DeltaParityCNOTbitstring 함수

네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .

패키지: [Microsoft](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry) .


의 클래식 처리 단계입니다 `ApplyDeltaParity` .
이는 두 PQRS 사이의 패리티 차이를 평가 하기 위한 제어 비트 목록을 계산 합니다. 짝수의 조건입니다.

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a>입력

### <a name="prevfermionicterm--int"></a>prevFermionicTerm: [Int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="nextfermionicterm--int"></a>nextFermionicTerm: [Int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--intbool"></a>Output: ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])



## <a name="remarks"></a>설명

여기서는 용어 길이가 짝수 라고 가정 합니다.
두 용어 사이의 패리티 차이에 대 한 컨트롤 목록을 계산 합니다.
여기서는 입력 목록이 오름차순으로 정렬 되어 있다고 가정 합니다.