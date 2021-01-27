---
uid: Microsoft.Quantum.Canon.MultiplexOperationsWithAuxRegister
title: MultiplexOperationsWithAuxRegister 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsWithAuxRegister
qsharp.summary: Implementation step of MultiplexOperations.
ms.openlocfilehash: 91db22d6261709c1c3506c80ff600c904748575a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852470"
---
# <a name="multiplexoperationswithauxregister-operation"></a>MultiplexOperationsWithAuxRegister 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


MultiplexOperations의 구현 단계입니다.

```qsharp
operation MultiplexOperationsWithAuxRegister<'T> (unitaries : ('T => Unit is Adj + Ctl)[], auxillaryRegister : Qubit[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="unitaries--t--unit--is-adj--ctl"></a>unitaries: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl []




### <a name="auxillaryregister--qubit"></a>auxillaryRegister: [](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="index--littleendian"></a>인덱스: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)




### <a name="target--t"></a>대상: ' '





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="see-also"></a>참고 항목

- [MultiplexOperations입니다.](xref:Microsoft.Quantum.Canon.MultiplexOperations)