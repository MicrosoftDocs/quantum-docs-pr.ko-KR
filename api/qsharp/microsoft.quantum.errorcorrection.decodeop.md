---
uid: Microsoft.Quantum.ErrorCorrection.DecodeOp
title: DecodeOp 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeOp
qsharp.summary: >-
  Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.

  The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.
ms.openlocfilehash: 0733ec016e50a320b162b111c7d87c32140fdacb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712412"
---
# <a name="decodeop-user-defined-type"></a><span data-ttu-id="7f576-102">DecodeOp 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="7f576-102">DecodeOp user defined type</span></span>

<span data-ttu-id="7f576-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="7f576-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="7f576-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7f576-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7f576-105">인코딩된 레지스터를 실제 레지스터로 디코딩하는 작업과 증후군을 기록 하는 데 사용 되는 스크래치 인스턴스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7f576-105">Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.</span></span>

<span data-ttu-id="7f576-106">DecodeOp에 대 한 인수는 EncodeOp에서 반환 하는 것과 동일 하며 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="7f576-106">The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.</span></span>

```qsharp

newtype DecodeOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => (Qubit[], Qubit[])));
```

