---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: FastHadamardTransformed 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: 3e48701f22ddf154721355866e15a85fca0bc7df
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203096"
---
# <a name="fasthadamardtransformed-function"></a>FastHadamardTransformed 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


{-1,1}Yates의 메서드를 사용 하 여 인코딩의 부울 함수 변환의 변환을 계산 합니다.

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a>입력

### <a name="func--int"></a>func: [Int](xref:microsoft.quantum.lang-ref.int)[]

{-1,1}인코딩의 테이블



## <a name="output--int"></a>Output: [Int](xref:microsoft.quantum.lang-ref.int)[]

함수의 Spectral 계수