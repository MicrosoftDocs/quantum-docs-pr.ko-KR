---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: 이상 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 64590606f7c36e0598a9d29c5c6a7ba6d6451aa1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721357"
---
# <a name="bigendian-user-defined-type"></a>이상 사용자 정의 형식

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지 [](https://nuget.org/packages/)


부호 없는 정수를 빅 endian 순서로 인코딩하는 레지스터입니다. 인덱스를 사용 하는가 중 비트는 `0` 부호 없는 정수의 상위 비트를 인코딩합니다.

```qsharp

newtype BigEndian = (Qubit[]);
```



## <a name="remarks"></a>설명

`BigEndian`설명서에서와 같이 축약 `BE` 됩니다.