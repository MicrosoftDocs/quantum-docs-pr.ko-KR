---
uid: Microsoft.Quantum.Synthesis.Encoded
title: 인코딩된 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 44f6b247e6bfab7b55c46146cb63f8b6d219955b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855492"
---
# <a name="encoded-function"></a>인코딩된 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


코딩에서 참 테이블 인코딩 {1,-1}

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a>입력

### <a name="table--bool"></a>테이블: [Bool](xref:microsoft.quantum.lang-ref.bool)[]

참 테이블을 실제 값 배열로



## <a name="output--int"></a>Output: [Int](xref:microsoft.quantum.lang-ref.int)[]

정수 배열로 서의 참 테이블 {1,-1}

## <a name="example"></a>예제

```qsharp
Encoded([false, false, false, true]); // [1, 1, 1, -1]
```