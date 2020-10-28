---
uid: Microsoft.Quantum.Extensions.Testing.AssertOperationsEqualInPlace
title: AssertOperationsEqualInPlace 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Extensions.Testing
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  > [!WARNING]

  > AssertOperationsEqualInPlace has been deprecated. Please use <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace> instead.

  >

  > Please use @"microsoft.quantum.diagnostics.assertoperationsequalinplace".

  > Note that the order of the arguments to this operation has changed.
ms.openlocfilehash: 6d2ead95a60ed3cc8ee95fb7f91e1aa49d366a48
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711677"
---
# <a name="assertoperationsequalinplace-operation"></a>AssertOperationsEqualInPlace 작업

네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Extensions.Testing) .

패키지 [](https://nuget.org/packages/)


> [!WARNING]
> AssertOperationsEqualInPlace는 더 이상 사용 되지 않습니다. 대신 <xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace>를 사용하십시오.
>
> @"microsoft.quantum.diagnostics.assertoperationsequalinplace"을 사용하세요.
> 이 작업에 대 한 인수의 순서가 변경 된 것을 확인 합니다.



```qsharp
operation AssertOperationsEqualInPlace (actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj), nQubits : Int) : Unit
```


## <a name="input"></a>입력

### <a name="actual--qubit--unit"></a>actual: [bit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) 




### <a name="expected--qubit--unit-adj"></a>예상: 이상 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj




### <a name="nqubits--int"></a>N Bits: [Int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

