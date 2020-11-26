---
uid: Microsoft.Quantum.Canon.ApproximateQFT
title: ApproximateQFT 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximateQFT
qsharp.summary: Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.
ms.openlocfilehash: 97a410133e80cc5bffc810e9d6455baaee32364b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207703"
---
# <a name="approximateqft-operation"></a>ApproximateQFT 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


퀀텀 레지스터에 AQFT (대략적인 퀀텀 푸리에 변환)을 적용 합니다.

```qsharp
operation ApproximateQFT (a : Int, qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="a--int"></a>a: [Int](xref:microsoft.quantum.lang-ref.int)

QFT 회로에서 발생 하는 제어 된 Z 회전이 정리 되는 수준을 결정 하는 근사값 매개 변수입니다.

근사값 매개 변수 a는 Z 회전의 정리 수준을 결정 합니다. 즉, ∈ {0. n}과 (와) 모든 Z 회전 2π/2k를 결정 합니다. 여기서 k>a는 QFT 회로에서 제거 됩니다. K >= log ₂ (n) + log ₂ (1/ε) + 3을 바인딩할 수 있는 것으로 알려져 있습니다. | | QFT-AQFT | | Ε를<합니다.


### <a name="qs--bigendian"></a>qs:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian)

대략적인 퀀텀 푸리에 변환이 적용 되는 n 개의 퀀텀 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

AQFT에는 2π/2k 및 Hadamard 게이트 형식의 Z-회전 게이트가 필요 합니다.

입력 및 출력은 big endian 인코딩으로 인코딩된 것으로 간주 됩니다.

## <a name="references"></a>참조 항목

- [대 수 Eng. Commun에 대 한 자세한 *내용은* 입니다. 컴퓨터. 19 (3): 177-193 (2008)](http://doi.org/10.1007/s00200-008-0072-2)
- [*D. Coppersmith* arxiv:/0201067v1](https://arxiv.org/abs/quant-ph/0201067)