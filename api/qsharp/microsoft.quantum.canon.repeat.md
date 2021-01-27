---
uid: Microsoft.Quantum.Canon.Repeat
title: 작업 반복
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 40ee191e8d9044f33aa1621303c70f7e0847e8f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852240"
---
# <a name="repeat-operation"></a>작업 반복

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 횟수 만큼 작업을 반복 합니다.

```qsharp
operation Repeat<'TInput> (op : ('TInput => Unit), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a>입력

### <a name="op--tinput--unit"></a>op: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) 

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
Repeat(U, 17, target);
(Bound(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a>참고 항목

- [Microsoft 양자 Many](xref:Microsoft.Quantum.Arrays.DrawMany)
- [RepeatA입니다.](xref:Microsoft.Quantum.Canon.RepeatA)
- [Microsoft 양자.](xref:Microsoft.Quantum.Canon.RepeatC)
- [Microsoft 양자.](xref:Microsoft.Quantum.Canon.RepeatCA)