---
uid: Microsoft.Quantum.Math.ExpModI
title: 예기치 않은 Modi 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: e31273702a9850d0162f160ca412ff6d50f38b28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723364"
---
# <a name="expmodi-function"></a>예기치 않은 Modi 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지 [](https://nuget.org/packages/)


지정 된 모듈러스와 관련 하 여 지정 된 지 수 만큼 거듭제곱 한 정수를 반환 합니다.

```qsharp
function ExpModI (expBase : Int, power : Int, modulus : Int) : Int
```


## <a name="description"></a>Description

$X $, power by $p $ 및 모듈러스를 $N $로 하 여이를 기반으로 하는 것을 나타낼 수 있습니다.
함수는 $x ^ p \operatorname{mod} N $을 반환 합니다.

$N $, $x $는 양수가 고 전원은 음수가 아닌 것으로 가정 합니다.

## <a name="input"></a>입력

### <a name="expbase--int"></a>기본: [Int](xref:microsoft.quantum.lang-ref.int)




### <a name="power--int"></a>power: [Int](xref:microsoft.quantum.lang-ref.int)




### <a name="modulus--int"></a>모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)



## <a name="remarks"></a>설명

는 자체가 아닌의 비트 수에 비례하여 시간을 사용 `power` `power` 합니다.