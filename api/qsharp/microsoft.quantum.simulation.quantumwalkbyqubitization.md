---
uid: Microsoft.Quantum.Simulation.QuantumWalkByQubitization
title: QuantumWalkByQubitization 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: QuantumWalkByQubitization
qsharp.summary: Converts a block-encoding reflection into a quantum walk.
ms.openlocfilehash: 8ffb6eb77a3f910d3064c4a3c90215d5d9a694aa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851047"
---
# <a name="quantumwalkbyqubitization-function"></a>QuantumWalkByQubitization 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


블록 인코딩 리플렉션을 퀀텀 탐색으로 변환 합니다.

```qsharp
function QuantumWalkByQubitization (blockEncoding : Microsoft.Quantum.Simulation.BlockEncodingReflection) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="description"></a>설명

특정 연산자를 대상으로 하 `BlockEncodingReflection` 는 일부 $H 연산자를 인코딩하는 단일 $U $로 표시 된는 $ \pm e ^ {\pm i\sin ^ {-1} (H)} $의 스펙트럼을 포함 하는 퀀텀 워크 $W $로 변환 합니다.

## <a name="input"></a>입력

### <a name="blockencoding--blockencodingreflection"></a>blockEncoding: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

`BlockEncodingReflection`퀀텀 탐색으로 변환할 단일 $U $입니다.



## <a name="output--qubitqubit--unit--is-adj--ctl"></a>Output: (추가[비트](xref:microsoft.quantum.lang-ref.qubit)[[], [](xref:microsoft.quantum.lang-ref.qubit)]) => [Unit](xref:microsoft.quantum.lang-ref.unit) is Adj + Ctl

퀀텀 탐색 $W $는 레지스터를 공동으로 수행 하 `a` 고 `s` $H $를 차단 하며 $ \pm e ^ {\pm i\sin ^ {-1} (H)} $의 스펙트럼을 포함 합니다.

## <a name="references"></a>참조

- Hamiltonian 시뮬레이션의 Guang Jia-hao Low, Isaac Chuang https://arxiv.org/abs/1610.06546

## <a name="see-also"></a>참고 항목

- [Microsoft 양자. 블록 인코딩](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [BlockEncodingReflection.](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)