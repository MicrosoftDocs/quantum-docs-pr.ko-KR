---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: FastHadamardTransformed 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: be54413ef2d3fdaf7ddc726bc0906adb4ec382ff
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855464"
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

## <a name="example"></a>예제

```qsharp
FastHadamardTransformed([1, 1, 1, -1]); // [2, 2, 2, -2]
```