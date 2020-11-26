---
uid: Microsoft.Quantum.Synthesis.Encoded
title: 인코딩된 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 803f35b9e7af547bc34f21de74684fba885bfda9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203181"
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