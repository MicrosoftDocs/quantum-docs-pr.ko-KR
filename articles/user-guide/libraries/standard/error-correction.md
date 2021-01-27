---
title: 표준 라이브러리의 오류 수정 Q#
description: 프로그램에서 오류 수정 코드를 사용 하는 방법에 대해 알아봅니다 Q# .
author: QuantumWriter
uid: microsoft.quantum.libraries.error-correction
ms.author: martinro
ms.date: 12/11/2017
ms.topic: conceptual
no-loc:
- Q#
- $$v
ms.openlocfilehash: fc8e46aa22cb2575de42cfc3d4f57c43e5d3f7b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857204"
---
# <a name="error-correction"></a>오류 수정 #

## <a name="introduction"></a>소개 ##

기존 컴퓨팅에서 오류 로부터 비트를 보호 하려는 경우에는 데이터 비트를 반복 하 여 *논리 비트* 를 통해 비트를 나타내는 것이 충분할 수 있습니다.
예를 들어 $ \overline {0} = $0은 데이터 비트 0의 인코딩입니다. 여기서 레이블 0 위의 줄을 사용 하 여 0 상태에 있는 비트의 인코딩입니다.
마찬가지로 $ \overline {1} = $111를 사용 하는 경우 단일 비트 대칭 이동 오류 로부터 보호 하는 간단한 반복 코드가 있습니다.
즉, 3 비트 중 하나라도 대칭 이동 하는 경우 과반수 투표를 수행 하 여 논리 비트의 상태를 복구할 수 있습니다.
이 특정 예제에서는 클래식 오류 수정이 훨씬 더 다양 한 주제 이지만 ( [코딩 이론에 대 한 보푸라기가를 도입 하](https://www.springer.com/us/book/9783540641339)는 것이 권장 됨) 위의 반복 코드는 이미 퀀텀 정보를 보호할 때 발생할 수 있는 문제를 가리킵니다.
즉, [복제 안 함 정리](xref:microsoft.quantum.concepts.pauli#the-no-cloning-theorem) 는 각 개별의 비트를 측정 하 고 위의 클래식 코드와 유사한 방식으로 과반수 투표를 수행 하는 경우 보호 하려고 하는 정확한 정보를 잃어버린 것을 의미 합니다.

퀀텀 설정에서 측정이 문제가 있음을 알 수 있습니다. 위의 인코딩을 여전히 구현할 수 있습니다.
이를 통해 퀀텀 사례에 대 한 오류 수정을 일반화 하는 방법을 확인 하는 것이 좋습니다.
따라서 $ \ket{\overline {0} } = \ket {000} = \ket {0} \otimes \ket {0} \otimes \ket {0} $ 및 let $ \ket{\overline {1} } = \ket $를 사용 {111} 합니다.
그런 다음, 선형으로 모든 입력에 대 한 반복 코드를 정의 했습니다. 예를 들어 $ \ket{\overline{+}} = (\ket{\overline {0} } + \ket{\overline {1} })/\sqrt {2} = (\ket {000} + \ket {111} )/\sqrt {2} $입니다.
특히, 비트 대칭 이동 오류 $X는 중간의 두 분기에 필요한 수정 내용이 정확 하 게 $X _1 $: $ $ \begin{align} X_1 \ket{\overline{+}} & = \frac {1} {\sqrt {2} } \left (X_1 \ket {000} + X_1 \ket {111} \right) \\ \\ & = \frac {1} {\sqrt {2} } \left (\ket {010} + \ket {101} \right) 인 것을 확인할 수 있습니다.
\end{align} $ $

보호 하려는 상태를 측정 하지 않고이를 어떻게 확인할 수 있는지 확인 하려면 각각의 서로 다른 비트 대칭 이동 오류가 다음 논리 상태에 미치는 것을 기록 하는 것이 좋습니다.

| 오류 $E $ | $E \ket{\overline {0} } $ | $E \ket{\overline {1} } $ |
| --- | --- | --- |
| $\boldone$ | $ \ket {000} $ | $ \ket {111} $ |
| $X_0$ | $ \ket {100} $ | $ \ket {011} $ |
| $X_1$ | $ \ket {010} $ | $ \ket {101} $ |
| $X_2$ | $ \ket {001} $ | $ \ket {110} $ |

인코딩할 상태를 보호 하기 위해 $ \ket{\overline {0} } $ 및 $ \ket{\overline} $를 구별 하지 않고 세 개의 오류와 id $ \boldone $를 구별할 수 있어야 합니다 {1} .
예를 들어 _0 $ $Z를 측정 하 {0} 는 경우 오류 없음 사례에서 $ \ket{\overline} $ 및 $ \ket{\overline} $에 대해 다른 결과를 얻게 {1} 되므로는 인코딩된 상태를 축소 합니다.
반면, 각 계산 기준 상태에서 처음 두 비트의 패리티 $Z _0 Z_1 $을 측정 하는 것이 좋습니다.
Pauli 연산자의 각 측정 측정은 측정 되는 상태에 해당 하는 eigenvalue를 확인 하므로, 위의 표에 있는 각 state $ \ket{\psi} $에 대해 $Z _0 Z_1 \ket{\psi} $을 계산 하 여 $ \pm\ket{\psi} $가 있는지 확인할 수 있습니다.
$Z _0 Z_1 \ket {000} = \ket {000} $ 이며 {111} {111} 이 측정값이 두 인코딩된 상태에 대해 동일한 작업을 수행 하는 것으로 결론을 Z_1 $Z 합니다.
반면에 _0 Z_1 \ket {100} =-\ket {100} $ 및 $Z _0 Z_1 \ket {011} =-\ket $를 $Z 합니다 {011} . 따라서 $Z _0 Z_1 $를 측정 하면 발생 한 오류에 대 한 유용한 정보가 표시 됩니다.

이를 강조 하기 위해 위의 표를 반복 하지만 각 행에 $Z _0 Z_1 $ 및 $Z _1 Z_2 $의 측정 결과를 추가 합니다.
각 측정 결과는 Q# `Result` 각각 및의 값에 해당 하는 $ + $ 또는 $-$ 중에서 관찰 된 eigenvalue의 부호를 기준으로 합니다 `Zero` `One` .

| 오류 $E $ | $E \ket{\overline {0} } $ | $E \ket{\overline {1} } $ | $Z _0 Z_1 $ 결과 | $Z _1 Z_2 $의 결과 |
| --- | --- | --- | --- | --- |
| $\boldone$ | $ \ket {000} $ | $ \ket {111} $ | $+$ | $+$ |
| $X_0$ | $ \ket {100} $ | $ \ket {011} $ | $-$ | $+$ |
| $X_1$ | $ \ket {010} $ | $ \ket {101} $ | $-$ | $-$ |
| $X_2$ | $ \ket {001} $ | $ \ket {110} $ | $+$ | $-$ |

따라서 두 측정값의 결과는 어떤 비트 대칭 오류가 발생 했는지를 고유 하 게 결정 하지만 인코딩된 상태에 대 한 정보는 노출 하지 않습니다.
이러한 결과를 *증후군* 로 호출 하 고 증후군를 *복구* 로 발생 시킨 오류에 다시 매핑하는 프로세스를 참조 합니다.
특히 복구는 발생 하는 증후군의 입력으로 사용 되는 *기존* 유추 프로시저 이며 발생 했을 수 있는 오류를 해결 하는 방법에 대 한 prescription를 반환 합니다.

> [!NOTE]
> 위의 비트 대칭 이동 코드는 단일 비트 대칭 오류에 대해서만 수정할 수 있습니다. 즉, `X` 단일 비트에 대해 작동 하는 연산입니다.
> 둘 이상의 `X` 추가 비트에 적용 하면 $ \ket{\overline {0} } $가 $ \ket{\overline {1} } $에 다음 복구에 매핑됩니다.
> 마찬가지로 단계 전환 작업을 적용 하면 $ `Z` \ket{\overline {1} } $가 $-\ket{\overline} $에 매핑되고 $ {1} \ket{\overline{+}} $가 $ \ket{\overline {-} } $로 매핑됩니다.
> 보다 일반적으로 더 많은 오류를 처리 하 고 $Z $ errors 및 $X $ errors를 처리 하는 코드를 만들 수 있습니다.

모든 코드 상태에서 동일한 방식으로 작동 하는 퀀텀 오류 수정의 측정을 설명할 수 있는 정보는 *안정기 정해진* 의 핵심입니다.
Q#라고은 안정기 코드에서의 인코딩 및 디코딩을 설명 하 고, 오류에서 복구 하는 방법을 설명 하기 위한 프레임 워크를 제공 합니다.
이 섹션에서는 몇 가지 간단한 퀀텀 오류 수정 코드에이 프레임 워크 및 해당 응용 프로그램을 설명 합니다.

> [!TIP]
> 안정기 정해진에 대 한 전체 소개는이 섹션의 범위를 벗어나는 것입니다.
> [Gottesman 2009](https://arxiv.org/abs/0904.2557)에 대 한 자세한 내용은 독자를 대상으로 합니다.

## <a name="representing-error-correcting-codes-in-no-locq"></a>오류 수정 코드 표시 Q# ##

오류 수정 코드를 지정 하는 데 도움이 되도록 Q# 라고은 다음과 같이 여러 가지 고유한 사용자 정의 형식을 제공 합니다.

- <xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister>`= Qubit[]`: 비트 레지스터는 오류 수정 코드의 코드 블록으로 해석 되어야 함을 나타냅니다.
- <xref:Microsoft.Quantum.ErrorCorrection.Syndrome>`= Result[]`: 측정 결과 배열을 코드 블록에서 측정 된 증후군 해석 해야 함을 나타냅니다.
- <xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn>`= (Syndrome -> Pauli[])`: *기존* 함수를 사용 하 여 증후군를 해석 하 고 적용 해야 하는 수정 사항을 반환 해야 함을 나타냅니다.
- <xref:Microsoft.Quantum.ErrorCorrection.EncodeOp>`= ((Qubit[], Qubit[]) => LogicalRegister)`: 오류 수정 코드의 코드 블록을 생성 하기 위해 작업에서 새로운 ancilla 된 비트와 함께 데이터를 표현 하는 데 필요한 비트를 사용 함을 나타냅니다.
- <xref:Microsoft.Quantum.ErrorCorrection.DecodeOp>`= (LogicalRegister => (Qubit[], Qubit[]))`: 분해는 작업에서 코드 블록을 데이터 요소에 수정 하 고 증후군 정보를 나타내는 데 사용 되는 ancilla을 사용 하는 작업을 나타냅니다.
- <xref:Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp>`= (LogicalRegister => Syndrome)`: 코드에서 보호 되는 상태를 방해 하지 않고 코드 블록에서 증후군 정보를 추출 하는 데 사용 해야 하는 작업을 나타냅니다.

마지막으로 라고은 <xref:Microsoft.Quantum.ErrorCorrection.QECC> 퀀텀 오류 수정 코드를 정의 하는 데 필요한 다른 형식을 수집 하기 위한 형식을 제공 합니다. 각 안정기 퀀텀 코드와 연결 된 코드 $n 길이는 $, logical st$d bits의 숫자 $k $, ⟦ $n $, $k $, $d $ ⟧ 표기법에서 편리 하 게 그룹화 되는 것입니다. 예를 들어 <xref:Microsoft.Quantum.ErrorCorrection.BitFlipCode> 함수는 ⟦ 3, 1, 1 ⟧ 비트 대칭 코드를 정의 합니다.

```qsharp
let encodeOp = EncodeOp(BitFlipEncoder);
let decodeOp = DecodeOp(BitFlipDecoder);
let syndMeasOp = SyndromeMeasOp(MeasureStabilizerGenerators([
    [PauliZ, PauliZ, PauliI],
    [PauliI, PauliZ, PauliZ]
], _, MeasureWithScratch));
let code = QECC(encodeOp, decodeOp, syndMeasOp);
```

형식에는 `QECC` 복구 기능이 포함 되어 *있지* 않습니다.
이렇게 하면 코드 자체의 정의를 변경 하지 않고 오류를 수정 하는 데 사용 되는 복구 기능을 변경할 수 있습니다. 이러한 기능은 특성화 측정의 피드백을 복구로 간주 되는 모델로 통합할 때 특히 유용 합니다.

이러한 방식으로 코드를 정의한 후에는 작업을 사용 하 여 <xref:Microsoft.Quantum.ErrorCorrection.Recover> 오류를 복구할 수 있습니다.

```qsharp
let code = BitFlipCode();
let fn = BitFlipRecoveryFn();
let X0 = ApplyPauli([PauliX, PauliI, PauliI], _);
using (scratch = Qubit[nScratch]) {
    let logicalRegister = encode(data, scratch);
    // Cause an error.
    X0(logicalRegister);
    Recover(code, fn, logicalRegister);
    let (decodedData, decodedScratch) = decode(logicalRegister);
    ApplyToEach(Reset, decodedScratch);
}
```

이에 대 한 자세한 내용은 [비트 대칭 코드 샘플](https://github.com/microsoft/Quantum/tree/main/samples/error-correction/bit-flip-code)을 살펴보세요.

비트 대칭 코드 외에도 Q# 라고은 [5 ~ 5 비트 코드](https://arxiv.org/abs/quant-ph/9602019)및 [일곱 번째 비트 코드](https://arxiv.org/abs/quant-ph/9705052)의 구현과 함께 제공 되며, 둘 다 임의의 단일 기능 비트 오류를 수정할 수 있습니다.
