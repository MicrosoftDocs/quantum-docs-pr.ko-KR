---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: StateGenerator 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: b4f6c3ca28e2976b6a0d58f4ef25ea943de9811e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854884"
---
# <a name="stategenerator-user-defined-type"></a>StateGenerator 사용자 정의 형식

네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)

패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


순차적 분류자에 대해 지정 된 입력을 준비 하는 작업을 설명 합니다.

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a>명명 된 항목

### <a name="nqubits--int"></a>N Bits: [Int](xref:microsoft.quantum.lang-ref.int)

인코딩된 입력이 정의 된 값입니다.
### <a name="prepare--littleendian--unit--is-adj--ctl"></a>준비: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

비트의 작은 endian 레지스터에서 인코딩된 입력을 준비 하는 연산입니다 `NQubits` .