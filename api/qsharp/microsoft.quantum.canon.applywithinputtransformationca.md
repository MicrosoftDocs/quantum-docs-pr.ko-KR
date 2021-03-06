---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationCA
title: ApplyWithInputTransformationCA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationCA
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: b31ed1b3da0d5467588f4cb2e4368e68f0dbe9d5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841108"
---
# <a name="applywithinputtransformationca-operation"></a>ApplyWithInputTransformationCA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


일부 입력을 허용 하는 작업, 해당 작업과 호환 되는 출력을 반환 하는 함수 및이 함수에 대 한 입력을 제공 하는 경우 함수를 사용 하 여 작업에 필요한 형식으로 입력을 변환 하는 작업을 적용 합니다.

```qsharp
operation ApplyWithInputTransformationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl), input : 'U) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="fn--u---t"></a>fn: ' U-> '

지정 된 입력을 작업에서 예상 하는 형식으로 변환 하는 함수입니다.


### <a name="op--t--unit--is-adj--ctl"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

적용 될 작업입니다.


### <a name="input--u"></a>입력: ' U

함수에 대 한 입력입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다


### <a name="u"></a>' U



## <a name="example"></a>예

다음 호출에서는를 사용 하 여 @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" 형식의 입력에 대 한 입력 용으로 설계 된 작업을 적용 합니다 @"Microsoft.Quantum.Arithmetic.BigEndian" @"Microsoft.Quantum.Arithmetic.LittleEndian" .

```qsharp
ApplyWithInputTransformation(LittleEndianAsBigEndian, ApplyXorInPlaceBE, LittleEndian(qubits));
```

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. ApplyWithInputTransformation](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [ApplyWithInputTransformationA입니다.](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [ApplyWithInputTransformationC입니다.](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [TransformedOperation입니다.](xref:Microsoft.Quantum.Canon.TransformedOperation)