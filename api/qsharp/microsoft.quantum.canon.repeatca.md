---
uid: Microsoft.Quantum.Canon.RepeatCA
title: RepeatCA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: af93220562d6be27b2f41e770bd953e5e808fcbf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852201"
---
# <a name="repeatca-operation"></a>RepeatCA 작업

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 횟수 만큼 작업을 반복 합니다.

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="op--tinput--unit--is-adj--ctl"></a>op: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

반복적으로 호출 되는 작업입니다.


### <a name="ntimes--int"></a>nTimes: [Int](xref:microsoft.quantum.lang-ref.int)

호출 하는 횟수 `op` 입니다.


### <a name="input--tinput"></a>입력: ' TInput

에 전달 되는 입력 `op` 입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>형식 매개 변수

### <a name="tinput"></a>'TInput



## <a name="example"></a>예

다음은 동일 합니다.

```qsharp
RepeatCA(U, 17, target);
(BoundCA(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a>참고 항목

- [Microsoft 양자 Many](xref:Microsoft.Quantum.Arrays.DrawMany)
- [Microsoft. 양자 반복](xref:Microsoft.Quantum.Canon.Repeat)
- [RepeatA입니다.](xref:Microsoft.Quantum.Canon.RepeatA)
- [Microsoft 양자.](xref:Microsoft.Quantum.Canon.RepeatC)