---
uid: Microsoft.Quantum.Arithmetic.FixedPoint
title: FixedPoint 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: FixedPoint
qsharp.summary: Represents a register of qubits encoding a fixed-point number. Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.
ms.openlocfilehash: 18e85120647c5a1f41ccab5fbfb27ea602a279af
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843198"
---
# <a name="fixedpoint-user-defined-type"></a><span data-ttu-id="1e1a8-102">FixedPoint 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="1e1a8-102">FixedPoint user defined type</span></span>

<span data-ttu-id="1e1a8-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1e1a8-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1e1a8-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="1e1a8-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="1e1a8-105">고정 소수점 수에 해당 하는 비트의 레지스터를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1e1a8-105">Represents a register of qubits encoding a fixed-point number.</span></span> <span data-ttu-id="1e1a8-106">는 이진 점의 왼쪽에 있는 값과 같은 정수 (즉, 1 보다 크거나 같은 가중치 비트)와 퀀텀 레지스터로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e1a8-106">Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.</span></span>

```qsharp

newtype FixedPoint = (Int, Qubit[]);
```

