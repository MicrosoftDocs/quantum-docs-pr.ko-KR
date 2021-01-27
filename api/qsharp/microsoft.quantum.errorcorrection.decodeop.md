---
uid: Microsoft.Quantum.ErrorCorrection.DecodeOp
title: DecodeOp 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeOp
qsharp.summary: >-
  Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.

  The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.
ms.openlocfilehash: 2b3d4558f6528c2e0f597398d12fc9331ab381b5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827380"
---
# <a name="decodeop-user-defined-type"></a><span data-ttu-id="f4cb4-102">DecodeOp 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="f4cb4-102">DecodeOp user defined type</span></span>

<span data-ttu-id="f4cb4-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="f4cb4-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="f4cb4-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f4cb4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f4cb4-105">인코딩된 레지스터를 실제 레지스터로 디코딩하는 작업과 증후군을 기록 하는 데 사용 되는 스크래치 인스턴스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f4cb4-105">Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.</span></span>

<span data-ttu-id="f4cb4-106">DecodeOp에 대 한 인수는 EncodeOp에서 반환 하는 것과 동일 하며 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="f4cb4-106">The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.</span></span>

```qsharp

newtype DecodeOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => (Qubit[], Qubit[])));
```

