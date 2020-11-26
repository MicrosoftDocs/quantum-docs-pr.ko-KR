---
uid: Microsoft.Quantum.ErrorCorrection.DecodeOp
title: DecodeOp 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeOp
qsharp.summary: >-
  Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.

  The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.
ms.openlocfilehash: f1fc2851b7ed8b12cf8a47fabe794235a3083d31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201005"
---
# <a name="decodeop-user-defined-type"></a><span data-ttu-id="b9736-102">DecodeOp 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="b9736-102">DecodeOp user defined type</span></span>

<span data-ttu-id="b9736-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="b9736-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="b9736-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b9736-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b9736-105">인코딩된 레지스터를 실제 레지스터로 디코딩하는 작업과 증후군을 기록 하는 데 사용 되는 스크래치 인스턴스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b9736-105">Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.</span></span>

<span data-ttu-id="b9736-106">DecodeOp에 대 한 인수는 EncodeOp에서 반환 하는 것과 동일 하며 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="b9736-106">The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.</span></span>

```qsharp

newtype DecodeOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => (Qubit[], Qubit[])));
```

