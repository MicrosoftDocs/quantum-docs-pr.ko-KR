---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: ReflectAboutInteger 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: e034f0a24d5c2f0465ebd1914b28cb8c695d978c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719713"
---
# <a name="reflectaboutinteger-operation"></a>ReflectAboutInteger 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지 [](https://nuget.org/packages/)


지정 된 기존 정수에 대 한 퀀텀 레지스터를 반영 합니다.

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>Description

처음에는 $ \ sum_i \ alpha_i \ket{i} $ 상태에 있는 퀀텀 레지스터가 제공 됩니다. 여기서 각 $ \ket{i} $은 정수 $i $를 나타내는 기본 상태 이며 지정 된 정수 $ \ket{j} $, $ $ \ sum_i (-1) ^ {\ delta_ {ij}} \ alpha_i \ket{i} $ $에 대 한 기본 상태에 대 한 레지스터의 상태를 반영 합니다.

## <a name="input"></a>입력

### <a name="index--int"></a>인덱스: [Int](xref:microsoft.quantum.lang-ref.int)

반영할 기준 상태를 인덱싱하는 기존 정수입니다.


### <a name="reg--littleendian"></a>reg: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)





## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

추가 보조 비트를 명시적으로 할당 하지 않고이 작업을 내부에서 구현 합니다.