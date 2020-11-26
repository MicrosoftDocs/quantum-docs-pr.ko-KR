---
uid: Microsoft.Quantum.Canon.QFT
title: QFT 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFT
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: 8f1aa8c3680a068e500503ca25afa9a49e4ef5bf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205541"
---
# <a name="qft-operation"></a>QFT 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


빅 endian 표현의 정수를 포함 하는 퀀텀 레지스터에서 퀀텀 푸리에 변환을 수행 합니다.

```qsharp
operation QFT (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="qs--bigendian"></a>qs:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian)

퀀텀 푸리에 변환이 적용 되는 퀀텀 레지스터



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

입력 및 출력은 big endian 인코딩에 있는 것으로 간주 됩니다.

## <a name="see-also"></a>참고 항목

- [ApplyQuantumFourierTransformBE입니다.](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)