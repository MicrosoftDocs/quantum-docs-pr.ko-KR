---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: AllowAtMostNCallsCA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: bb6ba2615b571b0d9d056b93f8e36d2dec0c4a21
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853532"
---
# <a name="allowatmostncallsca-operation"></a>AllowAtMostNCallsCA 작업

네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


이 작업 및 해당 adjoint 호출 사이에는 지정 된 작업이 지정 된 횟수 만큼만 호출 됨을 어설션 합니다.

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit is Adj
```


## <a name="input"></a>입력

### <a name="ntimes--int"></a>nTimes: [Int](xref:microsoft.quantum.lang-ref.int)

호출 될 수 있는 최대 횟수입니다 `op` .


### <a name="op--tinput--toutput--is-adj--ctl"></a>op: ' TInput => ' TOutput is Adj + Ctl

호출을 제한 해야 하는 작업입니다.


### <a name="message--string"></a>메시지: [문자열](xref:microsoft.quantum.lang-ref.string)

실패 시 표시 되는 메시지입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="tinput"></a>'TInput


### <a name="toutput"></a>' TOutput



## <a name="example"></a>예

다음 코드 조각은이 진단을 지 원하는 컴퓨터에서 실행 되는 경우 실패 합니다.

```qsharp
using (register = Qubit[4]) {
    within {
        AllowAtMostNCallsCA(3, H, "Too many calls to H.");
    } apply {
        // Fails since this calls H four times, rather than the
        // allowed maximum of three.
        ApplyToEach(H, register);
    }
}
```

## <a name="remarks"></a>설명

이 작업을 지원 하지 않는 대상에서는이 작업을 수행할 수 없습니다.