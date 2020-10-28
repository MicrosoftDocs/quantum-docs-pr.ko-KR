---
uid: Microsoft.Quantum.Math.InverseModL
title: InverseModL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModL
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: e7cb9e98cb0635c50162611f6a52c56027d4a5eb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723630"
---
# <a name="inversemodl-function"></a>InverseModL 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지 [](https://nuget.org/packages/)


$A \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $과 같은 $b $를 반환 합니다.

```qsharp
function InverseModL (a : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a>입력

### <a name="a--bigint"></a>a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

반전 되는 숫자입니다.


### <a name="modulus--bigint"></a>모듈러스: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

숫자의 반전에 따른 모듈러스입니다.



## <a name="output--bigint"></a>출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

정수 $b $ $a \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $입니다.