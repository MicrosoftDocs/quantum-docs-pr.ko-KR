---
uid: Microsoft.Quantum.Canon.ComposedOutput
title: ComposedOutput 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ComposedOutput
qsharp.summary: Returns the output of the composition of `inner` and `outer` for a given input.
ms.openlocfilehash: d39fcd6b2987b3a4f69df13fa83b69a199d6eddb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840882"
---
# <a name="composedoutput-function"></a>ComposedOutput 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


`inner`지정 된 입력에 대해 및의 컴퍼지션 출력을 반환 합니다 `outer` .

```qsharp
function ComposedOutput<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U), target : 'T) : 'V
```


## <a name="input"></a>입력

### <a name="outer--u---v"></a>외부: ' U-> ' V




### <a name="inner--t---u"></a>inner: ' t-> ' U




### <a name="target--t"></a>대상: ' '





## <a name="output--v"></a>출력: ' V



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다


### <a name="u"></a>' U


### <a name="v"></a>' V

