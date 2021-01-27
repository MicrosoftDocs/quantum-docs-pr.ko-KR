---
uid: Microsoft.Quantum.Convert.Call
title: 작업 호출
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 93458d08aa83ffa8b7b33de8bf51c970af291db9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850203"
---
# <a name="call-operation"></a>작업 호출

네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 입력을 사용 하 여 함수를 호출 합니다.

```qsharp
operation Call<'Input, 'Output> (fn : ('Input -> 'Output), input : 'Input) : 'Output
```


## <a name="description"></a>설명

함수 및이 함수에 대 한 입력이 지정 되 면는 함수를 호출 하 고 해당 출력을 반환 합니다.

## <a name="input"></a>입력

### <a name="fn--input---output"></a>fn: ' 입력 > ' 출력

호출할 함수입니다.


### <a name="input--input"></a>입력: ' 입력

함수에 전달 되는 입력입니다.



## <a name="output--output"></a>출력: ' 출력

호출하는 `fn`의 결과입니다.

## <a name="type-parameters"></a>형식 매개 변수

### <a name="input"></a>' 입력


### <a name="output"></a>' 출력



## <a name="remarks"></a>설명

이 작업은 작업 내의 특정 위치에서 함수를 강제로 호출 하거나 작업이 필요한 함수를 호출 하는 데 주로 유용 합니다.