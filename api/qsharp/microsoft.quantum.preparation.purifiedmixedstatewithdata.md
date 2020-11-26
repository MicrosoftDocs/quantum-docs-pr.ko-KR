---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateWithData
title: PurifiedMixedStateWithData 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateWithData
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed\rstate, entangled with a register representing a given collection of data.\rA \"purified mixed state with data\" refers to a state of the form Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |\U0001D465ᵢ⟩ |garbageᵢ⟩,\rwhere each \U0001D465ᵢ is a bitstring encoding additional data associated with the register |\U0001D456⟩.\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: c89ee8f5df58e5d6b154b67d2b39db208bc8a215
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229956"
---
# <a name="purifiedmixedstatewithdata-function"></a>PurifiedMixedStateWithData 함수

네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 데이터 컬렉션을 나타내는 레지스터와 함께 지정 된 혼합 된 상태의 purification을 준비 하는 작업을 반환 합니다.
"Purified mixed state with data"는 Σi √ pi | i ⟩ | 크 ⟩ | garbagei ⟩ 형식의 상태를 나타냅니다. 여기서 각 크 크는 register | i ⟩에 연결 된 추가 데이터를 인코딩하는 bitstring입니다.

자세한 내용은 https://arxiv.org/pdf/1805.03662.pdf?page=15 을 참조 하세요.

```qsharp
function PurifiedMixedStateWithData (targetError : Double, coefficients : (Double, Bool[])[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a>설명

는 퀀텀 ROM 기술을 사용 하 여 지정 된 밀도 행렬을 나타내고 해당 표현을 상태 준비 작업으로 반환 합니다.

특히 $ 계수의 $ \ alpha_j $ $N 목록과 각 계수와 연결 된 bitstring $ \vec{x} j $ 목록이 제공 됩니다._이 함수는 퀀텀 ROM 기술을 사용 하 여 근사값 $ $ \begin{align} \tilde\rho = \sum_{j = 0} ^ {n-1} p_j \ket{j}\bra{j} \otimes \ket{\vec{x} _j} \bra{\vec{x}_j} \end{align} $ $의 혼합 된 상태 $ $ \begin{align} \rho = \sum_{j = 0} ^ {n-1} \ frac {| alpha_j |}을 준비 하는 작업을 반환 합니다. {\ sum_k | \ alpha_k |} \ket{j}\bra{j} \otimes \ket{\vec{x} _j} \bra{\vec{x} _j}, \end{align} $ $ (각 $p _j alpha_j $는 $ $ \begin{align} \left | p_j \frac{| \ alpha_j |} {\ sum_k | \ alpha_k |} \le \frac{\epsilon}{N} \end{align} $ $ $j $.

에서 처음에는 $ \ket \ket{00\cdots 0} 상태로 인덱스 레지스터가 전달 되 고 가비지의 레지스터가 발생 합니다. {0} 반환 된 작업은 두 레지스터를 모두 $ \tilde \rho $, $ $ \begin{align} \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j} \ket{\vec{x} _j} \ket{\text{garbage} _j}, \end{align} $ $로 반환 합니다 .이는 가비지 레지스터를 다시 설정 하거나 할당 취소 하 여 대상 오류 $ \tilde $ 내에서 원하는 준비를 수행 합니다.

## <a name="input"></a>입력

### <a name="targeterror--double"></a>targetError: [Double](xref:microsoft.quantum.lang-ref.double)

$ \Epsilon $ 대상 오류입니다.


### <a name="coefficients--doublebool"></a>계수: ([Double](xref:microsoft.quantum.lang-ref.double),[Bool](xref:microsoft.quantum.lang-ref.bool)[]) []

각 계수와 연결 된 bitstring $ \vec{x} _j $와 함께 기본 상태의 확률을 지정 하는 $N $ 계수의 배열입니다.
음수 $-\ alpha_j $는 긍정 $ | \ alpha_j | $로 처리 됩니다.



## <a name="output--mixedstatepreparation"></a>출력: [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)

$ \Tilde \rho $를 조인트 인덱스 및 가비지 레지스터에 purification로 준비 하는 작업입니다.

## <a name="remarks"></a>설명

이 작업에 제공 되는 계수는 1을 기준으로 정규화 됩니다 .이에 따라 계수는 항상 유효한 범주 확률 분포를 설명 하는 것으로 간주 됩니다.

## <a name="references"></a>참조 항목

- 선형 T 복잡성 Ryan Babbush, Craig Gidney, Dominic Berry, 네, Spectra Wiebe, Jarrod McClean, Alexandru 고, 연한, 오스틴 Fowler, Hartmut Neven를 사용 하 여 퀀텀 회로에서 전자 인코딩 https://arxiv.org/abs/1805.03662

## <a name="see-also"></a>참고 항목

- [PurifiedMixedState.](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)