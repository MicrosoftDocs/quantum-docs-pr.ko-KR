---
uid: Microsoft.Quantum.Simulation._AddGeneratorSystems
title: _AddGeneratorSystems 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _AddGeneratorSystems
qsharp.summary: Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.
ms.openlocfilehash: e51addb38da99e508a71dffa757cd7fb19c89dcd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858002"
---
# <a name="_addgeneratorsystems-function"></a>_AddGeneratorSystems 함수

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


새를 `GeneratorSystem` 만드는 두 개의를 추가 `GeneratorSystem` 합니다.

```qsharp
function _AddGeneratorSystems (idxTerm : Int, nTermsA : Int, nTermsB : Int, generatorIndexFunctionA : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex), generatorIndexFunctionB : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>입력

### <a name="idxterm--int"></a>idxTerm: [Int](xref:microsoft.quantum.lang-ref.int)




### <a name="ntermsa--int"></a>nTermsA: [Int](xref:microsoft.quantum.lang-ref.int)




### <a name="ntermsb--int"></a>nTermsB: [Int](xref:microsoft.quantum.lang-ref.int)




### <a name="generatorindexfunctiona--int---generatorindex"></a>generatorIndexFunctionA: [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)




### <a name="generatorindexfunctionb--int---generatorindex"></a>generatorIndexFunctionB: [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)





## <a name="output--generatorindex"></a>출력: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)



## <a name="remarks"></a>설명

이는 중간 단계 이며 호출할 수 없습니다.