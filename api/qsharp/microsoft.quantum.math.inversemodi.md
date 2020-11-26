---
uid: Microsoft.Quantum.Math.InverseModI
title: InverseModI 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModI
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 217ce4cd113ecbc6a06ed83c6c1dcb7baa46387d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195378"
---
# <a name="inversemodi-function"></a>InverseModI 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


$A \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $과 같은 $b $를 반환 합니다.

```qsharp
function InverseModI (a : Int, modulus : Int) : Int
```


## <a name="input"></a>입력

### <a name="a--int"></a>a: [Int](xref:microsoft.quantum.lang-ref.int)

반전 되는 숫자입니다.


### <a name="modulus--int"></a>모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)

숫자의 반전에 따른 모듈러스입니다.



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

정수 $b $ $a \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $입니다.