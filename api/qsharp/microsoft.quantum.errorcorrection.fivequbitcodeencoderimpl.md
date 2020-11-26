---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoderImpl
title: FiveQubitCodeEncoderImpl 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeEncoderImpl
qsharp.summary: Private operation used to implement both the 5 qubit encoder and decoder.
ms.openlocfilehash: f70d2d1352c7b2eebee7a863eba97d78d7351dab
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200852"
---
# <a name="fivequbitcodeencoderimpl-operation"></a>FiveQubitCodeEncoderImpl 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


5 비트 인코더와 디코더를 모두 구현 하는 데 사용 되는 개인 작업입니다.

```qsharp
operation FiveQubitCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a>입력

### <a name="data--qubit"></a>data: [bit](xref:microsoft.quantum.lang-ref.qubit)[]

입력의 비트를 포함 하는 1 개의 비트를 포함 하는 배열입니다.


### <a name="scratch--qubit"></a>스크래치: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

중복성을 추가 하는 4 개의 비트를 포함 하는 배열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

선택한 특정 인코더는 Kliuchnikov 및 D. Maslov, "Clifford 회로의 최적화", 88 Phys, 052307 (2013);에서 가져온 것입니다. https://arxiv.org/abs/1305.0810, 그림 4b)를 사용 하는 경우 총 11 개의 게이트가 필요 합니다.