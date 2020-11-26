---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: _ComputeJordanWignerBitString 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 8121421a77174ef3e894381b281964b448e00a18
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203946"
---
# <a name="_computejordanwignerbitstring-function"></a>_ComputeJordanWignerBitString 함수

네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Fermion 개의 생성/annihilation 연산자를 사용 하 여 fermionic 연산자의 인덱스 사이에서 요르단 – Wigner 문자열의 Z 구성 요소를 계산 합니다.

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a>입력

### <a name="nfermions--int"></a>nFermions: [Int](xref:microsoft.quantum.lang-ref.int)

시스템의 fermions 수입니다.


### <a name="idxfermions--int"></a>idxFermions: [Int](xref:microsoft.quantum.lang-ref.int)[]

fermionic 연산자 인덱스입니다.



## <a name="output--bool"></a>Output: [Bool](xref:microsoft.quantum.lang-ref.bool)[]

`Bool[]` `true` 를 적용 해야 하는 비트 문자열입니다 `PauliZ` .