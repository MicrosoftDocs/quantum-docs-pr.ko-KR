---
uid: Microsoft.Quantum.Arithmetic.LittleEndian
title: LittleEndian 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: LittleEndian
qsharp.summary: Register that encodes an unsigned integer in little-endian order. The qubit with index `0` encodes the lowest bit of an unsigned integer.
ms.openlocfilehash: 12bc4dbf830e426365545826575d66a9683cb694
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846557"
---
# <a name="littleendian-user-defined-type"></a>LittleEndian 사용자 정의 형식

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


부호 없는 정수를 거의 endian 순서로 인코딩하는 레지스터입니다. 인덱스가 있는 이상 비트는 `0` 부호 없는 정수의 최하위 비트를 인코딩합니다.

```qsharp

newtype LittleEndian = (Qubit[]);
```



## <a name="remarks"></a>설명

`LittleEndian`설명서에서와 같이 축약 `LE` 됩니다.