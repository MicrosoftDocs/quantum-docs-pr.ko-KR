---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLE
title: ReversedOpLE 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLE
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: d02817e5372b841f3ab633cafa22af603c5310c2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846389"
---
# <a name="reversedople-function"></a>ReversedOpLE 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


는 작은 endian 입력을 사용 하는 작업에 대해 빅 endian 입력을 사용 하는 새 작업을 반환 합니다.

```qsharp
function ReversedOpLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)
```


## <a name="input"></a>입력

### <a name="op--littleendian--unit"></a>op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) 

입력이 반전 될 작업입니다.



## <a name="output--bigendian--unit"></a>출력:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [단위](xref:microsoft.quantum.lang-ref.unit) 

입력을 빅 endian 레지스터로 허용 하는 새 작업입니다.

## <a name="see-also"></a>참고 항목

- [ApplyReversedOpLE.](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [ReversedOpLEA.](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [ReversedOpLEC.](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [ReversedOpLECA.](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)