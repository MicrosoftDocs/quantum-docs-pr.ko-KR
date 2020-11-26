---
uid: Microsoft.Quantum.Diagnostics.DumpRegister
title: DumpRegister 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpRegister
qsharp.summary: Dumps the current target machine's status associated with the given qubits.
ms.openlocfilehash: 9623d6d881f1f0ec048c3a951fe259bdfac84766
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202025"
---
# <a name="dumpregister-function"></a>DumpRegister 함수

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


지정 된 비트와 연결 된 현재 대상 컴퓨터의 상태를 덤프 합니다.

```qsharp
function DumpRegister<'T> (location : 'T, qubits : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="location--t"></a>위치: ' '

상태 덤프를 생성할 위치에 대 한 정보를 제공 합니다.


### <a name="qubits--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

보고할 비트 목록입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

없음

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="remarks"></a>설명

이 메서드를 사용 하면 지정 된 비트의 상태와 연결 된 정보를 파일 또는 다른 위치에 덤프할 수 있습니다.
의 실제 정보 및 의미 체계는 `location` 각 대상 컴퓨터에만 적용 됩니다. 그러나 빈 튜플을 위치 ()로 제공 하면 `()` 일반적으로 콘솔에 대 한 출력을 생성 하는 것을 의미 합니다.

퀀텀 개발 키트의 일부로 분산 된 로컬 전체 상태 시뮬레이터의 경우이 메서드는 지정 된 요소 (즉, 해당 하위 시스템의 wave 함수)의 상태를 해당 상태를 측정할 확률의 amplitudes을 나타내는 복소수의 1 차원 배열로 기록 하는 파일에 대 한 경로가 포함 된 문자열을 예상 합니다.
지정 된 비트를 다른 몇 가지 다른 것으로 지정 하 고 해당 상태를 분리할 수 없는 경우,이는 해당 하는 것을 보고 합니다.