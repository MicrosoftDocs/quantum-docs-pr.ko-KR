---
uid: Microsoft.Quantum.Diagnostics.DumpMachine
title: 로 컴퓨터 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpMachine
qsharp.summary: Dumps the current target machine's status.
ms.openlocfilehash: 579300d4efb9e22cb671fbb4bce0a6f72dd0e2ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853413"
---
# <a name="dumpmachine-function"></a>로 컴퓨터 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


현재 대상 컴퓨터의 상태를 덤프 합니다.

```qsharp
function DumpMachine<'T> (location : 'T) : Unit
```


## <a name="input"></a>입력

### <a name="location--t"></a>위치: ' '

컴퓨터의 덤프를 생성 하는 위치에 대 한 정보를 제공 합니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

없음

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="remarks"></a>설명

이 메서드를 사용 하면 대상 컴퓨터의 현재 상태에 대 한 정보를 파일 또는 다른 위치에 덤프할 수 있습니다.
의 실제 정보 및 의미 체계는 `location` 각 대상 컴퓨터에만 적용 됩니다. 그러나 빈 튜플을 위치 ()로 제공 `()` 하거나 매개 변수를 생략 하는 것은 `location` 일반적으로 콘솔에 대 한 출력을 생성 하는 것을 의미 합니다.

퀀텀 개발 키트의 일부로 분산 된 로컬 전체 상태 시뮬레이터의 경우이 메서드는 웨이브 함수를 복소수의 1 차원 배열로 기록 하는 파일에 대 한 경로가 포함 된 문자열을 예상 합니다. 여기서 각 요소는 해당 상태를 측정할 확률의 amplitudes을 나타냅니다.