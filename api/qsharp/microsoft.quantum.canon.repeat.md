---
uid: Microsoft.Quantum.Canon.Repeat
title: 작업 반복
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 5aedd056b851b8d8d7c25a32eb22587292e132a8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715597"
---
# <a name="repeat-operation"></a>작업 반복

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)

패키지 [](https://nuget.org/packages/)


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



## <a name="see-also"></a>참고 항목

- [Microsoft 양자 Many](xref:Microsoft.Quantum.Arrays.DrawMany)
- [RepeatA입니다.](xref:Microsoft.Quantum.Canon.RepeatA)
- [Microsoft 양자.](xref:Microsoft.Quantum.Canon.RepeatC)
- [Microsoft 양자.](xref:Microsoft.Quantum.Canon.RepeatCA)