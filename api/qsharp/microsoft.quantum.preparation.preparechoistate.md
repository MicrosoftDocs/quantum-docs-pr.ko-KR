---
uid: Microsoft.Quantum.Preparation.PrepareChoiState
title: PrepareChoiState 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiState
qsharp.summary: Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.
ms.openlocfilehash: cb34078c09f8c28b5b9bbda1bae6936d13ffcc78
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854396"
---
# <a name="preparechoistate-operation"></a>PrepareChoiState 작업

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 작업에 대 한 Choi – Jamiołkowski 상태를 지정 된 참조 및 대상 레지스터로 준비 합니다.

```qsharp
operation PrepareChoiState (op : (Qubit[] => Unit), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a>입력

### <a name="op--qubit--unit"></a>op:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit) 

작업 $ \Lambda $ Choi – Jamiołkowski state $J (\Lambda)/2 ^ N $를 준비할 수 있습니다. 여기서 $N $은가 작동 하는가 중 비트 수입니다 `op` .


### <a name="reference--qubit"></a>참조:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[]

의 동작에 대 한 참조로 사용 되는 $ \ket{00\cdots 0} $ 상태에서 시작 하는 비트의 레지스터입니다 `op` .


### <a name="target--qubit"></a>target: [](xref:microsoft.quantum.lang-ref.qubit)

처음에이 적용 될 $ \ket{00\cdots 0} $ 상태에 있는 나머지 비트의 레지스터입니다 `op` .



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

퀀텀 프로세스의 Choi – Jamiłkowski state $J (\Lambda) $는 $ $ \begin{align} J (\Lambda) \mathrel{: =} (\boldone \otimes \Lambda) (| \boldone\rangle \! \rangle\langle \! \langle\boldone |), \end{align} $ $ where $ |로 정의 됩니다. X\rangle \! \rangle $는 열 스택 규칙에서 행렬 $X $의 *벡터화* 입니다. 이 상태에 대 한 기존 설명 학습은 임의의 입력 상태에서 수행 되는 $ \Lambda $의 효과에 대 한 전체 정보를 제공 하 고, *퀀텀 프로세스 tomography* 의 토대를 형성 합니다.

## <a name="see-also"></a>참고 항목

- [PrepareChoiStateA.](xref:Microsoft.Quantum.Preparation.PrepareChoiStateA)
- [PrepareChoiStateC.](xref:Microsoft.Quantum.Preparation.PrepareChoiStateC)
- [PrepareChoiStateCA.](xref:Microsoft.Quantum.Preparation.PrepareChoiStateCA)