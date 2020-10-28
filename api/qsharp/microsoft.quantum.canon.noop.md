---
uid: Microsoft.Quantum.Canon.NoOp
title: NoOp 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: NoOp
qsharp.summary: Performs the identity operation (no-op) on an argument.
ms.openlocfilehash: 987e39577c3b736418234431ed7a915ae461f763
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715758"
---
# <a name="noop-operation"></a>NoOp 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


인수에 대해 id 연산 (no op)을 수행 합니다.

```qsharp
operation NoOp<'T> (input : 'T) : Unit
```


## <a name="description"></a>Description

이 작업은 모든 형식의 값을 사용 하 고 아무 것도 수행 하지 않습니다.
이는 작업 형식의 입력이 예상 될 때마다 유용할 수 있지만 아무 동작도 수행 하지 않아야 합니다.
예를 들어 특정 오류 수정 증후군에서 오류가 발생 하지 않았음을 나타내는 경우는 `NoOp<Qubit[]>` 올바른 복구 프로시저일 수 있습니다.
마찬가지로 작업에서 상태 준비 절차를 입력으로 예상 하는 경우에 `NoOp<Qubit[]>` 는 $ \ket{0 \cst0} $ 상태를 준비 하는 데 사용할 수 있습니다.

## <a name="input"></a>입력

### <a name="input--t"></a>입력: ' '

무시할 값입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="remarks"></a>설명

거의 모든 경우에 대 한 형식 매개 변수를 `NoOp` 명시적으로 지정 해야 합니다. 예를 들어 `NoOp<Qubit>` 은와 동일 <xref:microsoft.quantum.intrinsic.i> 합니다.

## <a name="see-also"></a>참고 항목

- [Microsoft 양자](xref:Microsoft.Quantum.Intrinsic.I)