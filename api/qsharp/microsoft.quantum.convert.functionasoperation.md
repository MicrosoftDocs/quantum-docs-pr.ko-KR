---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: FunctionAsOperation 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: cf4f8c97bf38b3a64eb952d0a502bc21c29c579c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833832"
---
# <a name="functionasoperation-function"></a>FunctionAsOperation 함수

네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


함수를 작업으로 변환 합니다.

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a>설명

함수가 지정 된 경우 해당 함수를 호출 하 고 다른 작업은 수행 하지 않는 작업을 반환 합니다.

## <a name="input"></a>입력

### <a name="fn--input---output"></a>fn: ' 입력 > ' 출력

작업으로 변환 되는 함수입니다.



## <a name="output--input--output"></a>출력: ' Input => ' 출력 

`op` `op(input)` 모든에 대해와 동일한 작업입니다 `fn(input)` `input` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="input"></a>' 입력

변환할 함수의 입력 형식입니다.
### <a name="output"></a>' 출력

변환할 함수의 출력 형식입니다.

## <a name="remarks"></a>설명

이는 작업을 입력으로 사용할 함수 또는 작업에 함수를 전달 하는 데 주로 유용 합니다.