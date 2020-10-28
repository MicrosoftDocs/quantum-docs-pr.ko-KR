---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: DumpOperation 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: 444d42e2440b30b3bdf50d55a399568bed063222
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712860"
---
# <a name="dumpoperation-operation"></a>DumpOperation 작업

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지 [](https://nuget.org/packages/)


작업을 수행 하는 경우 현재 실행 대상에서 사용할 수 있는 작업에 대 한 진단을 표시 합니다.

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>입력

### <a name="nqubits--int"></a>N Bits: [Int](xref:microsoft.quantum.lang-ref.int)

지정 된 작업이 작동 하는 값의 수입니다.


### <a name="op--qubit--unit-adj"></a>op: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)

진단할 작업입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

이 작업을 호출 하면 Q # 내에서 관찰할 영향을 주지 않습니다. 표시 되는 정확한 진단 (있는 경우)은 현재 실행 대상 및 편집기 환경에 따라 달라 집니다.
예를 들어 전체 상태 퀀텀 시뮬레이터에서 사용 되는 경우를 나타내는 데 사용 되는 단일 매트릭스가 `op` 표시 됩니다.

전역 단계 모호성을 허용 하는 시뮬레이터에서 실행 하는 경우 (예: 전체 상태 시뮬레이터) 반환 된 표현은 글로벌 단계까지 달라질 수 있습니다.

마찬가지로 행 및 열 행렬 표현의 순서 지정은이 작업을 지 원하는 각 시뮬레이터에서 사용 되는 규칙에 따라 달라질 수 있습니다.