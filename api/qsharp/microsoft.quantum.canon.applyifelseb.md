---
uid: Microsoft.Quantum.Canon.ApplyIfElseB
title: ApplyIfElseB 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseB
qsharp.summary: Applies one of two operations, depending on the value of a classical bit.
ms.openlocfilehash: 68c06a5141b9ff423c2d18adc3a9e162eed939f6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718220"
---
# <a name="applyifelseb-operation"></a>ApplyIfElseB 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


는 클래식 비트의 값에 따라 두 작업 중 하나를 적용 합니다.

```qsharp
operation ApplyIfElseB<'T, 'U> (bit : Bool, (trueOp : ('T => Unit), trueInput : 'T), (falseOp : ('U => Unit), falseInput : 'U)) : Unit
```


## <a name="description"></a>Description

비트가 지정 된 경우 `bit` 가 인 경우 `trueOp` 해당 입력으로 작업을 적용 `trueInput` `bit` `true` 하 고가 인 경우 적용 됩니다 `falseOp(falseInput)` `bit` `false` .

## <a name="input"></a>입력

### <a name="bit--bool"></a>bit: [Bool](xref:microsoft.quantum.lang-ref.bool)

또는를 적용할지 여부를 결정 하는 데 사용 되는 부울 값 `trueOp` `falseOp` 입니다.


### <a name="trueop--t--unit"></a>trueOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) 

가 인 경우 적용 될 작업 `bit` 입니다 `true` .


### <a name="trueinput--t"></a>trueInput: ' '

가 인 경우에 제공 되는 입력입니다 `trueOp` `bit` `true` .


### <a name="falseop--u--unit"></a>falseOp: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) 

가 인 경우 적용 될 작업 `bit` 입니다 `false` .


### <a name="falseinput--u"></a>falseInput: ' U

가 인 경우에 제공 되는 입력입니다 `falseOp` `bit` `false` .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

조건부로 적용할 작업의 입력 형식 `trueOp` 입니다.
### <a name="u"></a>' U

조건부로 적용할 작업의 입력 형식 `falseOp` 입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyIfZero](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [Microsoft. 양자. ApplyIfOne](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [Microsoft. 양자. ApplyIfElseRC](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [Microsoft. 양자. ApplyIfElseRA](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [Microsoft. 양자. ApplyIfElseRCA](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)