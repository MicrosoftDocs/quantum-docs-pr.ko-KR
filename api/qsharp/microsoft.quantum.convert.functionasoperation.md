---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: FunctionAsOperation 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: 90e9f0c922a77fbb6d6faf8945d4f5d1c8ff33b7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713511"
---
# <a name="functionasoperation-function"></a>FunctionAsOperation 함수

네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)

패키지 [](https://nuget.org/packages/)


함수를 작업으로 변환 합니다.

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a>Description

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