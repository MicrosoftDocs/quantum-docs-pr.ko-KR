---
uid: Microsoft.Quantum.Canon.ApplyIfElseBC
title: ApplyIfElseBC 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical bit.
ms.openlocfilehash: ea06b0a0a07659407e13caa2baa4f3e37ca2a0f7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209522"
---
# <a name="applyifelsebc-operation"></a>ApplyIfElseBC 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


클래식 비트의 값에 따라 제어 가능한 두 작업 중 하나를 적용 합니다.

```qsharp
operation ApplyIfElseBC<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Ctl), trueInput : 'T), (falseOp : ('U => Unit is Ctl), falseInput : 'U)) : Unit is Ctl
```


## <a name="description"></a>Description

비트가 지정 된 경우 `bit` 가 인 경우 `trueOp` 해당 입력으로 작업을 적용 `trueInput` `bit` `true` 하 고가 인 경우 적용 됩니다 `falseOp(falseInput)` `bit` `false` .

## <a name="input"></a>입력

### <a name="bit--bool"></a>bit: [Bool](xref:microsoft.quantum.lang-ref.bool)

또는를 적용할지 여부를 결정 하는 데 사용 되는 부울 값 `trueOp` `falseOp` 입니다.


### <a name="trueop--t--unit--is-ctl"></a>trueOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.

가 일 때 적용 되는 제어 가능한 작업입니다 `bit` `true` .


### <a name="trueinput--t"></a>trueInput: ' '

가 인 경우에 제공 되는 입력입니다 `trueOp` `bit` `true` .


### <a name="falseop--u--unit--is-ctl"></a>falseOp: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.

가 일 때 적용 되는 제어 가능한 작업입니다 `bit` `false` .


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