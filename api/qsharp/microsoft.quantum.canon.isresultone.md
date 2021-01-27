---
uid: Microsoft.Quantum.Canon.IsResultOne
title: IsResultOne 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IsResultOne
qsharp.summary: Tests if a given Result value is equal to `One`.
ms.openlocfilehash: f259c21e6cc0a4886332e9ffcb546e527ec7def1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840322"
---
# <a name="isresultone-function"></a>IsResultOne 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 결과 값이와 같은지 테스트 `One` 합니다.

```qsharp
function IsResultOne (input : Result) : Bool
```


## <a name="input"></a>입력

### <a name="input--__invalidresult__"></a>입력: __잘못 <Result> 됨__

`Result` 테스트할 값입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

`true` `input` 가와 같으면를 반환 `One` 합니다.