---
uid: Microsoft.Quantum.Canon.ApplyIfElseRCA
title: ApplyIfElseRCA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRCA
qsharp.summary: Applies one of two unitary operations, depending on the value of a classical result.
ms.openlocfilehash: 6dfa2a5cf88029ac772b09bc2d36a5f19ef37a14
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844947"
---
# <a name="applyifelserca-operation"></a>ApplyIfElseRCA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


기존 결과의 값에 따라 두 개의 단일 작업 중 하나를 적용 합니다.

```qsharp
operation ApplyIfElseRCA<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Adj + Ctl), zeroInput : 'T), (oneOp : ('U => Unit is Adj + Ctl), oneInput : 'U)) : Unit is Adj + Ctl
```


## <a name="description"></a>설명

결과를 제공 하면 `result` 가와 같은 경우에는를 사용 하 여 작업을 적용 하 `zeroOp` `zeroInput` `result` `Zero` 고가 적용 됩니다 `oneOp(oneInput)` `result == One` .

## <a name="input"></a>입력

### <a name="result--__invalidresult__"></a>결과: __잘못 <Result> 됨__

또는이 적용 되었는지 확인 하는 데 사용 되는 측정 결과 `zeroOp` `oneOp` 입니다.


### <a name="zeroop--t--unit--is-adj--ctl"></a>zeroOp: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

일 때 적용할 단일 작업 `result == Zero` 입니다.


### <a name="zeroinput--t"></a>zeroInput: ' '

때 제공 되는 입력입니다 `zeroOp` `result == Zero` .


### <a name="oneop--u--unit--is-adj--ctl"></a>oneOp: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

일 때 적용할 단일 작업 `result == One` 입니다.


### <a name="oneinput--u"></a>oneInput: ' U

때 제공 되는 입력입니다 `oneOp` `result == One` .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

조건부로 적용할 작업의 입력 형식 `zeroOp` 입니다.
### <a name="u"></a>' U

조건부로 적용할 작업의 입력 형식 `oneOp` 입니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyIfZero](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [Microsoft. 양자. ApplyIfOne](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [Microsoft. 양자. ApplyIfElseRC](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [Microsoft. 양자. ApplyIfElseRA](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [Microsoft. 양자. ApplyIfElseRCA](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)