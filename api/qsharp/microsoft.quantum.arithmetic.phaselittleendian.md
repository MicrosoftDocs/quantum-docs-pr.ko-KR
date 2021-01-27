---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: PhaseLittleEndian 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: 59df1db31090f875ccd261fe6cc43995ba57b963
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842994"
---
# <a name="phaselittleendian-user-defined-type"></a>PhaseLittleEndian 사용자 정의 형식

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


QFT 기반의 작은 endian 부호 없는 정수입니다.

예를 들어 $ \ket{x} $가 계산을 기준으로 하는 정수 $x $의 작은 endian 인코딩이 면 $ \operatorname{QFTLE} \ket{x} $는 QFT의 $x $의 인코딩입니다.

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a>설명

`PhaseLittleEndian`설명서에서와 같이 축약 `PhaseLE` 됩니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. QFT](xref:Microsoft.Quantum.Canon.QFT)
- [QFTLE입니다.](xref:Microsoft.Quantum.Canon.QFTLE)