---
uid: Microsoft.Quantum.Canon.Angle
title: Angle 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: da3ecdaf1b2c88180bd2a660fac0b6e87b2cafa1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718489"
---
# <a name="angle-function"></a>Angle 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


에 짝수 1과-1이 있으면 1을 반환 `index` `index` 합니다.

```qsharp
function Angle (index : Int) : Int
```


## <a name="description"></a>Description

값은 회전 각도를 결정 하는 지정 된 할당에 대 한 n 변수 및 함수의 Rademacher-Walsh 스펙트럼 계수의 부호에 해당 합니다.

## <a name="input"></a>입력

### <a name="index--int"></a>인덱스: [Int](xref:microsoft.quantum.lang-ref.int)

입력 할당을 정수로 (0에서 2 ^ n-1)



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

