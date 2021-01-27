---
uid: Microsoft.Quantum.Bitwise.ZBits
title: ZBits 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: ZBits
qsharp.summary: Returns an integer representing the Z bits of an array of Pauli operators.
ms.openlocfilehash: d1ddc2a4cdbdfd3945885de856456b3108592594
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842069"
---
# <a name="zbits-function"></a>ZBits 함수

네임 스페이스: [Microsoft. 양자 비트](xref:Microsoft.Quantum.Bitwise)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Pauli 연산자 배열의 Z 비트를 나타내는 정수를 반환 합니다.

```qsharp
function ZBits (paulis : Pauli[]) : Int
```


## <a name="input"></a>입력

### <a name="paulis--pauli"></a>paulis: [Paulis](xref:microsoft.quantum.lang-ref.pauli)[]

정수로 나타낼 Pauli 연산자의 배열입니다.



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

정수 $x $ (p_ {62} \, p_ {61} \, \dots .. \, p_0) $ (여기서 $p _i = $0 인 경우 $p _i = $1 인 경우 `paulis[i]` `PauliI` `PauliX` `paulis[i]` 이 고 `PauliY` `PauliZ` , 그렇지 않으면입니다.

## <a name="remarks"></a>설명

배열의 길이가 63 보다 큰 경우 함수는을 throw 합니다 `paulis` .

## <a name="see-also"></a>참고 항목

- [Microsoft 양자. x x x 비트](xref:Microsoft.Quantum.Bitwise.XBits)