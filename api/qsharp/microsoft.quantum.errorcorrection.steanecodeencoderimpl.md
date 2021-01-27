---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: SteaneCodeEncoderImpl 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: 81abe75e2a315fe9a994147242f3c8c9bde586ed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824729"
---
# <a name="steanecodeencoderimpl-operation"></a>SteaneCodeEncoderImpl 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Steane 코드 인코더와 디코더를 모두 구현 하는 데 사용 되는 개인 작업입니다.

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a>입력

### <a name="data--qubit"></a>data: [bit](xref:microsoft.quantum.lang-ref.qubit)[]

입력의 비트를 포함 하는 1 개의 비트를 포함 하는 배열입니다.


### <a name="scratch--qubit"></a>스크래치: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

중복성을 추가 하는 6 개의 비트를 포함 하는 배열입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

