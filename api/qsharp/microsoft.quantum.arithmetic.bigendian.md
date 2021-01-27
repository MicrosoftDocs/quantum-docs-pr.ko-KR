---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: 이상 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 2f6ec9f83ac124ce9b06c278f8fda820c35c23aa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843388"
---
# <a name="bigendian-user-defined-type"></a>이상 사용자 정의 형식

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


부호 없는 정수를 빅 endian 순서로 인코딩하는 레지스터입니다. 인덱스를 사용 하는가 중 비트는 `0` 부호 없는 정수의 상위 비트를 인코딩합니다.

```qsharp

newtype BigEndian = (Qubit[]);
```



## <a name="remarks"></a>설명

`BigEndian`설명서에서와 같이 축약 `BE` 됩니다.