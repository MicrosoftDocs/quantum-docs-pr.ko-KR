---
uid: Microsoft.Quantum.Canon.TransformedOperationCA
title: TransformedOperationCA 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationCA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: bb39530ae28e17d07a6a5c2bb2d35f81be312d15
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840117"
---
# <a name="transformedoperationca-function"></a>TransformedOperationCA 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


함수 및 작업이 지정 된 경우 지정 된 함수가 입력을 변환 하는 새 작업을 반환 합니다.

```qsharp
function TransformedOperationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl)) : ('U => Unit is Adj + Ctl)
```


## <a name="input"></a>입력

### <a name="fn--u---t"></a>fn: ' U-> '

지정 된 입력을 작업에서 예상 하는 형식으로 변환 하는 함수입니다.


### <a name="op--t--unit--is-adj--ctl"></a>op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

변형할 작업입니다.



## <a name="output--u--unit--is-adj--ctl"></a>출력: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

Tbat는 입력을 사용 하 여를 호출 하 `fn` 고 결과 출력을에 전달 `op` 합니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다


### <a name="u"></a>' U



## <a name="example"></a>예

다음 호출에서는를 사용 하 여 입력 @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" 용으로 설계 된 작업을 @"Microsoft.Quantum.Arithmetic.BigEndian" 형식의 입력을 허용 하는 작업으로 변환 합니다 @"Microsoft.Quantum.Arithmetic.LittleEndian" .

```qsharp
let leOp = TransformedOperation(LittleEndianAsBigEndian, ApplyXorInPlaceBE);
```

## <a name="see-also"></a>참고 항목

- [TransformedOperation입니다.](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [TransformedOperationA입니다.](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [TransformedOperationCA입니다.](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [Microsoft. 양자. ApplyWithInputTransformation](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [Microsoft. 양자 구성](xref:Microsoft.Quantum.Canon.Composed)