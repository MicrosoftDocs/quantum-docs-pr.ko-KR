---
uid: Microsoft.Quantum.Arithmetic.FixedPoint
title: FixedPoint 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: FixedPoint
qsharp.summary: Represents a register of qubits encoding a fixed-point number. Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.
ms.openlocfilehash: 0fea6e4ee1b8c5391e815217f1ddf9e511d46463
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223105"
---
# <a name="fixedpoint-user-defined-type"></a>FixedPoint 사용자 정의 형식

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)


고정 소수점 수에 해당 하는 비트의 레지스터를 나타냅니다. 는 이진 점의 왼쪽에 있는 값과 같은 정수 (즉, 1 보다 크거나 같은 가중치 비트)와 퀀텀 레지스터로 구성 됩니다.

```qsharp

newtype FixedPoint = (Int, Qubit[]);
```

