---
uid: Microsoft.Quantum.Synthesis.Extended
title: 확장 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Extended
qsharp.summary: Extends a spectrum by inverted coefficients
ms.openlocfilehash: 1855f3cab98c5fbf08c4505b90423df50cbec95b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855466"
---
# <a name="extended-function"></a>확장 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


반전 계수를 기준으로 스펙트럼 확장

```qsharp
function Extended (spectrum : Int[]) : Int[]
```


## <a name="input"></a>입력

### <a name="spectrum--int"></a>스펙트럼: [Int](xref:microsoft.quantum.lang-ref.int)[]

Spectral 계수



## <a name="output--int"></a>Output: [Int](xref:microsoft.quantum.lang-ref.int)[]

계수와 반전 된 복사

## <a name="example"></a>예제

```qsharp
Extended([2, 2, 2, -2]); // [2, 2, 2, -2, -2, -2, -2, 2]
```