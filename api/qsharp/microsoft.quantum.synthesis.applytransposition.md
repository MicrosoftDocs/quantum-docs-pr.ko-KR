---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: ApplyTransposition 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: 46cf8c2c891aa02b0d8a1397e6c2b7a4b8618048
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855574"
---
# <a name="applytransposition-operation"></a>ApplyTransposition 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>설명

이 작업을 수행 하면 `a` `b` 길이가 $n $ 인 지정 된 상태 vector의 인덱스에 있는 진폭을 인덱스에 있는 진폭으로 바꿉니다 `register` .  `a`가와 같으면 `b` 상태 벡터는 변경 되지 않습니다.

## <a name="input"></a>입력

### <a name="a--int"></a>a: [Int](xref:microsoft.quantum.lang-ref.int)

첫 번째 인덱스 (0에서 $2 ^ n-$1 사이의 값 이어야 함)


### <a name="b--int"></a>b: [Int](xref:microsoft.quantum.lang-ref.int)

두 번째 인덱스 (0에서 $2 ^ n-$1 사이의 값 이어야 함)


### <a name="qubits--littleendian"></a>작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Transposition이 적용 되는 $ $n의 목록입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>예

Superposition의 숫자 상태 $ | 1 \ rangle $, $ | 2 \ rangle $ 및 $ | 3 \ rangle $ on 2를 준비 합니다.

```qsharp
using (qubits = Qubit[2]) {
  let register = LittleEndian(qubits);
  PrepareUniformSuperposition(3, register);
  ApplyTransposition(0, 3, register);
}
```