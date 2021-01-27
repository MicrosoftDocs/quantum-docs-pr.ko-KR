---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLEC
title: ReversedOpLEC 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLEC
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: 2dc6a596970f909af9c329dbe7002c165854cfec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846373"
---
# <a name="reversedoplec-function"></a>ReversedOpLEC 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


는 작은 endian 입력을 사용 하는 작업에 대해 빅 endian 입력을 사용 하는 새 작업을 반환 합니다.

```qsharp
function ReversedOpLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)
```


## <a name="input"></a>입력

### <a name="op--littleendian--unit--is-ctl"></a>op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.

입력이 반전 될 작업입니다.



## <a name="output--bigendian--unit--is-ctl"></a>출력:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [단위가](xref:microsoft.quantum.lang-ref.unit)  Ctl입니다.

입력을 빅 endian 레지스터로 허용 하는 새 작업입니다.

## <a name="see-also"></a>참고 항목

- [ApplyReversedOpLEC.](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [ReversedOpLE.](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [ReversedOpLEA.](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [ReversedOpLECA.](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)