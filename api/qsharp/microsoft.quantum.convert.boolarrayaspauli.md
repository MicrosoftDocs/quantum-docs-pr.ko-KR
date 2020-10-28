---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: BoolArrayAsPauli 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: c5ef71322dae248fc2c6b1db3adf891de7d72488
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713602"
---
# <a name="boolarrayaspauli-function"></a>BoolArrayAsPauli 함수

네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)

패키지 [](https://nuget.org/packages/)


비트 문자열이 지정 된 경우 단일 수준 비트 Pauli 연산자의 배열로 표시 되는 다중 값 비트 Pauli 연산자를 반환 합니다.

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a>입력

### <a name="pauli--pauli"></a>pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

에 적용 되는 pauli 연산자 `bitsApply == bits[idx]` .


### <a name="bitapply--bool"></a>bitApply: [Bool](xref:microsoft.quantum.lang-ref.bool)

bit가이 값 이면 Pauli를 적용 합니다.


### <a name="bits--bool"></a>bits: [Bool](xref:microsoft.quantum.lang-ref.bool)[]

부울 배열입니다.



## <a name="output--pauli"></a>출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]



## <a name="remarks"></a>설명

부울 배열과 퀀텀 레지스터의 길이는 같아야 합니다.