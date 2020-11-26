---
uid: Microsoft.Quantum.Arrays.DrawMany
title: DrawMany 연산
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: 3185f2ec01a2b9d01cff82a0c4667f12483801a7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209998"
---
# <a name="drawmany-operation"></a>DrawMany 연산

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


지정 된 수의 샘플에 대해 작업을 반복 하 여 배열에서 해당 출력을 수집 합니다.

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a>입력

### <a name="op--tinput--toutput"></a>op: ' TInput => ' TOutput 

반복적으로 호출 되는 작업입니다.


### <a name="nsamples--int"></a>nSamples: [Int](xref:microsoft.quantum.lang-ref.int)

`op`을 (를) 수집 하기 위해 호출 하는 샘플의 수입니다.


### <a name="input--tinput"></a>입력: ' TInput

에 전달 되는 입력 `op` 입니다.



## <a name="output--toutput"></a>출력: ' TOutput []



## <a name="type-parameters"></a>형식 매개 변수

### <a name="tinput"></a>'TInput


### <a name="toutput"></a>' TOutput



## <a name="see-also"></a>참고 항목

- [Microsoft. 양자 반복](xref:Microsoft.Quantum.Canon.Repeat)