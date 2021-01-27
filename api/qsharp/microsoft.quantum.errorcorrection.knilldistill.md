---
uid: Microsoft.Quantum.ErrorCorrection.KnillDistill
title: KnillDistill 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: KnillDistill
qsharp.summary: Implements the Knill magic state distillation algorithm.
ms.openlocfilehash: 4eff99eebb1e271d240513f827c6e93973ef79a6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853112"
---
# <a name="knilldistill-operation"></a>KnillDistill 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


Knill magic state 추출을 알고리즘을 구현 합니다.

```qsharp
operation KnillDistill (roughMagic : Qubit[]) : Bool
```


## <a name="description"></a>설명

매직 상태 $ $ \begin{align} \cos\frac{\pi} {8} \ket {0} + \sin \frac{\pi} \ket \end{align}의 15 개의 대략적인 {8} 복사본 {1} 을 지정 하면, $ $는 고품질의 복사본 하나를 생성 합니다.

## <a name="input"></a>입력

### <a name="roughmagic--qubit"></a>roughMagic: [](xref:microsoft.quantum.lang-ref.qubit)[]

매직 상태의 대략적인 복사본을 포함 하는 15 개의 비트 레지스터입니다. 이 추출을 절차의 다음 응용 프로그램에 `roughMagic[0]` 는 고품질 복사본이 하나 포함 되 고 나머지 레지스터는 $ \ket{00\cdots 0} $ 상태로 다시 설정 됩니다.



## <a name="output--bool"></a>출력: [Bool](xref:microsoft.quantum.lang-ref.bool)

이면 `true` 프로시저 성공 및 고품질 복사를 수락 해야 합니다. 이면 `false` 프로시저가 실패 하 고 레지스터의 상태가 undefined로 간주 되어야 합니다.

## <a name="remarks"></a>설명

Knill 알고리즘을 따릅니다.
그러나 현재 구현은 너무 많은 비트를 사용 하기 때문에 최적 상태가 아닙니다.
매직 상태는이 루틴에 삽입 되며,이 경우 더 나은 프로토콜이 있습니다.

## <a name="references"></a>참조

- [Knill](https://arxiv.org/abs/quant-ph/0402171)