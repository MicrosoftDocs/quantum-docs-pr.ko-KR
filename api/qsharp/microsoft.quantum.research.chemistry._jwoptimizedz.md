---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedZ
title: _JWOptimizedZ 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedZ
qsharp.summary: Applies a Rz rotation, with a C-NOT trick to double phase in phase estimation.
ms.openlocfilehash: 76c96153b6baf8b593e0770a44b6190c075c8f53
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854224"
---
# <a name="_jwoptimizedz-operation"></a>_JWOptimizedZ 작업

네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .

패키지: [Microsoft](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry) .


단계 추정에서 2 단계에 대 한 C NOT 트릭을 사용 하 여 Rz 회전을 적용 합니다.

```qsharp
operation _JWOptimizedZ (angle : Double, parityQubit : Qubit, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="angle--double"></a>angle: [Double](xref:microsoft.quantum.lang-ref.double)

Rz 회전의 각도입니다.


### <a name="parityqubit--qubit"></a>Paritybit: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

시간 진화의 부호를 결정 하는의 비트입니다.


### <a name="qubit--qubit"></a>작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)

