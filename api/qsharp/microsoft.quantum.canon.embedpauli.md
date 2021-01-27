---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: EmbedPauli 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: 0e6a93e22ee495abcc44bdf522e7c72c0981308b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840529"
---
# <a name="embedpauli-function"></a>EmbedPauli 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


단일 기능 비트를 지정 하는 경우 해당 인덱스 및 다른 모든 인덱스에서 지정 된 단일 수준 비트 연산자를 사용 하 여 다중 값 비트 Pauli 연산자를 반환 합니다 `PauliI` .

```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
```


## <a name="input"></a>입력

### <a name="pauli--pauli"></a>pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

지정 된 위치에 배치 되는 단일의 비트 Pauli 연산자입니다.


### <a name="location--int"></a>위치: [Int](xref:microsoft.quantum.lang-ref.int)

`output[location] == pauli`이 함수의 출력 인 인덱스입니다 `output` .


### <a name="n--int"></a>n: [Int](xref:microsoft.quantum.lang-ref.int)

반환 될 배열의 길이입니다.



## <a name="output--pauli"></a>출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]



## <a name="example"></a>예

배열을 가져오려면 다음을 `[PauliI, PauliI, PauliX, PauliI]` 수행 합니다.

```qsharp
EmbedPauli(PauliX, 2, 3);
```