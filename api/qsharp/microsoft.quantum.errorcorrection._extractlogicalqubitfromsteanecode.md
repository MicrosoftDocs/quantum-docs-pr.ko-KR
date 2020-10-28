---
uid: Microsoft.Quantum.ErrorCorrection._ExtractLogicalQubitFromSteaneCode
title: _ExtractLogicalQubitFromSteaneCode 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: _ExtractLogicalQubitFromSteaneCode
qsharp.summary: >-
  Syndrome measurement and the inverse of embedding.

  $X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit. This asymmetry leads to a different syndrome extraction routine. One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.
ms.openlocfilehash: 71390feb84660cc9bf7bb12b64eac6d3ca512387
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712559"
---
# <a name="_extractlogicalqubitfromsteanecode-operation"></a>_ExtractLogicalQubitFromSteaneCode 작업

네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)

패키지 [](https://nuget.org/packages/)


증후군 측정과 포함의 역함수입니다.

$X $-및 $Z $-stabilizers은 특정 인코딩 회로 선택 때문에 동일 하 게 처리 되지 않습니다.
이 비대칭는 다른 증후군 추출 루틴으로 이어집니다.
이는 코드 상태에서 직접 여러 가지 증후군 비트 Pauli 연산자를 측정 하 여이를 측정할 수 있지만 추출을 목적으로 인해 추가 ancillas 없이 증후군 측정값을 수행할 수 있는 단일의 비트에 논리가 반환 됩니다.

```qsharp
operation _ExtractLogicalQubitFromSteaneCode (code : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit, Int, Int)
```


## <a name="input"></a>입력

### <a name="code--logicalregister"></a>코드: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)





## <a name="output--qubitintint"></a>Output[: (가,](xref:microsoft.quantum.lang-ref.qubit)[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))

$X $-증후군 및 $Z $-증후군에 대 한 논리 비트 및 정수 쌍입니다.
이는 단일 $X $ 또는 $Z $-오류가 측정 된 증후군를 발생 시킨 코드의 인덱스를 나타냅니다.

## <a name="remarks"></a>설명

`internal`단위 테스트가이 작업에 직접적으로 종속 되므로이 작업은으로 표시 되지 않습니다. 이후 향상 된 기능으로 서, 단위 테스트는 공용 callables에만 종속 되도록 리팩터링 해야 합니다.

> [!WARNING]
> 이 루틴은 Steane의 7abit 코드에 대 한 특정 인코딩 회로에 맞게 조정 됩니다. 인코딩 회로가 수정 되 면 증후군 결과가 다르게 해석 될 수 있습니다.