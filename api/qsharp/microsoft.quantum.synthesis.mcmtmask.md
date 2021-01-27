---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: MCMTMask 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 50bec0f9aca95afab83491db6b742d1f0323371f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855368"
---
# <a name="mcmtmask-user-defined-type"></a>MCMTMask 사용자 정의 형식

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


다중 제어 되는 여러 대상 Toffoli gate를 나타내는 형식입니다.

첫 번째 정수는 컨트롤 줄의 비트 마스크입니다.  설정 되는 비트 인덱스는 줄 인덱스 제어에 해당 합니다.

두 번째 정수는 대상 줄의 비트 마스크입니다.  설정 되는 비트 인덱스는 대상 줄 인덱스에 해당 합니다.

두 정수의 비트 인덱스는 분리 되어야 합니다.

```qsharp

newtype MCMTMask = (ControlMask : Int, TargetMask : Int);
```



## <a name="named-items"></a>명명 된 항목

### <a name="controlmask--int"></a>ControlMask: [Int](xref:microsoft.quantum.lang-ref.int)


### <a name="targetmask--int"></a>TargetMask: [Int](xref:microsoft.quantum.lang-ref.int)

