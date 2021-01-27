---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBE
title: ReversedOpBE 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBE
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 878b0fae8a803b3136d1537309c945c052e1052c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846477"
---
# <a name="reversedopbe-function"></a>ReversedOpBE 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


빅 endian 입력을 사용 하는 작업의 경우는 작은 endian 입력을 사용 하는 새 작업을 반환 합니다.

```qsharp
function ReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)
```


## <a name="input"></a>입력

### <a name="op--bigendian--unit"></a>op:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [단위](xref:microsoft.quantum.lang-ref.unit) 

입력이 반전 될 작업입니다.



## <a name="output--littleendian--unit"></a>출력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) 

입력을 작은 endian 레지스터로 허용 하는 새 작업입니다.

## <a name="see-also"></a>참고 항목

- [ApplyReversedOpBE.](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [ReversedOpBEA.](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [ReversedOpBEC.](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [ReversedOpBECA.](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)