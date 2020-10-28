---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: HTermsToGenIdx 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: 73324a48cc4b42de0d5d8618ad9e833d289125f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714855"
---
# <a name="htermstogenidx-function"></a>HTermsToGenIdx 함수

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Chemistry)

패키지 [](https://nuget.org/packages/)


인덱스를 데이터 형식의 Hamiltonian 용어로 변환 `HTerm[]` 합니다.

```qsharp
function HTermsToGenIdx (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[], idx : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>입력

### <a name="data--hterm"></a>데이터: [Hterm](xref:Microsoft.Quantum.Chemistry.HTerm)[]

형식의 입력 데이터 `HTerm[]` 입니다.


### <a name="termtype--int"></a>termType: [Int](xref:microsoft.quantum.lang-ref.int)[]

추가 정보를 GeneratorIndex에 추가 했습니다.


### <a name="idx--int"></a>idx: [Int](xref:microsoft.quantum.lang-ref.int)

Hamiltonian의 용어에 대 한 인덱스



## <a name="output--generatorindex"></a>출력: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

가 나타내는 Hamiltonian 용어를에 `data[idx]` 의해 추가 된 추가 정보와 함께 나타내는 GeneratorIndex `termType` 입니다.