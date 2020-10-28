---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: ApplyFermionicSWAP 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 25dd91b200700d1474cf27bf1d0fa71d57f2e09b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718273"
---
# <a name="applyfermionicswap-operation"></a>ApplyFermionicSWAP 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


Fermionic SWAP을 적용 합니다.

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit
```


## <a name="description"></a>Description

이렇게 하면 기본적으로-1의 글로벌 단계를 적용 하는 동안 두 번째 비트는 모두 1이 됩니다. Orbitals의 symmetrization을 유지 합니다.
자세한 내용은  항목을 참조하세요.

이 작업은 단일 연산자 \begin{align} f_ {swap} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 0 & 1 & 0 & 0 0 & 0 & 0 \\ \\ \\ \\ &-1 \\ \\ \end{bmatrix}.에 의해 표시 됩니다.
\end{align}

## <a name="input"></a>입력

### <a name="qubit1--qubit"></a>qubit1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

교환할 첫 번째 비트입니다.


### <a name="qubit2--qubit"></a>qubit2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

스왑할 두 번째 비트입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>참조

- [*Ryan Babbush, 네, Wiebe, Jarrod McClean, James McClain, Hartmut Neven, Garnet Kin-Lic 변경 (* , arxiv: 1706.00023](https://arxiv.org/pdf/1706.00023.pdf)

## <a name="see-also"></a>참고 항목

- [Microsoft.](xref:Microsoft.Quantum.Intrinsic.SWAP)