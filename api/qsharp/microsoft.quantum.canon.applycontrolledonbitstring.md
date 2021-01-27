---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: ApplyControlledOnBitString 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 82adc74e23e1d50cb6436176a973fdd1a0eeb3bd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841936"
---
# <a name="applycontrolledonbitstring-operation"></a>ApplyControlledOnBitString 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 비트 마스크로 지정 된 상태에 의해 제어 되는 단일 작업을 대상 레지스터에 적용 합니다.

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="bits--bool"></a>bits: [Bool](xref:microsoft.quantum.lang-ref.bool)[]

지정 된 단일 작업을 제어 하는 비트 문자열입니다.


### <a name="oracle--t--unit--is-adj--ctl"></a>oracle: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

대상 레지스터에 적용 될 단일 작업입니다.


### <a name="controlregister--qubit"></a>controlRegister: [bit](xref:microsoft.quantum.lang-ref.qubit)[]

의 응용 프로그램을 제어 하는 퀀텀 레지스터입니다 `oracle` .


### <a name="targetregister--t"></a>targetRegister: ' t

입력으로에 전달 되는 대상 레지스터 `oracle` 입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="remarks"></a>설명

에 지정 된 패턴은 `bits` 보다 짧을 수 있습니다 `controlRegister` .이 경우 추가 컨트롤의 비트는 무시 됩니다. 즉, $ \ket {0} $ 또는 $ \ket $에서 제어 되지 않습니다 {1} .
`bits`가 보다 길면 `controlRegister` 오류가 발생 합니다.

예를 들어는 `bits = [0,1,0,0,1]` `oracle` `controlRegister` 가 $ \ket {0} \ket {1} \ket {0} \ket {0} \ket {1} $ 상태에 있는 경우에만 적용 됩니다.