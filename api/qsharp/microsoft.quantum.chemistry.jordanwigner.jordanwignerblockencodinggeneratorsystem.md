---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerBlockEncodingGeneratorSystem
title: JordanWignerBlockEncodingGeneratorSystem 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerBlockEncodingGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the Pauli `GeneratorIndex`.
ms.openlocfilehash: cffbb1e2d9b6566bf6c3da642e4479968f774ca3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839041"
---
# <a name="jordanwignerblockencodinggeneratorsystem-function"></a>JordanWignerBlockEncodingGeneratorSystem 함수

네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


에 설명 된 Hamiltonian를 `JWOptimizedHTerms` Pauli로 표현 된로 변환 합니다 `GeneratorSystem` `GeneratorIndex` .

```qsharp
function JordanWignerBlockEncodingGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>입력

### <a name="data--jwoptimizedhterms"></a>데이터: [JWOptimizedHTerms](xref:Microsoft.Quantum.Chemistry.JordanWigner.JWOptimizedHTerms)

형식의 Hamiltonian에 대 한 설명 `JWOptimizedHTerms` 입니다.



## <a name="output--generatorsystem"></a>출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Hamiltonian의 표현 `GeneratorSystem` 입니다.