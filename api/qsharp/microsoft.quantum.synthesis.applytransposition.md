---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: ApplyTransposition 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: ca22b090f2b2613f07caef698941ea608374ab1e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203317"
---
# <a name="applytransposition-operation"></a>ApplyTransposition 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Description

이 작업을 수행 하면 `a` `b` 길이가 $n $ 인 지정 된 상태 vector의 인덱스에 있는 진폭을 인덱스에 있는 진폭으로 바꿉니다 `register` .  `a`가와 같으면 `b` 상태 벡터는 변경 되지 않습니다.

## <a name="input"></a>입력

### <a name="a--int"></a>a: [Int](xref:microsoft.quantum.lang-ref.int)

첫 번째 인덱스 (0에서 $2 ^ n-$1 사이의 값 이어야 함)


### <a name="b--int"></a>b: [Int](xref:microsoft.quantum.lang-ref.int)

두 번째 인덱스 (0에서 $2 ^ n-$1 사이의 값 이어야 함)


### <a name="qubits--littleendian"></a>작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Transposition이 적용 되는 $ $n의 목록입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

