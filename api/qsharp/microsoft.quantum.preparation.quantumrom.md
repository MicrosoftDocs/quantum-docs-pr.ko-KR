---
uid: Microsoft.Quantum.Preparation.QuantumROM
title: QuantumROM 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROM
qsharp.summary: >-
  > [!WARNING]

  > QuantumROM has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.


  Uses the Quantum ROM technique to represent a given density matrix.

  Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$. In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$. In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}. \end{align} $$
ms.openlocfilehash: 64ed9aed7c9d9a4a689c5926f3cd085a2521c4db
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856816"
---
# <a name="quantumrom-function"></a>QuantumROM 함수

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> QuantumROM는 더 이상 사용 되지 않습니다. 대신 <xref:Microsoft.Quantum.Preparation.PurifiedMixedState>를 사용하십시오.

는 퀀텀 ROM 기술을 사용 하 여 지정 된 밀도 행렬을 나타냅니다.

$ 계수의 $ \ alpha_j $ $N 목록이 지정 된 경우,이는 \ket{j}\bra{j} 기술을 사용 하 여 밀도 행렬 $ \rho = \ p_j {j = 0} ^ {N-1} \frac{| sum_ |}의 purification에 대 한 근사치 $ \tilde\rho\ sum_ {j = 0} ^ {N-1} alpha_j $를 준비 하는 단일 $U $를 반환 합니다. {\ sum_k | \ alpha_k |} \ket{j}\bra{j} $. 이러한 근사값에서 $ \epsilon $ 오류는 $ | p_j-\frac{| alpha_j |}입니다. {\ sum_k | \ alpha_k |} | \le \le/N $ 및 $ \| \tilde\rho-\rho \| \le \te\e $를 입력 합니다. 즉, $ $ \begin{align} U\ket {0} ^ {\lceil\ log_2 N\rceil} \ k {0} ^ {m} = \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\text{garbage} _j}입니다.
\end{align} $ $

```qsharp
function QuantumROM (targetError : Double, coefficients : Double[]) : ((Int, (Int, Int)), Double, ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))
```


## <a name="input"></a>입력

### <a name="targeterror--double"></a>targetError: [Double](xref:microsoft.quantum.lang-ref.double)

$ \Epsilon $ 대상 오류입니다.


### <a name="coefficients--double"></a>계수: [Double](xref:microsoft.quantum.lang-ref.double)[]

기본 상태의 확률을 지정 하는 $N $ 계수의 배열입니다.
음수 $-\ alpha_j $는 긍정 $ | \ alpha_j | $로 처리 됩니다.



## <a name="output--intintintdoublelittleendianqubit--unit--is-adj--ctl"></a>Output: (([int](xref:microsoft.quantum.lang-ref.int), ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double), ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Adj []](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is + Ctl)

## <a name="first-parameter"></a>첫 번째 매개 변수

`(x,(y,z))`는 할당 된 총 수 인 튜플을,는 레지스터의 값이 고,은 `x = y + z` `y` 가비지 비트 수입니다 `LittleEndian` `z` .

## <a name="second-parameter"></a>두 번째 매개 변수

계수 배열의 일회용 $ \ sum_j | \ alpha_j | $입니다.

## <a name="third-parameter"></a>세 번째 매개 변수

단일 $U $입니다.

## <a name="example"></a>예

다음 코드 조각에서는 $3 $-stbit 상태 $ \rho = \ sum_ {j = 0} ^ {4} \frac{| alpha_j |}의 purification를 준비 합니다. {\ sum_k | \ alpha_k |} \ket{j}\bra{j} $, where $ \vec\alpha = (1.0, 2.0, 3.0, 4.0, 5.0) $ 및 오류는 `1e-3` 입니다.

```qsharp
let coefficients = [1.0,2.0,3.0,4.0,5.0];
let targetError = 1e-3;
let ((nTotalQubits, (nIndexQubits, nGarbageQubits)), oneNorm, op) = QuantumROM(targetError, coefficients);
using (indexRegister = Qubit[nIndexQubits]) {
    using (garbageRegister = Qubit[nGarbageQubits]) {
        op(LittleEndian(indexRegister), garbageRegister);
    }
}
```

## <a name="references"></a>참조

- 선형 T 복잡성 Ryan Babbush, Craig Gidney, Dominic Berry, 네, Spectra Wiebe, Jarrod McClean, Alexandru 고, 연한, 오스틴 Fowler, Hartmut Neven를 사용 하 여 퀀텀 회로에서 전자 인코딩 https://arxiv.org/abs/1805.03662