---
uid: Microsoft.Quantum.Math.InverseModI
title: InverseModI 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModI
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 6efc9da5f5ebb64065a90e749daa629dc2dce9cf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723637"
---
# <a name="inversemodi-function"></a>InverseModI 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지 [](https://nuget.org/packages/)


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