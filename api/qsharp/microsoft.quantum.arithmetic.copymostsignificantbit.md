---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: CopyMostSignificantBit 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 609e937a03bebf45aa9398225bd1b7e2b717807a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843263"
---
# <a name="copymostsignificantbit-operation"></a>CopyMostSignificantBit 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


`from`부호 없는 정수를 나타내는 값 비트 레지스터의 가장 중요 한 비트를 해당 비트에 복사 합니다 `target` .

```qsharp
operation CopyMostSignificantBit (from : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj
```


## <a name="input"></a>입력

### <a name="from--littleendian"></a>시작: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

상위 비트가 복사 되는 부호 없는 정수입니다.
정수는 작은 endian 형식으로 인코딩됩니다.


### <a name="target--qubit"></a>대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

가장 높은 비트를 복사할 때 기준이 되는 비트입니다. 비트 인코딩은 계산 기준입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [LittleEndian.](xref:Microsoft.Quantum.Arithmetic.LittleEndian)