---
uid: Microsoft.Quantum.Canon.ControlledOnBitString
title: ControlledOnBitString 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnBitString
qsharp.summary: Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.
ms.openlocfilehash: 9435406506fc99fe211f5dce628b21c18ee4f9fe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216662"
---
# <a name="controlledonbitstring-function"></a>ControlledOnBitString 함수

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


컨트롤 레지스터 상태가 지정 된 비트 마스크에 해당 하는 경우 대상 레지스터에 oracle을 적용 하는 단일 작업을 반환 합니다.

```qsharp
function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="description"></a>Description

이 함수의 출력은 \begin{align} U \ket{b_0 b_1 \cdots b_ {n-1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_ {n-1}}와 같이 단일 변환 $U $로 나타낼 수 있는 작업입니다. \cdots \begin{cases} V \ket{\psi} & \t extrm{if} (b_0 b_1 \cdots b_ {n-1}) = \texttt{bits} \\ \\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} where $V $은 작업 동작을 나타내는 단일 변환입니다 `oracle` .

## <a name="input"></a>입력

### <a name="bits--bool"></a>bits: [Bool](xref:microsoft.quantum.lang-ref.bool)[]

지정 된 단일 작업을 제어 하는 비트 문자열입니다.


### <a name="oracle--t--unit--is-adj--ctl"></a>oracle: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

대상 레지스터에 적용 될 단일 작업입니다.



## <a name="output--qubitt--unit--is-adj--ctl"></a>출력[: (Adj](xref:microsoft.quantum.lang-ref.qubit)+ [], ' t) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl + Ctl

`oracle`컨트롤 레지스터 상태가 비트 마스크에 해당 하는 경우 대상 레지스터에 적용 되는 단일 작업입니다 `bits` .

## <a name="type-parameters"></a>형식 매개 변수

### <a name="t"></a>없습니다



## <a name="remarks"></a>설명

에 지정 된 패턴은 `bits` 보다 짧을 수 있습니다 `controlRegister` .이 경우 추가 컨트롤의 비트는 무시 됩니다. 즉, $ \ket {0} $ 또는 $ \ket $에서 제어 되지 않습니다 {1} .
`bits`가 보다 길면 `controlRegister` 오류가 발생 합니다.

부울 배열과 `bits` 단일 연산이 제공 되는 경우 `oracle` 이 함수의 출력은 다음 단계를 수행 하는 작업입니다.

* `X`의 요소에 해당 하는 컨트롤 레지스터의 각 요소에 작업을 적용 `false` 합니다 `bits` .
* `Controlled oracle`컨트롤 및 대상 레지스터에 적용 됩니다.
* `X`의 요소에 해당 하는 컨트롤 레지스터의 각 요소에 작업을 적용 하 여 `false` `bits` 컨트롤을 원래 상태로 되돌립니다.

함수 출력은 `Controlled` `ControlledOnBitString` `bits` 가와 같은 특수 한 경우입니다 `[true, ..., true]` .