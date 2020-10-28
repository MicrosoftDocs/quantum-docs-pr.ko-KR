---
uid: Microsoft.Quantum.Math.IsCoprimeI
title: IsCoprimeI 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeI
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: bdfaecb61f56967e21bf85ba190638b43685214d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723357"
---
# <a name="iscoprimei-function"></a>IsCoprimeI 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지 [](https://nuget.org/packages/)


$A $ 및 $b $가 같은 경우 true를 반환 하 고 그렇지 않으면 false를 반환 합니다.

```qsharp
function IsCoprimeI (a : Int, b : Int) : Bool
```


## <a name="input"></a>입력

### <a name="a--int"></a>a: [Int](xref:microsoft.quantum.lang-ref.int)

공동 primality을 테스트 하는 첫 번째 숫자입니다.


### <a name="b--int"></a>b: [Int](xref:microsoft.quantum.lang-ref.int)

공동 primality을 테스트 하는 두 번째 숫자입니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

$A $ 및 $b $가 같은 경우 (예: 최대 공약수가 1 임) True이 고, 그렇지 않으면 false입니다.