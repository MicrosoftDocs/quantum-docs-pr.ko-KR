---
uid: Microsoft.Quantum.Chemistry.HTermToGenIdx
title: HTermToGenIdx 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermToGenIdx
qsharp.summary: Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.
ms.openlocfilehash: 59391a882fdbc55172ee93a7428c1735bbb29500
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216033"
---
# <a name="htermtogenidx-function"></a>HTermToGenIdx 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Chemistry)

패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


데이터 형식의 Hamiltonian 항을 `HTerm` GeneratorIndex로 변환 합니다.

```qsharp
function HTermToGenIdx (term : Microsoft.Quantum.Chemistry.HTerm, termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>입력

### <a name="term--hterm"></a>용어: [Hterm](xref:Microsoft.Quantum.Chemistry.HTerm)

형식의 입력 데이터 `HTerm` 입니다.


### <a name="termtype--int"></a>termType: [Int](xref:microsoft.quantum.lang-ref.int)[]

추가 정보를 GeneratorIndex에 추가 했습니다.



## <a name="output--generatorindex"></a>출력: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

가 나타내는 Hamiltonian 용어를에 `term` 의해 추가 된 추가 정보와 함께 나타내는 GeneratorIndex `termType` 입니다.