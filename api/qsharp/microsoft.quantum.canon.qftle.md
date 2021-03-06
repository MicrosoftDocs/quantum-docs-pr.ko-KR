---
uid: Microsoft.Quantum.Canon.QFTLE
title: QFTLE 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFTLE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: 893366833e5bd6b358884c11f4534609efd72d24
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852271"
---
# <a name="qftle-operation"></a>QFTLE 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


작은 endian 표현의 정수를 포함 하는 퀀텀 레지스터에서 퀀텀 푸리에 변환을 수행 합니다.

```qsharp
operation QFTLE (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="qs--littleendian"></a>qs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

퀀텀 푸리에 변환이 적용 되는 퀀텀 레지스터



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

입력 및 출력은 little endian 인코딩에 있는 것으로 간주 됩니다.

## <a name="see-also"></a>참고 항목

- [Microsoft. 양자. QFT](xref:Microsoft.Quantum.Canon.QFT)