---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: AssertMostSignificantBit 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 41381455d1a96970647f887e038f7dff3a4eb204
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223785"
---
# <a name="assertmostsignificantbit-operation"></a>AssertMostSignificantBit 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


부호 없는 정수를 나타내는 고 비트 레지스터의 가장 중요 한 것이 특정 상태에 있음을 어설션 합니다.

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="value--__invalidresult__"></a>값: __잘못 <Result> 됨__

어설션된 상위 비트의 값입니다.


### <a name="number--littleendian"></a>number: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

가장 높은 비트를 확인 하는 부호 없는 정수입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

이 작업의 제어 된 버전은 컨트롤을 무시 합니다.

## <a name="see-also"></a>참고 항목

- [Microsoft 양자. Assert](xref:Microsoft.Quantum.Intrinsic.Assert)