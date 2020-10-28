---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: PrepareIdentity 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: a3f96fbdafb19c90fb2b563243600cca60841566
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724890"
---
# <a name="prepareidentity-operation"></a>PrepareIdentity 작업

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지 [](https://nuget.org/packages/)


레지스터가 지정 된 경우 최대 혼합 상태에서 등록을 준비 합니다.

레지스터는 각 \boldone에 전체 depolarizing 채널을 적용 하 여 $/2 ^ N $ 상태에서 준비 됩니다. 여기서 $N $은 레지스터의 길이입니다.

```qsharp
operation PrepareIdentity (register : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="register--qubit"></a>register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

위에서 설명한 방식으로 해당 상태가 depolarized 인 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>참고 항목

- [PrepareSingleQubitIdentity.](xref:Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity)