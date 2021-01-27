---
uid: Microsoft.Quantum.Canon.TrotterArbitraryImplCA
title: TrotterArbitraryImplCA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterArbitraryImplCA
qsharp.summary: Recursive implementation of even-order Trotter–Suzuki integrator.
ms.openlocfilehash: bb93517a479ce344277bfe97d070e6630a8fccc0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840093"
---
# <a name="trotterarbitraryimplca-operation"></a>TrotterArbitraryImplCA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


짝수 order Trotter – Suzuki 통합자의 재귀 구현입니다.

```qsharp
operation TrotterArbitraryImplCA<'T> (order : Int, (nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="order--int"></a>순서: [Int](xref:microsoft.quantum.lang-ref.int)

Trotter-Suzuki 통합자의 순서입니다.


### <a name="nsteps--int"></a>n 단계: [Int](xref:microsoft.quantum.lang-ref.int)

시간 단계로 분해할 작업 수입니다.


### <a name="op--intdoublet--unit--is-adj--ctl"></a>op: ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

분해를 위해 인덱스 입력 (형식 `Int` ) 및 시간 입력 (형식) 및 퀀텀 레지스터 (형식)를 허용 하는 작업 `Double` `'T` 입니다.


### <a name="stepsize--double"></a>Stsize: [Double](xref:microsoft.quantum.lang-ref.double)

시뮬레이션의 각 단계 크기에 대 한 승수입니다.


### <a name="target--t"></a>대상: ' '

작업이 작동 하는 퀀텀 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다

각 시간 단계가 작동 해야 하는 형식입니다. 일반적으로 `Qubit[]` 또는 `Qubit` 입니다.