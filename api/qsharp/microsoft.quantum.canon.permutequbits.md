---
uid: Microsoft.Quantum.Canon.PermuteQubits
title: PermuteQubits 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: PermuteQubits
qsharp.summary: Permutes qubits by using the SWAP operation.
ms.openlocfilehash: 2fbbe0d99ad1383d77cb08ff6b03bcebd8a1971f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852335"
---
# <a name="permutequbits-operation"></a>PermuteQubits 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


교환 작업을 사용 하 여 Permutes 된 비트

```qsharp
operation PermuteQubits (ordering : Int[], register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="ordering--int"></a>순서 지정: [Int](xref:microsoft.quantum.lang-ref.int)[]

이제 인덱스 i의 새 정렬에 대해 설명 합니다. 여기서는 이제 [i]를 순서 대로 정렬 합니다.


### <a name="register--qubit"></a>register: [](xref:microsoft.quantum.lang-ref.qubit)

작업할의 비트 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>예

지정 된 주문 = [2, 1, 0] 및 등록 $ \ket{\ alpha_0} \ket{\ alpha_1} \ket{\ alpha_2} $ PermuteQubits는 레지스터를 $ \ket{\ alpha_2} \ket{\ alpha_1} \ket{\ alpha_0} $로 변경 합니다.

```qsharp
// The following two lines are equivalent
PermuteQubits([2, 1, 0], register);
SWAP(register[0], register[2]);
```