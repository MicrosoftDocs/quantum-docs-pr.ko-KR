---
uid: Microsoft.Quantum.Math.ExpModL
title: ExpModL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 73d434bd364847b4e5e06d1a9f460424e0c50850
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723728"
---
# <a name="expmodl-function"></a>ExpModL 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)

패키지 [](https://nuget.org/packages/)


지정 된 모듈러스와 관련 하 여 지정 된 지 수 만큼 거듭제곱 한 정수를 반환 합니다.

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a>Description

$X $, power by $p $ 및 모듈러스를 $N $로 하 여이를 기반으로 하는 것을 나타낼 수 있습니다.
함수는 $x ^ p \operatorname{mod} N $을 반환 합니다.

$N $, $x $는 양수가 고 전원은 음수가 아닌 것으로 가정 합니다.

## <a name="input"></a>입력

### <a name="expbase--bigint"></a>기본: [BigInt](xref:microsoft.quantum.lang-ref.bigint)




### <a name="power--bigint"></a>power: [BigInt](xref:microsoft.quantum.lang-ref.bigint)




### <a name="modulus--bigint"></a>모듈러스: [BigInt](xref:microsoft.quantum.lang-ref.bigint)





## <a name="output--bigint"></a>출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)



## <a name="remarks"></a>설명

는 자체가 아닌의 비트 수에 비례하여 시간을 사용 `power` `power` 합니다.